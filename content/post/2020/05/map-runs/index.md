---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "map-runs: overlaying Runkeeper runs on a single map"
subtitle: "A simple python tool for combining GPS files in HTML"
summary: "A simple python tool for combining GPS files in HTML"
authors:
- admin
tags:
- running
- videogames
- python
categories: []
date: 2020-01-21T15:56:33+01:00
lastmod: 2020-01-21T15:56:33+01:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## **Background**

I always use [Runkeeper](https://runkeeper.com/) to track my runs. Its free version provides just about everything I need for following my running progress: charts for pace, elevation, cadence... and most importantly, it tracks my GPS position and renders it in a nice map:

{{< figure src="fig1.png" title="**Mapped run in my Runkeeper app**" lightbox="true" >}}

Although I really enjoy these functionalities, one thing that I always wanted to see was a single world map with all runs combined. This need started after I played the first DLC of _The Legend of Zelda: Breath of the Wild_. In it, I was introduced to an awesome feature: "Hero's Path Mode", which kept track of my position in Hyrule's map for the last 200 hours of gameplay:

{{< figure src="fig2.png" title="**Source: [polygon.com](https://www.polygon.com/zelda-breath-of-the-wild-guide-walkthrough/2017/7/2/15906402/heros-path-controls-how-to-use-pause-rewind-fast-forward-scrub-playback)**" lightbox="true" >}}

This feature was HUGE, not necessarily for knowing where I have been, but where I _haven't_ been, so that I could explore those never before seen areas (in hope of shrines or korok seeds). So then I thought back about the real world, and remembered Änggårdsbergen, a big nature reserve in Gothenburg (my hometown at the time), where even though I had been many times running, I knew that it had several sections I had not explored yet. Wouldn't be convenient that my Runkeeper app then showed me the overlay of all of my runs into a single map, so that I could find nice new areas with undiscovered ponds, peaks and views? And as in May 2019 Runkeeper did not provide that feature ~~and I was unemployed with lots of free time~~, I decided to create it myself.

## **Implementation**

The solution, using Python, was pretty simple. [Here](https://runkeeper.com/exportData) I downloaded each run I have ever gone for as a `.gpx` file, with my GPS location recorded every ~5 seconds. The very handy [gpxpy](https://github.com/tkrajina/gpxpy) package let me then parse these files into lists of longitude/latitude pairs:

```python
import gpxpy
gpx_file = open(<run_file.gpx>, 'r')
gpx = gpxpy.parse(gpx_file)

run_list = list()
for track in gpx.tracks:
  for segment in track.segments:
    for point in segment.points:
      run_list.append([point.longitude, point.latitude])
```

Then, using the [folium](https://python-visualization.github.io/folium/) package, which in turn calls the [Leaflet.js](https://leafletjs.com/) library for interactive maps, I easily created a map object:

```python
import folium
run_map = folium.Map(location=[<lat>, <lon>])  # lat/lon where I run most often
```

With both the run lists and the run map, I added each list to the map as a `GeoJson` object (as other object types could not render after adding around 70 to the same map):

```python
geojson = folium.GeoJson({'type': 'LineString', 'coordinates': run_list})
geojson.add_to(run_map)
```

The final step was to export the object to an `.html` map:

```python
run_map.save('./output-map.html')
```

That's it! I added some additional display settings, such as transparency to show overlapped runs, highlighting of any run you hover on, and a tooltip to display the date + type of activity (sometimes I use Runkeeper for tracking other activities such as hiking or biking).

## **End product**

The map for Änggårdsbergen below:

{{< figure src="fig3.png" title="**A zoom of my running world map into Änggårdsbergen, showing (still) many unexplored areas!**" lightbox="true" >}}

Knowing the areas I had not been to, I was then able to plan pre-run where would I go each time. As an added bonus, by zooming out enough I also got for free a world map with all places I've been running:

{{< figure src="fig4.png" title="**Full world map with all runs (note the tiny red spots)**" lightbox="true" >}}

However, the final challenge was that as new run logs would come in, I needed a way to keep the map updated. I'm a sucker for automation, so I added all `.gpx` files + scripts to [this](https://github.com/BenjaSanchez/map-runs) Github repo, and I set up [Travis CI](https://travis-ci.org/) to update the map every time I add new runs. Now the only thing I need to do every 3 months (when my [Trello](https://trello.com/) board reminds me) is to download all new `.gpx` files to the proper folder and commit + push the files to Github. Travis will then run the script to create the latest map and publish it [here](https://benjasanchez.github.io/map-runs/output-map.html).

## **Final Words**

_Could this tool be better?_ For sure. It could display extra information like total distance or some basic stats, but those are features that Runkeeper already provides. Additionally, the tool could be packaged as a full fledged app that also shows you your current position, to use in real time when exploring new areas. Alas, what I have for now is good enough for my purpose.

_Interested in any of this?_ I documented [here](https://benjasanchez.github.io/map-runs/) the instructions on how to implement it for your own runs. Feel free to comment below if you find the tool useful or if you have any feedback!

Ben

> _PS: Thanks to [@eHanseJoerg](https://github.com/eHanseJoerg) for [this](https://nbviewer.jupyter.org/github/eHanseJoerg/folium/blob/master/examples/Highlight_Function.ipynb) useful jupyter notebook explaining how to use the geoJSON format in folium._
