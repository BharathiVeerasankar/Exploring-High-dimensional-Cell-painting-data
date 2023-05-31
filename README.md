# Exploring-High-dimensional-Cell-painting-data

## Objective 
To learn techniques in exploratory data analysis using an existing data set from Cell Painting

## Introduction

## CellProfiler 
### What is CellProfiler?
- a free, open-source software program for image analysis
- [CellProfiler](https://cellprofiler.org) helps scientists to
    -  identify 
    - measure biological entities
    - process images ( at any scale) - from a small scale experiment to a large one 
    - export data for further analysis.
### How it works ?
1. Load an example pipeline : a series of image processing modules
2. Adjust settings : to identify and measure the objects of interest 
3. Accomplish a workflow which fits your image 
4. After preprocessing image, identify the regions 
5. Process Images automatically
6. Export your data to a spreadsheet or database
7. Explore your data and classify phenotypes using machine learning, eg. CellProfiller Analyst 

## Cell Painting 

### What is cell painting ?
It is a high-content image-based assay for morphological profiling using multiplexed fluorescent dyes.
- cell painting, which is a morphological profiling assay that multiplexes six fluorescent dyes, imaged in five channels, to reveal eight broadly relevant cellular components or organelles. 
- cells are plated in multiwell plates, perturbed with the treatments to be tested, stained, fixed, and imaged on a high-throughput microscope. next, an automated image analysis software identifies individual cells and measures ~1,500 morphological features (various measures of size, shape, texture, intensity, and so on) to produce a rich profile that is suitable for the detection of subtle phenotypes 
- profiles of cell populations treated with different experimental perturbations can be compared to suit many goals, such as identifying the phenotypic impact of chemical or genetic perturbations, grouping compounds and/or genes into functional pathways, and identifying signatures of disease. 

### How to do cell painting ? For what type of cells can we do cell painting?
- The technique enables single-cell resolution, allowing detection of perturbations even in subsets of cells.
- The Cell Painting assay could also be adapted for living cells, imaged over time, by using an alternative set of live cell–compatible stains or cells expressing fluorescently tagged proteins. 
- successfully applied the Cell Painting assay to 13 different cell cultures, including cell lines, primary cells, and coculture systems. 
- A major criterion in choosing a cell line is that a seeding density can be identified at which individual cells do not substantially or frequently overlap each other in the final images—i.e., the cells form a monolayer. 
- A second major criterion is that the cell type should grow in a manner conducive to fluorescence imaging and analysis. 
- Specifically, the cells should typically be adherent and grow reasonably flat (i.e., nonspheroid), without substantial clumping, under the culture conditions used 
-  The more rounded a cell type is, or the more cells grow on top of each other, the less internal structure is clearly visible by microscopy. In such cases, the staining protocol itself will label the appropriate components, and images can be produced and processed, but the information content is likely to be reduced for cell types with a rounded morphology as compared with a more flattened one. 

### How is it better than other methods ?
- gene-expression profiling in high throughput can be currently performed only by aggregating cell populations and not at the single-cell level, 
- whereas morphological profiles are obtained at the level of individual cells, which potentially improves the ability to resolve changes in subpopulations of cells. 
- Cell Painting also costs substantially less per sample. 
- better predictive power for Cell Painting versus L1000 gene expression profiling, 

### What are its disadvantages ?
- Although the Cell Painting assay is intended to be unbiased with regard to the cell type chosen, certain biological processes may simply not yield any relevant discernible morphological phenotypes, given the experimental conditions used (stains, cell type, time point, and so on) 
- In this case, augmenting the image-based profiles with additional or orthogonal assays may reveal additional biological effects that would be otherwise missed. 
- here are several computational challenges that are associated with this assay. 
- First, there are statistical challenges associated with analyzing the high-dimensional feature space that results from Cell Painting. 
- curse of dimensionality’, 
- model overfitting, 
- spurious correlations, 
- and multiple testing complicate the data analysis of this assay 
### What type of data do we get out of it ?
After running the profiling scripts to normalize the image features across plates and to create the per-well profiles, the output will be a morphological profile file in CSV format. Each row of this file represents a data vector for an individual plate and well, with each column containing the median for each of the ~1,500 image features across all the cells in that well. 

### REFERENCES 
#### Cell Profiler
* watch: [digest video](https://www.youtube.com/watch?v=waJXi6z6bwA&list=PLXSm9cHbSZBBy7JkChB32_e3lURUcT3RL)
* watch: [tutorial](http://-%20https/www.youtube.com/watch?v=eriZdORpFxs)

#### Cell Painting
* read: [Bray et al. (2016) Nature Protocols](https://www.nature.com/articles/nprot.2016.105)
* watch: [Cell Painting basics](https://www.biorxiv.org/content/10.1101/2022.07.13.499171v2)
* watch: [Cell Painting applications](https://www.youtube.com/watch?v=UfB1rzXcc-A) 

#### Cell Painting + JUMP-MOA
* read: [JUMP consortium Cimini et al. (2022)](https://www.biorxiv.org/content/10.1101/2022.07.13.499171v2) 

## Contents 
### (i) PCA_iris_example 
* Replicated PCA using scikit Python from [Builtin Tutorial](https://builtin.com/machine-learning/pca-in-python)

### (ii) Yokogawa_Japan 
* Contains codes plotting heatmaps, PCA, UMAP and Tsne and analysis of cell painting data got from [Jamali et al](https://www.biorxiv.org/content/10.1101/2023.02.15.528711v1)
* Contains 2 subfolders containing replicates of 20X data and 40X data and their analysis

### (iii) Yokogawa_US 
* Contains codes plotting heatmaps, PCA, UMAP and Tsne and analysis of cell painting data got from [Jamali et al](https://www.biorxiv.org/content/10.1101/2023.02.15.528711v1) 
* Contains 6 subfolders containing different plates and their analysis 

### (iv) UMAP&TSne_example.ipynb
* Replicated UMAP and TSne plots using sklearn Python from [Towardsdatascience Tutorial](https://towardsdatascience.com/umap-variance-explained-b0eacb5b0801)








    
    
    
  
  
  
