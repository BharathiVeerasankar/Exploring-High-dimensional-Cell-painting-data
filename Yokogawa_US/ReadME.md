# Contents
## 1. Yokogawa_US_10X_data 

### i. UMAP_&_tSNE_Yokogawa_10X
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/ae8f0904-3560-4939-a174-2a7015d966ff)

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


## 2. Yokogawa_US_20X_5Ch

### i. UMAP_&_tSNE_Yokogawa_20X_5Ch_plate_b
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/e9335638-37a9-4de3-a432-5e22934948a0)

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
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/347da21c-cf76-4b92-9ae2-41bcb5d8e559)

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


## 3. Yokogawa_US_20X_5Ch_12Z
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/5d04ee78-246c-47bf-9e79-d1697fc2303d)

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

## 4. Yokogawa_US_20X_6Ch_plate1
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/72cb1aa2-4855-4dbc-838d-b8e818630f0c)

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

## 5. Yokogawa_US_20X_6Ch_plate2
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/662c83c7-860c-4c4e-a738-bdf639f8df74)

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


## 6. Yokogawa_US_40X
![image](https://github.com/BharathiVeerasankar/Exploring-High-dimensional-Cell-painting-data/assets/127401579/f6877e27-3687-4a52-8b68-a737dadd8f46)

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
