This repository contains code used to perform analysis and figures featured SpatialBench project.

# SpatialBenchVisium
[**Spotlight on 10x Visium: a multi-sample protocol comparison of spatial technologies**](https://www.biorxiv.org/content/10.1101/2024.03.13.584910v1) 

Mei R. M. Du, Changqing Wang, Charity W. Law, Daniela Amann-Zalcenstein, Casey J. A. Anttila, Ling Ling,
Peter F. Hickey, Callum J. Sargeant, Yunshun Chen, Lisa J. Ioannidis, Pradeep Rajasekhar, Raymond Yip, Kelly
L. Rogers, Diana S. Hansen, Rory Bowden, and Matthew E. Ritchie

![Visium data generation and analysis workflow](https://github.com/mritchielab/SpatialBench/blob/main/Visium%20workflow.png) 
Figure created with [BioRender](https://biorender.com).

## Data Availability

Our processed Visium and 10x scRNA-seq datasets, along with the code are available from zenodo: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.12788291.svg)](https://doi.org/10.5281/zenodo.12788291), data is also accessible through GEO: [GSE254652](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE254652).

Please cite our paper if you use our data and/or scripts in your studies.

## Index

Code to produce the reports are stored as Rmarkdown documents in `analysis`. Objects are saved in `output`.

### Pre-processing

#### Spatial
Sample 709 FFPE CA: `analysis/EDA_709_FFPE_CA.Rmd`

Sample 713 FFPE CA: `analysis/EDA_713_FFPE_CA.Rmd`

#### scRNA-seq
`analysis/sc_preprocessing.Rmd`

### Downstream analysis

Multi-sample feature selection, clustering, cell type deconvolution: `analysis/FFPE_CA_multi-sample.Rmd`

Pseudo-bulk differential expression analysis: as [targets](https://docs.ropensci.org/targets/) project under the `targets_project` folder

#### Running targets

Simply navigate to the `targets_project` folder from the zenodo tarball `SpatialBenchVisium.tar.gz` and run `targets::tar_make()` to run the entire pipeline, outputs are saved in the `targets_project/output` folder.

### Figures

Figures 1-3, Supplementary figures S2-S7: `analysis/figures.R`

Figure 4 & 5, Supplementary figures S8-S11: run `targets::tar_make()` in the `targets_project` folder, figures are saved to `targets_project/output`

# Future datasets

More datasets will be added to our benchmarking study and will be accessible through this repository, stay tuned!
