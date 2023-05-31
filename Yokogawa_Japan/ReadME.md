## Contents 
## 1. Yokogawa_Japan_20X Folder
#### This folder contains 4 replicates of Yokogawa 20X data

### i.   heatmap.ipnb 
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

## ii. zscore.ipynb 
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

### iii. PCA.ipynb 
* Principal Component Analysis technique was performed on the Jamali dataset using sklearn.decomposition.pca . 
* PCA with 3 principal components, 2 principal components and single principal component were plotted. 
* Percentage of variance explained by each of the selected components were calculated using explained_variance_ratio_, where the sum of ratios will be 1.0 
#### Inference 
* 22% of variance explained with PCA1 (40% with PCA1+PCA2)
* much of the data points lie along one line in PCA1 vs. PCA2 plane

### UMAP and TSne 
* UMAP and TSne techniques were perfomed on Jamali dataset using sklearn.manifold and umap.umap 
* PCA, UMAP and TSne plots were plotted side by side to compare each against each other. 
* These plots were plotted for the following features such as Cell count, RNA intensity, Area shape and DNA Granularity
* This was perfomed to the 4 replicate datas of Yokogawa japan 20x 


### iv. UMAP_&_tSNE-yokogawa_20X.ipynb
This is the PCA-TSne-UMAP plot marking cell-count. 
![image](https://user-images.githubusercontent.com/127401579/233843805-94c11794-c2c6-48e4-bc21-0792a40496bf.png)
The orange wells here represent the orange cluster present in TSne and UMAP and the blue wells represent the blue cluster in TSne and UMAP, and the blue points which are not in the main PCA cluster which represent low cell-count wells.

![image](https://user-images.githubusercontent.com/127401579/233844414-03a9dda4-e107-4d92-a178-cbea403f0781.png)

### v. UMAP_&_tSNE-yokogawa_20X-replicate1.ipynb
This is the PCA-TSne-UMAP plot marking cell-count. 
![image](https://user-images.githubusercontent.com/127401579/233843827-48d49fd6-06b2-457d-b245-e48e49254963.png)
The orange wells here represent the orange cluster present in TSne and UMAP and the blue wells represent the blue cluster in TSne and UMAP, and the blue points which are not in the main PCA cluster which represent low cell-count wells

![image](https://user-images.githubusercontent.com/127401579/233846708-449cf94e-c39e-417b-8e70-500f62ed9554.png)

### vi. UMAP_&_tSNE-yokogawa_20X-replicate2.ipynb
This is the PCA-TSne-UMAP plot marking cell-count.
![image](https://user-images.githubusercontent.com/127401579/233843853-507c899c-71af-4aea-97af-7cdb743eeaa9.png)
The orange wells here represent the orange cluster present in TSne and UMAP and the blue wells represent the blue cluster in TSne and UMAP, and the blue points which are not in the main PCA cluster which represent low cell-count wells

![image](https://user-images.githubusercontent.com/127401579/233847245-7c88e0b8-c85b-486a-aeeb-d0cc0a7a0025.png)

### vii. UMAP_&_tSNE-yokogawa_20X-replicate3.ipynb
This is the PCA-TSne-UMAP plot marking cell-count.
![image](https://user-images.githubusercontent.com/127401579/233843864-62be1ce6-288b-40b8-99da-fb3f8fd74e29.png)
The orange wells here represent the orange cluster present in TSne and UMAP and the blue wells represent the blue cluster in TSne and UMAP, and the blue points which are not in the main PCA cluster which represent low cell-count wells

![image](https://user-images.githubusercontent.com/127401579/233850788-b042176b-1a4d-4964-8e13-00472a35ee1c.png)

#### Inference 
* All the replicate plates seem to replicate the results got in each other 
* There is a ambiguous orange cluster in TSne and UMAP which is not present in PCA

