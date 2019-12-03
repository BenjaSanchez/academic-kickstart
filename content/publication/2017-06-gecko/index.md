---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Improving the phenotype predictions of a yeast genome-scale metabolic model by incorporating enzymatic constraints"
authors:
- admin
- Cheng Zhang
- Avlant Nilsson
- Petri-Jaan Lahtvee
- Eduard J Kerkhoven
- Jens Nielsen
date: "2017-06-19"
doi: "10.15252/msb.20167411"

# Schedule page publish date (NOT publication's date).
# publishDate: {{ .Date }}

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Molecular Systems Biology"
publication_short: ""

abstract: "A common problem when simulating metabolism with constraint-based modeling is that the user has to define _a priori_ the limitations of consumption, production and/or growth, as otherwise there are no internal constraints in the model that represent a biologically meaningful maximum capacity. This paper introduced GECKO, my flagship project throughout my PhD. GECKO is a computational tool that connects in a straightforward way metabolic fluxes to enzyme levels, imposing intrinsic limitations in metabolism due to the limited intracellular space for enzymes. We tested this approach for _S. cerevisiae_, creating a so-called 'enzyme-constrained model' (ecModel) of yeast, and with it we showed that without including any additional constraints we were able to correctly predict cell phisiology under a number of experimental conditions, provide insight into enzyme usage across metabolism, and significantly reduce the inherent variability of flux predictions."

# Summary. An optional shortened abstract.
summary: "A simple computational framework for connecting metabolism and enzyme levels"

tags:
- GEMs
- proteomics
- yeast
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://www.embopress.org/doi/epdf/10.15252/msb.20167411
url_code: https://github.com/SysBioChalmers/GECKO
url_dataset: https://www.ebi.ac.uk/pride/archive/projects/PXD005041
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Overview of the GECKO method and its applications. Taken from the original publication: https://www.doi.org/10.15252/msb.20167411"
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
