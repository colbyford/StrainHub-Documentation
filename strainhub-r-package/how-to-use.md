# How to Use

## Getting Started

First, you'll need to read in the tree file, metadata, and location geodata \(optional\).

```r
## Load in StrainHub
library(strainhub)

## Read in tree, metadata, and geodata
treedata <- ape::read.tree("../../data/parsimonious/chikv/chikv_westernafrica.phy")
metadata <- readr::read_csv("../../data/parsimonious/chikv/chikv_westernafrica_metadata.csv", col_names = TRUE)
geodata <- readr::read_csv("../../data/parsimonious/chikv/chikv_geo.csv", col_names = TRUE)
```

{% hint style="info" %}
**Note:** Example data files are available [here](https://github.com/colbyford/StrainHub/tree/master/data).
{% endhint %}

Next, you can list the states that are available in your metadata.

```r
## Check to See Which States are available by which to generate the network
listStates(treedata,
           metadata,
           treeType = "parsimonious")
```

Then, make the transmission network by calling the `makeTransNet` function.

```r
## Make the Transmission Network
graph <- makeTransNet(treedata,
                      metadata,
                      columnSelection = "Country",
                      centralityMetric = 6,
                      treeType = "parsimonious")
                      
print(graph)
```

Finally, render a map that has the overlay of the generated transmission network.

```r
## Make Leaflet/Swoopy map
make_map(graph,
         geodata = geodata,
         columnSelection = "Country")
```

