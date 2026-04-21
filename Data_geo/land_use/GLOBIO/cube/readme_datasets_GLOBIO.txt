EBV Data Portal Datasets — GLOBIO / BES-SIM2
================================================

This folder contains finalised EBV Cube NetCDF datasets derived from
GLOBIO (BES-SIM2) land-use and land-cover outputs, prepared for
integration into the EBV Data Portal.

Source data: GLOBIO4 / BES-SIM2 land-use projections
             ESA-CCI land cover, processed through the IMAGE model
             and GLOBIO allocation module


Datasets
--------

1) alkemade_ecostr_id98_20260223.nc
   Dataset ID : 98
   Title      : Land-Use Projections (BES-SIM2 GLOBIO) — 10 arcseconds
   EBV class  : Ecosystem Structure
   Script     : 01_landuse_conversion_id98.Rmd

   Global categorical land-use projections at native GLOBIO resolution,
   derived from ESA-CCI land cover.

   Spatial resolution : ~300 m (10 arcseconds)
   Temporal coverage  : 2020, 2030, 2050, 2070
   Scenarios          : Nature for Nature (NfN), Nature as Culture (NaC),
                        Nature for Society (NfS), SSP2-Baseline
   Entities           : 12 terrestrial land-cover classes (binary rasters)
   Metric             : Presence/absence (0/1) per land-cover class
   Fill value         : -1
   Data type          : byte (INT1S)

   Each grid cell contains a binary value per land-cover class,
   time step, and scenario.


2) alkemade_ecostr_id103_20260216.nc
   Dataset ID : 103
   Title      : Land-Use Projections (BES-SIM2 GLOBIO) — 0.5 degrees
   EBV class  : Ecosystem Structure
   Script     : 02_landuse_downscaling_id103.Rmd

   Global land-use projections aggregated from ~300 m to 0.5° spatial
   resolution. Each class fraction represents the proportion of a 0.5°
   grid cell occupied by that land-cover class.

   Spatial resolution : 0.5° (~55 km at equator)
   Temporal coverage  : 2020, 2030, 2050, 2070
   Scenarios          : Nature for Nature (NfN), Nature as Culture (NaC),
                        Nature for Society (NfS), SSP2-Baseline
   Entities           : 12 terrestrial land-cover classes
   Metric             : Fraction of grid cell (0–1)
   Fill value         : -3.4e+38
   Data type          : float

   Each 0.5° grid cell contains the fractional area covered by each
   land-cover class per time step and scenario.


Naming Convention
-----------------

   <first_author>_<ebv_class>_id<ID>_<YYYYMMDD>.nc

   first_author : surname of the dataset's primary author
   ebv_class    : abbreviated EBV class (e.g. ecostr = Ecosystem Structure)
   ID           : dataset identifier on the EBV Data Portal
   YYYYMMDD     : date the cube was created

   This convention ensures traceability, versioning, and compatibility
   with the EBV Data Portal.


Technical Notes
---------------

   Coordinate Reference System : EPSG:4326 (WGS84, geographic)
   Projection                  : None (unprojected lat/lon)
   Standard                    : EBV Cube NetCDF (ebvcube R package)
