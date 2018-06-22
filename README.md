# pretzel-application-note
A repository for an application note about [pretzel](https://github.com/plantinformatics/pretzel).

# Source

Application note is drafted in [RMarkdown](https://rmarkdown.rstudio.com/) in [pretzel.Rmd](pretzel.Rmd) file. RMarkdown is well intergrated in RStudio, but if you'd rather write/edit in a text editor of your choice, here is all that should be required to render the manuscript.

# Rendering dependencies

* `R` e.g. on ubuntu `sudo apt apt install r-base-core`
* `pandoc` e.g. on ubuntu `sudo apt install pandoc pandoc-citeproc`
* `LaTeX` e.g. on ubuntu `sudo apt install texlive texlive-latex-extra`
* additional R packages installed and loaded by [render.R](render.R)

# Rendering

```
./render.R
```


