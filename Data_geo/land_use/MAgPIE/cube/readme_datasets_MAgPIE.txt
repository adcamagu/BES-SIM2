EBV Data Portal Datasets — LUH3 v1.1 / MAgPIE
================================================

This folder contains finalised EBV Cube NetCDF datasets derived from
LUH3 v1.1 land-use projections prepared for CMIP7, organised by EBV
type and ready for integration into the EBV Data Portal.

Source data : LUH3 v1.1 — Land-Use Harmonization dataset
              University of Maryland (UofMD) · Hurtt et al. 2020
              CMIP7 ScenarioMIP
Scenarios   : Low-MAgPIE / VL (REMIND-MAgPIE IAM · author: Alexander Popp)
              H-GCAM / H      (GCAM IAM           · author: Louise Chini)


Datasets
--------

--- Land Cover States ---

1) Popp_ecostr_id105_20260325.nc
   Dataset ID : 105
   Scenario   : VL only (Low-MAgPIE / REMIND-MAgPIE)
   Script     : 02_land_cover_states_id105_id106.Rmd

2) Chini_ecostr_id106_20260325.nc
   Dataset ID : 106
   Scenario   : H only (H-GCAM / GCAM)
   Script     : 02_land_cover_states_id105_id106.Rmd

3) Popp&Chini_ecostr_id105_20260325.nc
   Dataset ID : 105
   Scenario   : VL + H (combined)
   Script     : 02_land_cover_states_id105_id106.Rmd

   EBV class          : Ecosystem Structure
   Spatial resolution : 0.5° (~55 km at equator)
   Temporal coverage  : 2022, 2030, 2050, 2070
   Entities           : 13 land-cover classes
                        (c3ann, c3nfx, c3per, c4ann, c4per, pastr, range,
                         urban, primf, primn, secdf, secdn, pltns)
   Metric             : Land-cover fraction (0–1)
   Fill value         : -3.4e+38


--- Forestry Management ---

4) Popp_ecoser_id107vl_20260325.nc
   Dataset ID : 107
   Scenario   : VL only (Low-MAgPIE / REMIND-MAgPIE)
   Script     : 03_forestry_management_id107.Rmd

5) Chini_ecoser_id107h_20260325.nc
   Dataset ID : 107
   Scenario   : H only (H-GCAM / GCAM)
   Script     : forestry_management_id107.Rmd

6) Popp&Chini_ecoser_id107_20260325.nc
   Dataset ID : 107
   Scenario   : VL + H (combined)
   Script     : 03_forestry_management_id107.Rmd

   EBV class          : Ecosystem Services
   Spatial resolution : 0.5° (~55 km at equator)
   Temporal coverage  : 2022, 2030, 2050, 2070
   Entities           : 5 forest harvest allocation types
                        (rndwd, fulwd, combf, pltns_bfuel, pltns_wdprd)
   Metric             : Allocation fraction of harvested wood biomass carbon (0–1)
   Fill value         : -3.4e+38
   Note               : pltns_bfuel and pltns_wdprd are spatially empty
                        in LUH3 v1.1 and are inserted as fill-value layers.


--- Crop Management and Land-Use Intensity ---

7) Popp_ecoser_id108vl_20260330.nc
   Dataset ID : 108
   Scenario   : VL only (Low-MAgPIE / REMIND-MAgPIE)
   Script     : 04_crop_management_id108.Rmd

8) Chini_ecoser_id108h_20260410.nc
   Dataset ID : 108
   Scenario   : H only (H-GCAM / GCAM)
   Script     : 04_crop_management_id108.Rmd

9) Popp&Chini_ecoser_id108_20260410.nc
   Dataset ID : 108
   Scenario   : VL + H (combined)
   Script     : 04_crop_management_id108.Rmd

   EBV class          : Ecosystem Services
   Spatial resolution : 0.5° (~55 km at equator)
   Temporal coverage  : 2022, 2030, 2050, 2070
   Entities           : 6 crop types
                        (c3ann, c3nfx, c3per, c4ann, c4per, flood)
   Metrics            : 4 management intensity variables
                        (fertl  = nitrogen fertilization, kg ha-1 yr-1)
                        (irrig  = irrigated fraction, 0–1)
                        (cpbf1  = 1st generation biofuel fraction, 0–1)
                        (cpbf2  = 2nd generation biofuel fraction, 0–1)
   Fill value         : -3.4e+38
   Note               : cpbf1 and cpbf2 are all-zero in LUH3 v1.1.
                        They are included for structural completeness
                        and will be updated in future dataset versions.


--- Protected Areas ---

   Dataset ID : 109
   Status     : NOT GENERATED

   Protection fractions (prtct_primf, prtct_primn, prtct_secdf,
   prtct_secdn, prtct_pltns) are all-zero in LUH3 v1.1. EBV Cube
   creation is deferred until non-zero data are available in a future
   version of the dataset.


Naming Convention
-----------------

   <first_author>_<ebv_class>_id<ID>[scenario]_<YYYYMMDD>.nc

   first_author : surname of the primary scenario author
                  (Popp = VL/REMIND-MAgPIE, Chini = H/GCAM,
                   Popp&Chini = combined)
   ebv_class    : abbreviated EBV class
                  (ecostr = Ecosystem Structure,
                   ecoser = Ecosystem Services)
   ID           : dataset identifier on the EBV Data Portal
   scenario     : optional suffix for single-scenario cubes (vl or h)
   YYYYMMDD     : date the cube was created


Technical Notes
---------------

   Coordinate Reference System : EPSG:4326 (WGS84, geographic)
   Projection                  : None (unprojected lat/lon)
   Temporal extent             : 2022–2070 (4 time steps)
   Standard                    : EBV Cube NetCDF (ebvcube R package)
   Extraction script           : 01_extract_tiffs.Rmd
