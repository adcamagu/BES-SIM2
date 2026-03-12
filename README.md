![](images/BESSIM_logo_v2_Colour.png)

This repository contains all scripts and datasets used for the analysis and figures for the second Biodiversity and Ecosystem Services Scenario Inter-Model comparison (BES-SIM 2)

This repository, and its releases be will be available to download from Zenodo.

## Authors

Henrique M. Pereira, Andres Marmol-Guijarro, Emmanuel Oceguera, Magali Weissgerber and Gavin Stark.

## Version history

Version 1.0, 29.01.2026 (Link to be created)

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
   │  └─ ISIMIP3b\
   ├─ land_use\t
   │  ├─ GLOBIO\
   │  │  ├─ cubes\
   │  │  ├─ raw\
   │  │  └─ scripts\
   │  └─ PLUM\
   │     ├─ cubes\
   │     ├─ raw\
   │     └─ scripts\
   ├─ ne_110m_land\
   └─ protected_areas\
      ├─ GLOBIO-based_PAs\
      └─ PLUM-based_PAs\
```

For output files

```         
└─ BES_results\
   ├─ EBVcube_ensamble_Tutorial\
   ├─ results_biodiversity\
   │   ├─ Model1\
   │   │   ├─ EBVcubes\
   │   │   └─ reports\
   │   └─ Model2\
   │       ├─ EBVcubes\
   │       └─ reports\
   └─ results_ecosystems\
       ├─ Model3\
       │   ├─ EBVcubes\
       │   └─ reports\
       └─ Model4\
           ├─ EBVcubes\
           └─ reports\
```

## Land use datasets.

Raw data sets include: 1) land use projections; and 2) land use intensities for agriculture and forestry.

Two modelling teams (three in the coming weeks) have submitted their land use projections as part of BES-SIM 2 and will be available in the following links:

| ID  | Title                                         | DOI | Resolution     |
|-----|-----------------------------------------------|-----|----------------|
| 98  | Land Use projection (BES-SIM 2 GLOBIO)        | TBD | 10 arc seconds |
| 99  | Land Use projection (BES-SIM 2 LandSymm-PLUM) | TBD | 0.01 degrees   |

In addition, two coarser versions of LandSyMM-PLUM and GLOBIO are provided.

| ID  | Title                                                | DOI | Resolution  |
|------------------|------------------|-----------------|------------------|
| 102 | Upscaled Land Use projections (BES-SIM 2 GLOBIO)     | TBD | 0.5 degrees |
| 103 | Upscaled 0.5 Land Use projections (BES-SIM 2 GLOBIO) | TBD | 0.5 degrees |

The other ancillary datasets are listed below

| ID  | Title                                                | DOI | Resolution  |
|------------------|-------------------|------------------|-------------------|
| 100 | Forest management (BES-SIM 2 LandSyMM-PLUM)          | TBD | 0.5 degrees |
| 101 | Crop areas and intensities (BES-SIM 2 LandSyMM-PLUM) | TBD | 0.5 degrees |

A third data set from the modelling team at PIK using MAgPIE-REMIND model is also expected to be shared with the modelling teams.

### From raw to data cubes: processing original land use datasets:

Each of the land use projections and ancillary data has been processed from their raw versions delivered to NetCDF data cubes to be distributed among the modelling teams. Individual notebooks on how to process the raw data are provided in the `script` subfolder within each land_use folder (see folder structure). All of them are accessible through NextCloud.

### Climate data

Two different datasets of climate are available in the BES-SIM 2 NextCloud.

1.  ISIMIP3b datasets derived from the ISPL-CM6A-LR. A total of 9 files for each climate scenario are provided to fill the full time extent. This means that for SSP1-RCP2.6 there are nine .nc files.

| Name | Format | Time extent | Resolution |
|-----------------------------------|-------------|-------------|-------------|
| ipsl-cm6a-lr_r1i1p1f1_w5e5_ssp126_tas_global_daily | NetCDF | 2015-2100 | 0.5 degrees |
| ipsl-cm6a-lr_r1i1p1f1_w5e5_ssp245_tas_global_daily | NetCDF | 2015-2100 | 0.5 degrees |
| ipsl-cm6a-lr_r1i1p1f1_w5e5_ssp460_tas_global_daily | NetCDF | 2015-2100 | 0.5 degrees |

2.  WorldClim datasets derived from ISPL-CM6A-LR.

| Name                                             | Time extent | Resolution |
|---------------------------------------|----------------|----------------|
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp126_2021-2040.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp126_2041-2060.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp126_2061-2080.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp245_2021-2040.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp245_2041-2060.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_IPSL-CM6A-LR_ssp245_2061-2080.tif | 2015-2100   | 10 min     |
| wc2.1_10m_bioc_1.tif                             | 1970-2000   | 10 min     |

**NOTE:** Worldclim bioclim datasets do not have projections for SSP4-RCP6.0, posing a challenge for modelling teams aiming to run this scenario in their exercises.

### Protected areas

Protected area layers used by each land use modelling team are available in BES-SIM 2 NextCloud at `\Data_geo\protected_areas`. These layers are model specific and are listed in the table below:

| Model         | Scenarios                | File                               |
|-----------------|----------------------|---------------------------------|
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
