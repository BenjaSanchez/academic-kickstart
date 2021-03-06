---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Construction of robust dynamic genome-scale metabolic model structures of Saccharomyces cerevisiae through iterative re-parameterization"
authors:
- admin
- José R. Pérez-Correa
- Eduardo Agosin
date: "2014-07-19"
doi: "10.1016/j.ymben.2014.07.004"

# Schedule page publish date (NOT publication's date).
# publishDate: {{ .Date }}

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Metabolic Engineering"
publication_short: ""

abstract: "This was the publication that came out of my master thesis, and my first ever published paper. In it we present an algorithm for finding the best combination of kinetic parameters in a dynamic flux balance analysis (dFBA) model, and its implementation for _S. cerevisiae_ (RY-dFBA). We show that by following the algorithm we can get simple models (with only 5-6 parameters to estimate) that are easy to tune and predict well across different experimental conditions. We also show that consumption/production kinetics are the most relevant parameters to look into when calibrating these models."

# Summary. An optional shortened abstract.
summary: "An algorithm for improving dFBA predictions and its implementation in yeast."

tags:
- GEMs
- kinetics
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

url_pdf:
url_code: https://github.com/BenjaSanchez/RY-dFBA
url_dataset: https://github.com/BenjaSanchez/RY-dFBA/blob/master/main/data/DATA.xls
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Iterative reparameterization algorithm of kinetic parameters. Adapted from the original publication: https://www.doi.org/10.1016/j.ymben.2014.07.004"
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
