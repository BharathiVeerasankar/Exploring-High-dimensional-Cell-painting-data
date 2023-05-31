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





## 2. Yokogawa_10X_data 

### i. UMAP_&_tSNE_Yokogawa_10X
- there is a clear separate cluster for wells with high cell count in all 3 plots 
- There is no repetition perturbations used in high cell count cluster, the perturbations are: 
    * A12 quazinone 
    * A09 SGX523 
    * A11 DMSO 
    * A03 ML324 
    * A02 delta-Tocotrienol 
    * A04 KH-CB19 
    * A06 GDC-0879 
    * A08 SHP099 
    * A01 AZ191 
    * A07 filgitinib 
- all the wells which are present in this high cell count cluster are from row A 
- Perturbation AMG900 gives highest RNA intensity and all the wells with this perturbation cluster together 
- Lowest area is due to perturbation SCH-900776 and they cluster together in all 3 plots to an extend 
- Highest area is due to perturbation ponatinib, SU3327 and THZ1 , they all cluster together in all 3 plots to an extend 
- Lowest DNA granularity is due to perturbation with romidepsin, and they cluster together in all 3 plots 


## 3. Yokogawa_20X_5Ch

### i. UMAP_&_tSNE_Yokogawa_20X_5Ch_plate_b
- there is a clear separate cluster for wells with high cell count in all 3 plots 
- There is no repetition perturbations used in high cell count cluster, the perturbations are: 
    * A12 quazinone 
    * A09 SGX523 
    * A11 DMSO 
    * A03 ML324 
    * A02 delta-Tocotrienol 
    * A04 KH-CB19 
    * A06 GDC-0879 
    * A08 SHP099 
    * A01 AZ191 
    * A07 filgitinib 
- all the wells which are present in this high cell count cluster are from row A 
- Perturbation AMG900 gives highest RNA intensity and all the wells with this perturbation cluster together 
- Lowest area is due to perturbation SCH-900776 and they cluster together in all 3 plots to an extend 
- Highest area is due to perturbation ponatinib, SU3327 and THZ1 , they all cluster together in all 3 plots to an extend 
- Lowest DNA granularity is due to perturbation with romidepsin, and they cluster together in all 3 plots 

#### Same observations as seen in Yokogawa_10X 

### ii. UMAP_&_tSNE_Yokogawa_20X_5Ch_plate_2
- a distinct separate cluster seen in all 3 plots, with the following perturbations and wells: 
    - B09 SU3327
    - G24 SU3327
    - O23 SU3327 
    - P05 Compound 2 
    - H20 valrubicin 
    - I22 rheochrysidin 
    - H22 pomalidomide 
    - H24 GDC-0879 
    - P06 EPZ015666
    - E22 Compound 8 
    - H24 GDC-0879 
    - J24 CHIR-99021 
    - H23 AMG-925 
    - H21 halopemide 
    - D20 Compound 1 
    - G22 Compound 3 
    - K24 DMSO 
    - E23 AZD2014
    - J21 DMSO 
    - P24 Compound 6 
    - E24 sirolimus 
    - J23 IOX2 
    - D21 Compound 1 
    - G18 PFI-1 
    - A09 SGX523 
    - B11 rheochrysidin 
    - B12 GW-3965
    - M01 T-0901317
    - G19 carmustine 
    - G21 GW-3965
    - E21 PS178990 
    ![image](https://user-images.githubusercontent.com/127401579/233050514-85d3fc98-46f7-44d5-acf3-b00802cc70cf.png)
     All cells in this separated cluster seem to have very high DNA granularity 
- AMG900 has highest RNA intensity and clusters together 
- H04 ponatinib, P03 ispinesib has only 1 cell count


## 4. Yokogawa_20X_5Ch_12Z
- there is a prominent separate cluster in tSNE and UMAP, and a not so prominent separate cluster in UMAP, with the following wells and perturbations 
    - P05 compound 2 
    - H20 valrubicin 
    - B09 SU3327 
    - G24 SU3327 
    - P06 EPZ015666
    - J24 CHIR-99021 
    - H24 GDC-0879 
    - H22 pomalidomide 
    - H23 AMG-925 
    - O23 SU3327 
    - I22 rheochrysidin 
    - K24 DMSO 
    - H21 halopemide 
    - G22 compound 3 
    - G21 GW-3965
    - M01 T-0901317 
    - A10 AMG-925 
    - E21 PS178990 
    - P24 compound 6 
    - E22 compound 8 
    - D21 compound 1 
    - J21 DMSO 
    - J23 IOX2 
    - E24 sirolimus 
    - E23 AZD2014 
    - L02 PNU-74654
    - A09 SGX523 
    - B11 rheochrysidin 
    - G18 PFI-1 
    - D20 compound 1 
    - G19 carmustine 
    - B12 GW-3965
![image](https://user-images.githubusercontent.com/127401579/233058461-4e89079d-99fc-4609-b37f-1a5f211bd87a.png)
- AMG900 has highest RNA intensity and clusters together 

## 4. Yokogawa_20X_6Ch_plate1
- there is a separate cluster seen in tSNE and UMAP, with the following wells
    - G22 compound 3 
    - H21 halopemide 
    - G20 DMSO 
    - H23 AMG-925 
    - E24 sirolimus 
    - F24 DMSO 
    - G21 GW-3965 
    - A23 sirolimus 
    - E23 AZD2014 
    - A24 ponatinib 
    - D22 ABT-737 
    - D21 Compound 1 
    - D23 valrubicin 
    - B01 PFI-1 
    - E21 PS178990 
This cluster has low RNA intensity ( but not the lowest) 
![image](https://user-images.githubusercontent.com/127401579/233062186-8eb5abef-b899-44a6-bbdf-b2256e8e3229.png)

- perturbation APY0201 has highest RNA intensity 
- Ponatinib, PF-477736, SU3327, THZ1 perturbations give the lowest cell count and all form a cluster in tSNE and UMAP, are away from the main cluster in PCA 

## 5. Yokogawa_20X_6Ch_plate2
- there is a obvious separate cluster in all 3 plots, with the following wells and perturbation
    - B11 rheochrysidin 
    - B02 carmustine 
    - P22 delta-tocotrienol 
    - O22 NVP-AEW541 
    - D22 ABT-737 
    - O21 compound 3 
    - P23 SGX523 
    - J20 GSK-3-inhibitor-IX 
    - F24 DMSO 
    - H22 pomalidomide 
    - D21 compound 1 
    - K22 GW-3965 
    - G22 compound 3 
    - H21 halopemide 
    - I21 NVP-AEW541 
    - J22 T-0901317 
    - E22 compound 8 
    - G24 SU3327 
    - J19 filgotinib 
    - A10 AMG-925 
    - G19 carmustine 
    - G20 DMSO 
    - H19 dimethindene-(S)-(+) 
    - A09 SGX523 
    - P24 compound 6 
    - I20 VX-745 
    - 122 rheochrysidin 
    - A01 AZ191 
    - D23 valrubicin 
    - J21 DMSO 
    - H23 AMG-925 
    - H20 valrubicin 
    - I18 A-366 
    - E24 sirolimus 
    - E23 AZD2014 
![image](https://user-images.githubusercontent.com/127401579/233066132-fbd30d2e-6948-4393-a788-cefa00c527ea.png)
These wells have relatively low RNA intensity 
- BI78D3, Ponatinib, PF-477736, SU3327, THZ1, ispinesib perturbations give the lowest cell count and all form a cluster in tSNE and UMAP, are away from the main cluster in PCA 

## 6. Yokogawa 40X 
- no prominent separate cluster seen other than lowest cell count cluster 
- Perturbation AMG900 has highest RNA intensity and its wells cluster together 

## 7. Yokogawa 40X_plate2
 - There is a cluster in tSNE and UMAP containing following wells 
    - E21 PS178990 
    - G22 compound 3 
    - D21 compound 1 
    - H23 AMG-925 
    - D22 ABT-737 
    - G21 GW-3965 
    - H21 halopemide 
    - G24 SU3327 
    - E23 AZD2014 
    - B01 PFI-1 
    - F24 DMSO 
    - D23 valrubicin 
    - G20 DMSO 
    - B24 Andarine    

this cluster has low RNA intensity and low area shape 
![image](https://user-images.githubusercontent.com/127401579/233073448-94b35335-941f-46c8-a313-197c8ebffaf4.png)
- The highest RNA intensity is shown by wells with perturbation AMG900


    
    
    
  
  
  
