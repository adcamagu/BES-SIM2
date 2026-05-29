![](images/BESSIM_logo_v2_Colour.png)

This repository contains all scripts and datasets used for the analysis and figures for the second Biodiversity and Ecosystem Services Scenario Inter-Model comparison (BES-SIM 2)

This repository, and its releases be will be available to download from Zenodo.

## Authors

Henrique M. Pereira, Andres Marmol-Guijarro, Emmanuel Oceguera, Magali Weissgerber and Gavin Stark.

## Version history

Version 1.0, 29.01.2026 (Link to be created)

Version 1.1. 26.05.2026\
Links to climate datasets are provided, replacing the table description of datasets in the previous version.

Addition of ScenMIP7-LUH3 to the `Data_geo` folder

## License

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit <http://creativecommons.org/licenses/by/4.0/> or send a letter to creative Commons PI Box 1866, Mountain View, CA 94042, USA.

All project data is hosted at iDiv and it is mirrored through NextCloud. **NOTE:** Continuous password update are needed when working teams are no longer part of BES-SIM 2 (email from Christopher Zimmerman via [it-support\@idiv.de](#0){.email} on the 23.01.2026 to Andres Mármol).

# Code Folder

### **Main files**

Notebooks to to produce the different figures/analysis for the manuscript.

# Folder structure for code and data

All scripts are run with relative paths. Before run make sure to use the following folder structure:

To process input datasets:

```         
└─ Data_geo\
   ├─ climate_data\
   │  ├─ ISIMIP3b\
   │  └─ WorldClim\
   ├─ land_use\
   │  ├─ GLOBIO\
   │  │  ├─ code\
   │  │  ├─ cube\             # GLOBIO BES-SIM 2 EBVcube .nc files
   │  │  └─ raw\
   │  ├─ PLUM\
   │  │  ├─ code\
   │  │  ├─ cube\             # LandSyMM-PLUM BES-SIM 2 EBVcube .nc files
   │  │  └─ raw\
   │  └─ ScenMIP7-LUH3\
   │     ├─ code\
   │     ├─ cube\
   │     └─ raw\
   └─ protected_areas\
      ├─ GLOBIO-based_PAs\
      │  ├─ code\
      │  ├─ cube\
      │  └─ raw\
      └─ PLUM-based_PAs\
         ├─ code\
         ├─ cube\
         └─ raw\
```

For output files

```         
└─ BES_results\
   ├─ EBVcube_ensamble_Tutorial\
   ├─ results_biodiversity\
   │   ├─ Model1\
   │   │   ├─ EBVcubes\
   │   │   ├─ figures\
   │   │   └─ reports\
   │   └─ Model2\
   │       ├─ EBVcubes\
   │       ├─ figures\
   │       └─ reports\
   └─ results_ecosystems\
       ├─ Model3\
       │   ├─ EBVcubes\
       │   ├─ figures\
       │   └─ reports\
       └─ Model4\
           ├─ EBVcubes\
           ├─ figures\
           └─ reports\
```

## Land use datasets.

Raw data sets include: 1) land use projections; and 2) land use intensities for agriculture and forestry.

Two modelling teams (three in the coming weeks) have submitted their land use projections as part of BES-SIM 2 and will be available in the following links:

| ID | Title | DOI | Resolution | File |
|---------------|---------------|---------------|---------------|---------------|
| 98 | Land Use projection (BES-SIM 2 GLOBIO) | TBD | 10 arc seconds | alkemade_ecostr_id98_20260223.nc |
| 99 | Land Use projection (BES-SIM 2 LandSymm-PLUM) | TBD | 0.01 degrees | alexander_ecostr_id99_20260217.nc |

In addition, two coarser versions of LandSyMM-PLUM and GLOBIO are provided.

| ID | Title | DOI | Resolution | File |
|---------------|---------------|---------------|---------------|---------------|
| 102 | Upscaled Land Use projections (BES-SIM 2 GLOBIO) | TBD | 0.5 degrees | alkemade_ecostr_id103_20260216.nc |
| 103 | Upscaled 0.5 Land Use projections (BES-SIM 2 LandSymm-PLUM) | TBD | 0.5 degrees | alexander_ecostr_id102_20260309.nc\* |

\*dataset needs to be updated to its latest version

The other datasets are listed below

| ID | Title | DOI | Resolution | File |
|---------------|---------------|---------------|---------------|---------------|
| 100 | Forest management (BES-SIM 2 LandSyMM-PLUM) | TBD | 0.5 degrees | alexander_ecostr_id100_20260204.nc |
| 101 | Crop areas and intensities (BES-SIM 2 LandSyMM-PLUM) | TBD | 0.5 degrees | alexander_croscut_id101_20260202.nc |

A third data set from the modelling team at PIK using MAgPIE-REMIND model is also expected to be shared with the modelling teams.

## ⛔⛔⛔ RESTRICTED DATA — BES-SIM 2 INTERNAL USE ONLY⛔⛔⛔

The land use datasets in the repository are **strictly for internal BES-SIM 2 use** and **must not be shared with external teams or collaborators**.

Data will be made available once: (1) Land use modelling teams have published their results (2) he BES-SIM 2 protocol paper is published.

If in doubt, contact the data owners before sharing:

**GLOBIO:** [Rob Alkemade (PBL)](rob.alkemade@pbl.nl)\
LandSyMM-PLUM: [Peter Alexander (University of Edinburgh)](peter.alexander@ed.ac.uk)

### From raw to data cubes: processing original land use datasets:

Each of the land use projections and ancillary data has been processed from their raw versions delivered to NetCDF data cubes to be distributed among the modelling teams. Individual notebooks on how to process the raw data are provided in the `script` subfolder within each land_use folder (see folder structure). All of them are accessible through NextCloud.

### Climate data

Two different datasets of climate are suggested to be used in BES-SIM 2.

1.  **ISIMIP3B datasets derived from the ISPL-CM6A-LR.** The datasets include mean (tas), minimum (tasmin) and maximum (tasmax) air surface temperature, precipitation (pr), near surface relative humidity (hurs), near surface specific humidity (huss), etc. All datasets are found as NetCDFs, spanning from 2015-2100 and at a 0.5 degree resolution. The following table summarises climate data for the Shared Socioeconomic Pathways to be tested in BES-SIM 2 and their links to ISIMIP3b repository.

    | SSP-RCP | Link |
    |---------------|---------------------------------------------------------|
    | SSP1-RCP2.6 | <https://data.isimip.org/search/tree/ISIMIP3b/InputData/climate/atmosphere/ipsl-cm6a-lr/ssp126/> |
    | SSP2-RCP4.5 | <https://data.isimip.org/search/tree/ISIMIP3b/SecondaryInputData/climate/atmosphere/ipsl-cm6a-lr/ssp245/> |
    | SSP4-RCP6.0 | <https://data.isimip.org/search/tree/ISIMIP3b/SecondaryInputData/climate/atmosphere/ipsl-cm6a-lr/ssp460/> |

<https://www.worldclim.org/data/cmip6/cmip6_clim10m.html>

2.  **WorldClim datasets derived from ISPL-CM6A-LR.** Worldclim datasets variables available are monthly average minimum temperature (°C) (tn), monthly average maximum temperature (°C) (tx), monthly total precipitation (mm) (pr), and bioclimatic variables (bc), for the periods 2021-2040, 2041-2060, 2061-2080 and 2081-2100 for SSP1-RCP2.6 and SSP2-RCP4.5 that will be used in BES-SIM 2. Datasets are available at different resolutions and they are summarised in the folllowing table.

    | Spatial Resolution | Links |
    |--------------------|----------------------------------------------------|
    | 30 seconds | <https://www.worldclim.org/data/cmip6/cmip6_clim30s.html> |
    | 2.5 minutes | <https://www.worldclim.org/data/cmip6/cmip6_clim2.5m.html> |
    | 5 minutes | <https://www.worldclim.org/data/cmip6/cmip6_clim5m.html> |
    | 10 minutes | <https://www.worldclim.org/data/cmip6/cmip6_clim10m.html> |

**NOTE:** Worldclim bioclim datasets do not have projections for SSP4-RCP6.0, posing a challenge for modelling teams aiming to run this scenario in their exercises.

### Protected areas

Protected area layers used by each land use modelling team are available in BES-SIM 2 NextCloud at `\Data_geo\protected_areas`. These layers are model specific and are listed in the table below:

| Model         | Scenarios                | File                               |
|------------------|-----------------------|-------------------------------|
| GLOBIO        | NfN & NfS                | alkemade_ecostr_idTBD_20260309.nc  |
| LandSyMM-PLUM | NfN, NfNl, NfS, NaC, BAU | alexander_ecostr_idTBD_20260306.nc |

## Biodiversity and ecosystem services models outputs

All modelling teams will upload their files into the `BES_results` folder, within a subfolder with the name of the model in question.

```         
Naming Convention
---------------------------------

EBV Data Cube format - naming convention:

    <first_author>_<ebv_class>_id<ID>_<YYYYMMDD>.nc

Other information:
    - Author(s): (e.g. Oceguera-Conchas Emmanuel, Pereira Henrique)
    - Spatial resolution: (e.g. 0.5°)
    - Temporal coverage: (e.g. 2020, 2030, 2040, 2050, 2060, 2070)
    - Scenarios: (e.g. NfN, NfNl, NaC, NfS, BAU)
    - EBV class: (e.g. Ecosystem Structure)
    
# This ensures traceability, versioning, and compatibility with EBV Portal


Coordinate Reference System - CRS
---------------------------------
    - EPSG:4326 (WGS84)
```

# 
