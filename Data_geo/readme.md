# Data_geo folder:

### Version control

11.03.2026 Readme created

## Description:

This folder stores all input datasets, from raw to processed, and includes the notebooks for processing them to ensamble the EBVcubes.

### Climate data

-   Three sub-folders: (1) ISIMIP3b; & (2) WorldClim.

    -   ISIMIP files contain .nc files for daily estimates from 2015 to 2100. These are based on IPSL-CM6A models for SSP1-RCP2.6, SSP2-RCP4.5, SPP4-RCP6.0.

    -   WorldClim containts normal mean for 2021-2040 (2030), 2041-2060 (2050) and 2061-2080 (2070) data based on IPSL-CM6A models for SSP1-RCP2.6 and SSP2-RCP4.5. No IPSL-CM6A for SSP4-RCP6.0 are found.

### land_use

-   Two subfolders: (1) GLOBIO; (2) LandSyMM-PLUM. Each of them contain 3 subfolders that are: cubes, raws and scripts.

    -   cubes subfolder: contains the processed land use datasets to be used in the modelling exercise.

    -   raw subfolder: contains the raw datasets shared with us by the land use modelling teams.

    -   scripts: contains the scripts use to process the raw data into the EBV data cubes.

NOTE: in this folder we will also upload the land use projections provided by MAgPIE in the upcoming weeks.

### protected_areas:

-   To subfolders: (1) GLOBIO-based_PAs and (2) PLUM-based_PAs. Each of them containing cubes, raw and scripts; following the same logic explained in land_use.
