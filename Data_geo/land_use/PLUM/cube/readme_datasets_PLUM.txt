EBV Data Portal Datasets — PLUM / BES-SIM2
==========================================

This folder contains finalised EBV Cube NetCDF datasets derived from
PLUM (BES-SIM2) land-use outputs, prepared for integration into the
EBV Data Portal.

Source data : Parsimonious Land Use Model (PLUM) / BES-SIM2
              Nature Futures Framework scenarios
Scenarios   : NfN       = Nature for Nature
              NfNl      = Nature for Nature (landscape variant)
              NaC       = Nature as Culture
              NfS       = Nature for Society
              BAU       = Business as Usual (baseline)


Datasets
--------

1) alexander_ecostr_id99_20260217.nc
   Dataset ID : 99
   Title      : Land-Use Projections (BES-SIM2 PLUM)
   EBV class  : Ecosystem Structure
   Script     : 

   Global categorical land-use projections from BES-SIM2 (PLUM), based
   on the Nature Futures Framework scenarios.

   Spatial resolution : 0.5° (native PLUM grid)
   Temporal coverage  : 2020, 2030, 2040, 2050, 2060, 2070
   Scenarios          : NfN, NfNl, NaC, NfS, BAU
   Entities           : 10 land-cover classes (HILDA+ classification)
   Metric             : Land-cover class per grid cell
   Fill value         : 
   Data type          : 

   Each grid cell contains a single land-cover class value per time
   step and scenario.


2) alexander_ecostr_id100_20260204.nc
   Dataset ID : 100
   Title      : Forest Management Projections (BES-SIM2 PLUM)
   EBV class  : Cross-cutting (driver of biodiversity change)
   Script     : 

   Global forest management projections from BES-SIM2 (PLUM), based on
   the Nature Futures Framework scenarios.

   Spatial resolution : 0.5° (native PLUM grid)
   Temporal coverage  : 2020, 2030, 2040, 2050, 2060, 2070
   Scenarios          : NfN, NfNl, NaC, NfS, BAU
   Entities           : Forestry (protected), Forestry (unprotected)
   Metrics            : Rotation intensity (harvest frequency)
                        Timber forest area (area managed for wood production)
                        Yield (annualised wood production)
   Fill value         : 
   Data type          : 

   Note (methodology) : Forest rotation is calculated endogenously by
                        PLUM using cost optimisation, incorporating
                        timber costs and yields as inputs.
                        (B. Arednarczyk, 16 March 2026)


3) alexander_croscut_id101_20260202.nc
   Dataset ID : 101
   Title      : Crop Intensity Projections (BES-SIM2 PLUM)
   EBV class  : Cross-cutting (driver of biodiversity change)
   Script     : 

   Global projections of crop areas and management intensities from
   BES-SIM2 (PLUM), based on the Nature Futures Framework scenarios.

   Spatial resolution : 0.5° (native PLUM grid)
   Temporal coverage  : 2020, 2030, 2040, 2050, 2060, 2070
   Scenarios          : NfN, NfNl, NaC, NfS, BAU
   Entities           : Crop type (crop groups) x farming type
                        (conventional / restricted / agrivoltaics)
   Metric             : 
   Fill value         : 
   Data type          : 


4) alexander_ecostr_id102_20260204.nc
   Dataset ID : 102
   Title      : Land-Cover Area Projections (BES-SIM2 PLUM)
   EBV class  : Ecosystem Structure
   Script     : 

   Global projections of land-cover fractional area per class from
   BES-SIM2 (PLUM), based on the Nature Futures Framework scenarios.

   Spatial resolution : 0.5° (native PLUM grid)
   Temporal coverage  : 2020, 2030, 2040, 2050, 2060, 2070
   Scenarios          : NfN, NfNl, NaC, NfS, BAU
   Entities           : 10 land-cover classes
                        (Cropland, Pasture, TimberForest, CarbonForest,
                         UnmanagedForest, OtherNatural, Agrivoltaics,
                         Photovoltaics, Barren, Urban)
   Metric             : Proportion of grid cell covered by each class (0–1)
   Fill value         : 
   Data type          : 


Naming Convention
-----------------

   <first_author>_<ebv_class>_id<ID>_<YYYYMMDD>.nc

   first_author : surname of the dataset's primary author
   ebv_class    : abbreviated EBV class
                  (ecostr   = Ecosystem Structure,
                   croscut  = Cross-cutting)
   ID           : dataset identifier on the EBV Data Portal
   YYYYMMDD     : date the cube was created

   This convention ensures traceability, versioning, and compatibility
   with the EBV Data Portal.


Technical Notes
---------------

   Coordinate Reference System : EPSG:4326 (WGS84, geographic)
   Projection                  : None (unprojected lat/lon)
   Standard                    : EBV Cube NetCDF (ebvcube R package)
