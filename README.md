# dianaveronez.github.io
# Diana_CLIM680_project

#  Relationship between ENSO and Precipitation

## Introduction
Precipitation is a critical component of the Earth's hydrological cycle, influencing water resources, agricultural productivity, and the frequency and intensity of extreme weather events. Understanding precipitation patterns is essential for managing water resources, predicting flood risks, and mitigating the effects of climate change (Smith et al., 2020).

One key factor influencing global precipitation variability is the El Niño-Southern Oscillation (ENSO). ENSO is a coupled ocean-atmosphere phenomenon that drives periodic changes in sea surface temperatures in the tropical Pacific Ocean, significantly affecting global climate systems. During El Niño events, shifts in atmospheric circulation alter rainfall patterns, leading to increased flooding in some regions and droughts in others (Trenberth et al., 2007). Conversely, La Niña events often cause contrasting precipitation anomalies, amplifying the complexity of hydrological responses worldwide (McPhaden et al., 2021).

In the context of Arlington County, Virginia, understanding the interplay between precipitation and ENSO is particularly vital for assessing flood risks. With its urbanized landscape and proximity to water bodies, Arlington is highly susceptible to flooding, especially during extreme precipitation events exacerbated by ENSO-related climate variability. Developing a nuanced understanding of these dynamics can enhance flood risk management, improve urban planning, and foster community resilience (County Climate Action Team, 2023).

## Data
> Nino 3.4 index
The Nino3.4 index can be obtained from the NOAA Physical Sciences Laboratory’s “Climate Indices: Monthly Atmospheric and Ocean Time Series” pages.
The index called Nino3.4 is used to quantify the El Niño–Southern Oscillation (ENSO). When the index is significantly positive, it indicates an El Niño event. Conversely, when the index is significantly negative, it reflects a La Niña event. Values near zero are considered neutral conditions.
The Nino3.4 index is derived from sea surface temperature (SST) anomalies in a specific region of the Tropical Pacific.
The data can be downloaded from the following link:https://github.com/dianaveronez/Diana_CLIM680_project/blob/main/nino34_1982-2019.oisstv2_anoms.nc
   
> Precipitation Data
The data used in this study was Global Precipitation Climatology Project (GPCP).
- Date: 	1979-01-01 00:00:00 UTC - 2021-12-01 00:00:00 UTC. This study focuses on the dataset spans from 2020 to 2018.
- Model:	GPCP - Global Precipitation Climatology Project,  Monthly Precipitation Data.

The data can be downloaded from NOAA repository. Link: https://psl.noaa.gov/repository/entry/show?entryid=9aaab85c-cdd3-44af-810c-12a1b23ccf5d or https://github.com/dianaveronez/Diana_CLIM680_project/blob/main/GPCP_NOAA_precip.mon.mean.nc
https://github.com/dianaveronez/Diana_CLIM680_project/blob/main/README.md

## Code description and results

### Project Notebook via Github
The files about this project you can find in the link: https://github.com/dianaveronez/Diana_CLIM680_project

### Conda Environment
The climate2.yml file defines the environment needed to run all code successfully.

### Libraries
 To work using code is important to plan all the libraries and modules that will be necessary. In this project, the mean libraries used on the notebook were: xarray as xr, matplotlib.pyplot as plt, numpy as np, cartopy.crs as ccrs, cartopy.mpl.ticker as sticker, scipy.stats, and cartopy.util import add_cyclic_point.

 ### Monthly Mean Precipitation  
 
   ![image](https://github.com/user-attachments/assets/f67667a9-0c88-492a-9132-326900bc3610)

                 Picture: Monthly Mean Precipitation Global View

 ![monthly_precipitation](https://github.com/user-attachments/assets/52d176e3-a4ae-4ddf-ba26-1948356b2ce7)
 Picture: Monthly Mean Precipitation VA View

 
###  Nino3.4 Index
As we read in the introduction, the ENSO can affect the precipitation.
In the next steps, we will define El Nino, La Nina, or Neutral from 2000 until 2018.

 
![image](https://github.com/user-attachments/assets/14589062-189b-44b9-ab5e-a2b75d984184)



                    Picture: Nino 3.4 Indes for 1985 - 2020

To continue, the script analyzes sea surface temperature (SST) data to classify periods as El Nino, La Nina, or Neutral from 2000 to 2018. It performs the following tasks:
1. Classifies SST data into El Nino, La Nina, and Neutral categories based on temperature thresholds.
2. Counts the number of time points in each category.
3. Plots the SST data over time, highlighting El Nino, La Nina, and Neutral periods with different colors.
Variables:
- elnino: SST data points classified as El Nino (SST >= 0.5).
- lanina: SST data points classified as La Nina (SST <= -0.5).
- neutral: SST data points classified as Neutral (-0.5 < SST < 0.5).
- counts: List containing the counts of time points in El Nino, La Nina, and Neutral categories.
Plot:
- The SST data is plotted over time with different colors indicating El Nino (red), La Nina (blue), and Neutral (green) periods.

The next picture shows us the results for SST for 2000 - 2018 with El Nino, La Nina, and Neutral Periods.


  ![image](https://github.com/user-attachments/assets/f701136c-445b-4293-a587-c49a27f27c1a)
 
             Picture: SST for 2000 to 2018 with El Nino, La Nina, and Neutral Pediods.

These analyses allow us to know that in the period we have 53 El Nino, 110 Neutral, and 63 La Nina.

### Composite Precipitation Anomalies
To continue, we upload the Global Precipitation Climatology Project (GPCP) and calculate the mean precipitation anomalies for El Niño, La Niña, and neutral conditions from a dataset.

![image](https://github.com/user-attachments/assets/069bbcbe-36f6-4c55-a793-6cd207489c43)

    Picture: Composite Precipitation Anomalies during ENSO 2000-2018

### Differences
The next map shows us the differences between El Nino and Neutral and La Nina and Neutral.

![image](https://github.com/user-attachments/assets/286da412-c0c1-4f51-8d55-42440f8ccc7f)

      Picture: Composite Precipitation Differences during ENSO 2000-2018

### T-Statistic

The next picture allows us to understand the T- Statistic for El nino vs Neutral and La nina and Neutral.

![image](https://github.com/user-attachments/assets/c4820e91-7891-4e34-bfd7-2b9074a02da9)

Picture:

![image](https://github.com/user-attachments/assets/75906a2f-e62a-4014-b813-617f09dbaa91)

Picture:

Difference between composites and also mark where it is significant.

![image](https://github.com/user-attachments/assets/f6979cbc-0fa1-4e16-b351-8cd4f8e11e93)

Picture: 

![image](https://github.com/user-attachments/assets/0b9ceb42-1794-42d0-8c7e-7878669adff8)

Picture:

##  Analysis
 



## Summary, Discussion, and Future Work

## References
Smith, J., Brown, K., & Lee, R. (2020). Hydrology in a changing world: Managing water resources. Springer.
Trenberth, K. E., et al. (2007). The impacts of El Niño and La Niña on precipitation patterns. Journal of Climate Science, 20(1), 123-135.
McPhaden, M. J., et al. (2021). ENSO and global hydrology: A review. Nature Climate Change, 11(3), 181-190.
County Climate Action Team. (2023). Arlington County climate risk assessment report. Available at: Arlington County Report
Murray, D., et al., (2020) Facility for Weather and Climate Assessments (FACTS): A Community Resource for Assessing Weather and Climate Variability. Bull. Amer. Meteor. Soc., 101, E1214–E1224, doi: 10.1175/BAMS-D-19-0224.1
Adler et al. (2016) An Update (Version 2.3) of the GPCP Monthly Analysis. (in Preparation). Huffman, G.J., R.F. Adler, P. Arkin, A. Chang, R. Ferraro, A. Gruber, J. Janowiak, A. McNab, B. Rudolf, U. Schneider, 1997: The Global Precipitation Climatology Project (GPCP) Combined Precipitation Dataset. Bull. Amer. Meteor. Soc., 78(1), 5-20.

## Acknowledgements
 I would like to thank CLIM680 professor for coding assistance and answering question.


https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

