# Comparing 10x Visium spatial transcriptomic technologies with SpatialBench

This repository contains code used to perform analysis and figures featured in our paper:

[**Comparing 10x Visium spatial transcriptomic technologies with SpatialBench**](https://www.biorxiv.org/content/10.1101/2024.03.13.584910v1) 

Mei R. M. Du, Changqing Wang, Charity W. Law, Daniela Amann-Zalcenstein, Casey J. A. Anttila, Ling Ling,
Peter F. Hickey, Callum J. Sargeant, Yunshun Chen, Lisa J. Ioannidis, Pradeep Rajasekhar, Raymond Yip, Kelly
L. Rogers, Diana S. Hansen, Rory Bowden, and Matthew E. Ritchie

![Visium data generation and analysis workflow](https://github.com/mritchielab/SpatialBench/blob/main/Visium%20workflow.png) 
Figure created with [BioRender](https://biorender.com).



## Data Availability
Our Visium and 10x scRNA-seq datasets are available from GEO under accession number GSE254652.

Please cite our paper if you use our data and/or scripts in your studies.

## Index

Download analysis folder and open index.html to view scripts as a website.

### Quality control

Spatial (example samples): EDA_709_FFPE_CA.Rmd, EDA_713_FFPE_CA.Rmd
scRNA-seq: sc_preprocessing.Rmd

### Downstream analysis

FFPE CA multi-sample: FFPE_CA_multi-sample.Rmd
Pseudo-bulk differential expression analysis: as [targets](https://docs.ropensci.org/targets/) project under the `targets_project` folder

#### Running targets

Before running the targets project, you will need to replace the `targets_project/data/SpaceRanger` symlink with the appropriate path to the SpaceRanger output folder, and update the `targets_project/data/sample_ids.tsv` file's folder field. 

### Figures

Figure 1c-e: figures.R

Figure 2: compile script

Figure 3: compile script

Figure 4 & 5, Supplementary figures S8-S11: run `targets::tar_make()` in the `targets_project` folder, figures are saved to `targets_project/output`

Supplementary figures: compile script
