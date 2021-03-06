GT Plotting
================

<!-- badges: start -->

<!-- badges: end -->

Functions for plotting the genotypes from a vcf file.

## Installation

You can install the released version of SorghumTestingData from Github
with:

``` r
devtools::install_github("AnzaGhaffar/GT-Plotting")
install.packages("GTPlotting")
library(GTPlotting)
```

## Functions

We will have access to three functions:

## VcfToTable

``` r
vcf_testdata<-VcfToTable('vcffilename')
```

This function takes as input a vcf file with extension vcf or vcf.gz and
creates an object which consists of 2 data frames

``` r
vcf_testdata$vcfdata
```

The vcfdata is the data frame which has the important features extracted
from the vcf file for the genotype plotting

``` r
vcf_testdata$chromlen
```

This data frame has the chromosome names and the size of each
chromosome.

## GTPlotting\_Chromosome

``` r
GTPlotting_Chromosome(vcf_testdata$vcfdata,vcf_testdata$chromlen,'Grinkan_CTRL')
```

This function plots the genotype of each chromosome, it takes three
inputs the vcf data frame generated by the VcfToTable function, the
chromosome length table generated by the VcfToTable function and the
name of the control sample should be same as in the vcf file.

## GTPlotting\_Chromosome\_Combined

``` r
GTPlotting_Chromosome_Combined(vcf_testdata$vcfdata,vcf_testdata$chromlen)
```

This function plots the genotype of all the chromosomes, it takes two
inputs the vcf data frame generated by the VcfToTable function, the
chromosome length table generated by the VcfToTable function.
