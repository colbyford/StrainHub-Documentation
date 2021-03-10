# Installing the R Package

If you want to install the standalone R package locally, you can do so by running the following command:

```r
devtools::install_github("colbyford/strainhub", subdir="pkg")
```

{% hint style="info" %}
**Note:** If you have issues getting the StrainHub R package to install, this may be due to the fact that the package has quite a few dependencies. You can manually ensure that all the dependencies are installed by running the following script first:

```r
packages <- c("ade4",
              "adegenet",
              "ape",
              "castor",
              "colourpicker",
              "data.table",
              "dplyr",
              "DT",
              "geosphere",
              "ggplot2",
              "ggtree",
              "ggtree",
              "globe4r",
              "hashmap",
              "htmltools",
              "htmlwidgets",
              "igraph",
              "import",
              "knitr",
              "leaflet",
              "magrittr",
              "markdown",
              "network",
              "phangorn",
              "plotly",
              "plyr",
              "randomcoloR",
              "rbokeh",
              "readr",
              "rhandsontable",
              "rmarkdown",
              "shiny",
              "shinycssloaders",
              "shinyjqui",
              "shinythemes",
              "shinyWidgets",
              "stringr",
              "tibble",
              "treeio",
              "visNetwork",
              "webshot")

if (length(setdiff(packages, rownames(installed.packages()))) > 0) {
  install.packages(setdiff(packages, rownames(installed.packages())))  
}
```
{% endhint %}

