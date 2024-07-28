---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Reconstruction of a catalogue of genome-scale metabolic models with enzymatic constraints using GECKO 2.0"
authors:
- Iván Domenzain
- admin
- Mihail Anton
- Eduard J Kerkhoven
- Aarón Millán-Oropeza
- Céline Henry
- Verena Siewers
- John P Morrissey
- Nikolaus Sonnenschein
- Jens Nielsen
date: "2022-06-30"
doi: "10.1038/s41467-022-31421-1"

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

abstract: "This is the sequel of the [GECKO paper](https://www.benjasanchez.com/publication/2017/06/gecko/) that I developed in my PhD, for integration of proteomics data in GEMs. In this new paper, Iván, an extremely talented former colleague, took over the lead of the code development and elevated the GECKO tool to new heights. The main achievements were to make the tool compatible with any GEM reconstruction, and to develop a workflow where as GEMs get upgraded and curated, the enzyme-constrained counterparts (ecModels) get automatically updated, using a container called [ecModels](https://github.com/SysBioChalmers/ecModels) (see figure). This was implemented for 5 species: _Saccharomyces cerevisiae_, _Yarrowia lipolytica_, _Kluyveromyces marxianus_, _Escherichia coli_ and _Homo sapiens_. GECKO this way becomes an even more versatile tool for studying the interplay between enzymes and metabolic reactions within cells."

# Summary. An optional shortened abstract.
summary: "Streamlining generation of enzyme-constrained models using GECKO"

tags:
- yeast
- proteomics
- protein turnover
- GEMs
- tool
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://www.nature.com/articles/s41467-022-31421-1.pdf
url_code: https://github.com/SysBioChalmers/GECKO2_simulations
url_dataset: https://www.ebi.ac.uk/pride/archive/projects/PXD012836
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Workflow of automatic update of enzyme-constrained models. Taken from the original publication: https://doi.org/10.1038/s41467-022-31421-1"
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
