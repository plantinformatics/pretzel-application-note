# pretzel-application-note
A repository for an application note about [pretzel](https://github.com/plantinformatics/pretzel).

# Source

Application note is drafted in [RMarkdown](https://rmarkdown.rstudio.com/) in [`pretzel.Rmd`](pretzel.Rmd) file. RMarkdown is well intergrated in RStudio, but if you'd rather write/edit in a text editor of your choice, you can render it as per instructions below.

## Bibliography

Among the [alternatives available](https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html#specifying_a_bibliography) we opted for BibTeX, see [`references.bib`](references.bib).


# Rendering

### Using docker

```sh
docker run --rm --user $(id -u):$(id -g) \
  --volume $(pwd):/writing \
  --workdir /writing rsuchecki/renderer:0.1 ./render.R
```

### Using singularity

Note that this is rather slow, possibly due to container conversion from docker to singularity format.

```sh
singularity exec docker://rsuchecki/renderer:0.1 ./render.R
```

### Natively

If you'd like to render the manuscript without docker/singularity, you will need the following:

* `R` e.g. on ubuntu `sudo apt apt install r-base-core`
* `pandoc` e.g. on ubuntu `sudo apt install pandoc pandoc-citeproc`
* `LaTeX` e.g. on ubuntu `sudo apt install texlive texlive-latex-extra`
* `R` packages:
  * `rmarkdown`
  * `rticles`
  * `bookdown`

Then:

```
./render.R
```




