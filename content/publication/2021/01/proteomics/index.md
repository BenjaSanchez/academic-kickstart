---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Benchmarking accuracy and precision of intensity-based absolute quantification of protein abundances in Saccharomyces cerevisiae"
authors:
- admin
- Petri-Jaan Lahtvee
- Kate Campbell
- Sergo Kasvandik
- Rosemary Yu
- Iván Domenzain
- Aleksej Zelezniak
- Jens Nielsen
date: "2021-01-16"
doi: "10.1002/pmic.202000093"

# Schedule page publish date (NOT publication's date).
# publishDate: {{ .Date }}

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Proteomics"
publication_short: ""

abstract: "This was a side project in my PhD, as I needed to measure the exact amount of protein copy number inside a cell for combining it with my simulations, so I generated a dataset using label-free mass spectrometry proteomics. However, I saw that the technique had really poor technical reproducibility, i.e. it did not deliver consistent results when the same sample would be measured repeatedly. Therefore, we decided to perform a dedicated study of accuracy and precision of this technique by measuring proteomics data for yeast with both biological and inter-batch technical triplicates. We also analyzed how do the results vary when applying different methods for converting the raw data. Surprisingly, we demonstrated that a simple normalization and rescaling can perform as accurately, yet more precisely, than "state of the art" methods that rely on expensive external standards, meaning that for achieving best results, it's better not to use any external standard, and apply the suggested conversion instead. Additionally, we showed that inter-batch reproducibility is worse than biological reproducibility regardless of the method used, which is evidence of the current limitations of this technique. Even though the findings were quite controversial, I'm very happy we published this story, and even more so that we did it in a fully reproducible way, with all supplementary material being a rendered R markdown file."

# Summary. An optional shortened abstract.
summary: "How reproducible is the absolute quantification of protein levels?"

tags:
- yeast
- proteomics
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://analyticalsciencejournals.onlinelibrary.wiley.com/doi/epdf/10.1002/pmic.202000093
url_code: https://github.com/SysBioChalmers/reproduce
url_dataset: https://proteomecentral.proteomexchange.org/cgi/GetDataset?ID=PXD011725
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Variability across different batch runs of the mass spectrometer. Taken from the original publication: https://doi.org/10.1002/pmic.202000093"
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
