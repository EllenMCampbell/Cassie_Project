Baseline\_Data
================

-   [Goal](#goal)
-   [Data](#data)
    -   [Reading Data In](#reading-data-in)

Goal
----

Learn how to manipulate data in the *tidyverse*, keep data organized and [pretty](https://en.wikipedia.org/wiki/Pretty_Things), and **reproducible**. I also want to learn how to make awesome graphs and maps from the data I have tidied in **R**.

Data
----

The data files for this project are in the './data' directory. We have two files that Anthony shared which are from the chinook baseline project.

-   First file contains samples (fish) and the metadata that is connected to the sample ID of those fish.
    -   Important variables are the NMFS ID, analysisID, sampleID (which may not be unique); location data and length if we are interested in that down the road.
    -   This file *might* have duplicate samples that were extracted more than once?
-   Second file has the genotype data for the fish.
    -   Looks like the "analysisID" is the link between the two files and they should be unique identifers.
    -   This file is in two column format, so we will probably have to play around with the formatting quite a bit before analyzing the data
    -   This file also contains the assignment locations of these fish based on the genotype data

### Reading Data In

#### Metadata

``` r
metadata <- read.csv("data/baseline_metadata.csv")
```

#### Genotypes

``` r
genotypes <- read.csv("data/baseline_genotypes.csv")
```
