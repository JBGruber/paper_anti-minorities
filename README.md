[![DOI](https://img.shields.io/badge/DOI-10.31219%2Fosf.io%2Fdyuwa-38bbf1?logo=osf&logoColor=38bbf1)](https://doi.org/10.31219/osf.io/dyuwa)

# Weaponizing rights: Political Uses of LGBTQ+ Rhetoric in Media Outlets

Authors: *Johannes B. Gruber, Alberto López Ortega Mariken A.C.G. van der Velden[^1]*

This is the code to reproduce the numbers, figures and analyses for the chapter *Weaponizing rights: Political Uses of LGBTQ+ Rhetoric in Media Outlets*. Preprint: <https://doi.org/10.31219/osf.io/dyuwa>

The main analysis is done with [`rollama`](https://jbgruber.github.io/rollama/index.html), which requires the software [Ollama](https://ollama.com/) to run the utilised model.

All other dependencies can be installed with:

```r
if (!requireNamespace("rlang", quietly = TRUE)) install.packages("rlang", dependencies = TRUE)
rlang::check_installed("attachment")
rlang::check_installed(attachment::att_from_qmds(path = ".", recursive = TRUE))
```

The Quarto (.qmd) files 1-4 contain all code and some explanations. To reproduce everything, simply run:

```r
rlang::check_installed("quarto")
for (file in list.files(pattern = ".qmd")) {
  quarto::quarto_render(file)
}
```

If something does not work, look at the end of the rendered versions of the notebooks (.html files) for the specific versions of the packages utilized here.

[^1]: The order of authorship for this chapter reflects equal contributions from all authors. The names are listed alphabetically to emphasize this shared effort.
