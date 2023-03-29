# Exploring-High-dimensional-Cell-painting-data

## Objective 
To learn techniques in exploratory data analysis using an existing data set from Cell Painting

## Introduction

## Cell profiler 
### What is cell profiler?
- a free, open-source software program for image analysis
- CellProfiler helps scientists to
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


## Contents 
### 1. data_Jamali2023 Folder
  Contains all the source data files from

### 2.   heatmap.ipnb 
#### Heat maps of cell number per well in a "plate view" were created 
- 384 well = 16 rows x 24 columns
    
#### Contains following heat maps 
-  Cell count per well : Metadata_Count_Cells
- Cell area in well : Cells_AreaShape_Area
- Intensity of RNA in cell : Cells_Intensity_IntegratedIntensityEdge_RNA

#### Inference 
* A well number J03 had a very high intensity of RNA, it was perturbated with romidepsin which is a HDAC inhibitor \
* The histone deacetylase inhibitors (HDAC) are a new class of cytostatic agents that inhibit the proliferation of tumor cells in culture and in vivo by inducing cell cycle arrest, differentiation and/or apoptosis.
* Romidepsin is known to inhibit RNA splicing, so it makes RNA intensity high in the well 

### 3. zscore.ipynb 
* zscore normalisation of 1.csv data was done, and it was compared with normalisation.csv data to see if in the data they have indeed used zscore normalisation technique to normalise the data. 
* #### zscore normalized value = (x – μ) / σ
    * where:
        * x: Original value
        * μ: Mean of data
        * σ: Standard deviation of data
* #### scipy.stats.zscore(arr, axis=0, ddof=0) function was used for the same
    * function computes the relative Z-score of the input data, relative to the sample mean and standard deviation.
    * #### Parameters :
        * arr : [array_like] Input array or object for which Z-score is to be calculated.
        * axis : Axis along which the mean is to be computed. By default axis = 0.
        * ddof : Degree of freedom correction for Standard Deviation.
        * Results : Z-score of the input data.

### 4. PCA.ipynb 
* Principal Component Analysis technique was performed on the Jamali dataset using sklearn.decomposition.pca . 
* PCA with 3 principal components, 2 principal components and single principal component were plotted. 
* Percentage of variance explained by each of the selected components were calculated using explained_variance_ratio_, where the sum of ratios will be 1.0 
#### Inference 
* 22% of variance explained with PCA1 (40% with PCA1+PCA2)
* much of the data points lie along one line in PCA1 vs. PCA2 plane



    



    
    
    
  
  
  
