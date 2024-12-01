# Weaponizing rights: Political Uses of LGBTQ+ Rhetoric in Media Outlets

Authors: *Alberto López Ortega, Johannes Gruber, Mariken A.C.G. van der Velden*

This is the code to reproduce the numbers, figures and analyses for the chapter *Weaponizing rights: Political Uses of LGBTQ+ Rhetoric in Media Outlets*.

The main analysis is done with [`rollama`](https://jbgruber.github.io/rollama/index.html), which requires the software [Ollama](https://ollama.com/) to run the utiliyed model.

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
