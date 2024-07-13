---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Combining mechanistic and machine learning models for predictive engineering and optimization of tryptophan metabolism"
authors:
- Jie Zhang
- Søren D. Petersen
- Tijana Radivojevic
- Andrés Ramirez
- Andrés Pérez-Manríquez
- Eduardo Abeliuk
- admin
- Zak Costello
- Yu Chen
- Michael J. Fero
- Hector Garcia Martin
- Jens Nielsen
- Jay D. Keasling
- Michael K. Jensen
date: "2020-09-25"
doi: "10.1038/s41467-020-17910-1"

# Schedule page publish date (NOT publication's date).
# publishDate: {{ .Date }}

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Nature Communications"
publication_short: ""

abstract: "Machine learning is becoming more and more popular for screening for targets, as it can decrease the number of combinations to be studied. Here we combined in a two-step approach mechanistic and machine learning models to increase tryptophan production in yeast, as a proof of concept. In the first step we used genome-scale modeling to pinpoint the genes to focus on, and in the second step we used machine learning for predicting the most promising promoters for said genes, using fluorescent data from a tryptophan biosensor. I was in charge of the genome-scale modeling step of the approach, which was the same as the method introduced in a [previous](https://www.benjasanchez.com/publication/2019/10/fine-tuning) publication. Running this approach gave us a strain that increased tryptophan titer and productivity by up to 74% and 43%, respectively, so it presents as a promising tool for metabolic engineering."

# Summary. An optional shortened abstract.
summary: "Over-producing tryptophan using a combination of machine learning and flux balance analysis"

tags:
- GEMs
- metabolic-engineering
- machine-learning
- yeast
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://www.nature.com/articles/s41467-020-17910-1.pdf
url_code: https://github.com/biosustain/trp-scores
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Connectivity network of all reactions in the yeast model. Taken from the original publication: https://doi.org/10.1038/s41467-020-17910-1"
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
