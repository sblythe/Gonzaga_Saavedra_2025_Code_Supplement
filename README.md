# Gonzaga_Saavedra_2025_Code_Supplement
Data and code for reproducing differential enrichment analysis and general surveying of ChIP-seq experiments to determine the effect of GAGA-factor and Zelda on the establishment of H3K27me3 modifications at Drosophila ZGA.

## Overview

This repository has two versions of an R markdown (.Rmd and knit .html) that will reproduce the calculations and differential enrichment analysis presented in the Gonzaga-Saavedra manuscript. The markdown is identical to the one published as supplemental data in the original manuscript. 

To facilitate the standalone reproduction of the analysis, the repository has a Data directory that contains the necessary files for running the markdown as-is. These are .RDS formatted versions of peaks lists that were also submitted to GEO for the associated manuscript. Additionally, we have provided counts tables for the GAF knockdown and zelda mutant ChIP seq experiments (conducted by counting overlaps in the original mapped .bam files over a set of 2 kb bins spanning the Drosophila genome (dm6)).

## Use

Following cloning of this repository, open the .Rmd file, change the line `d = ~/Dropbox/Blythe Lab...` to reflect the file path to the cloned `Data` directory, and the code should run, provided you also have all the necessary R libraries. 

## Necessary R Libraries

GenomicRanges

tidyverse

DESeq2

BSgenome.Dmelanogaster.UCSC.dm6

Rsamtools

GenomicAlignments

The knit markdown (.html) concludes with a call to `sessionInfo()` that can be consulted if a library has been overlooked in this list.  
