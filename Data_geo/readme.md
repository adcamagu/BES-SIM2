# Data_geo folder:

### Version control

11.03.2026 Readme created

01.06.2026: Content in the climate folder changed.

- All climate data is now indicated in the main Readme file in GitHub (<https://github.com/adcamagu/BES-SIM2>).

- Decadal BIOCLIM estimates based on ISIMIP3b are now available (shared by Martin Jung).

## Description:

This folder stores all input datasets, from raw to processed, and includes the notebooks for processing them to ensamble the EBVcubes.

### Climate data

- one sub-folder: (1) Decadal BIOCLIM estimates based on ISIMIP3b .

  - This folder contains .nc files for decadal BIOCLIM data, from historical SSP1-RCP2.6, SSP2-RCP4.5, SSP3-RCP7.0, SPP4-RCP6.0, SSP5-RCP8.5.

### land_use

- Two subfolders: (1) GLOBIO; (2) LandSyMM-PLUM. Each of them contain 3 subfolders that are: cubes, raws and scripts.

  - cubes subfolder: contains the processed land use datasets to be used in the modelling exercise.

  - raw subfolder: contains the raw datasets shared with us by the land use modelling teams.

  - scripts: contains the scripts use to process the raw data into the EBV data cubes.

NOTE: in this folder we will also upload the land use projections provided by MAgPIE in the upcoming weeks.

### protected_areas:

- To subfolders: (1) GLOBIO-based_PAs and (2) PLUM-based_PAs. Each of them containing cubes, raw and scripts; following the same logic explained in land_use.

### tutorial_code:

- Folder containing a guide to use and explore EBVcube .nc files.
