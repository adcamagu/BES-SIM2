# README_Code

### High Resolution datasets

The Code folder is subdivided into the two (soon three) subfolders named after their corresponding land use projection. Each folder contains the code to process the raw data provided by the land use modelling teams which consist of the following steps:

| No. | Step | Model |
|-------|----------------------------------------------|--------------------|
| 1 | Recategorisation |  GLOBIO |
| 2 | Raster disggregation to single independent rasters per band | PLUM (HILDA+); GLOBIO |
| 3 | Binarisation | PLUM (HILDA+); GLOBIO |
| 4 | Creation of the NetCDF data cube | PLUM (HILDA+); GLOBIO |

### Other datasets

PLUM has provided additional model outputs including "forestry.txt.gz", "LandCover.txt.gz", and LandUse.txt.gz". The code available for processing this data setis into data cubes is also included for each of the datasets.
