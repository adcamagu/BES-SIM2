# Readme

## EBV Data Portal Datasets — LUH3 v1.1 / H-GCAM + VL-MAgPIE (Chini)

Readme Author: Andrés Mármol

Date: 01.06.2026

This folder contains finalised EBV Cube NetCDF datasets derived from LUH3 v1.1 land-use projections prepared for CMIP7, organised by EBV type and ready for integration into the EBV Data Portal.

Source data : LUH3 v1.1 — Land-Use Harmonization dataset University of Maryland (UofMD) · Chini & Hurtt 2026 CMIP7 ScenarioMIP

Scenarios : VL (Low-MAgPIE / REMIND-MAgPIE · author: Alexander Popp) H (H-GCAM / GCAM · author: Louise Chini)

References : Chini, L., & Hurtt, G. (2026). Land-Use Harmonization 3 Future Scenario H v1.1 for ScenarioMIP (LUH3-H v1.1). Zenodo. <https://doi.org/10.5281/zenodo.19354835> Chini, L., & Hurtt, G. (2026). Land-Use Harmonization 3 Future Scenario VL v1.1 for ScenarioMIP (LUH3-VL v1.1). Zenodo. <https://doi.org/10.5281/zenodo.19353397>

## Datasets

### Land Cover States

chini_ecostr_id105_20260325.nc

Dataset ID : 105

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 13 land-cover classes (c3ann, c3nfx, c3per, c4ann, c4per, pastr, range, urban, primf, primn, secdf, secdn, pltns)

EBV class : Ecosystem Structure

Metric : Fraction (0-1) of the grid cell occupied by that land cover type.

### Forestry Management

chini_ecoser_id106_20260325.nc

Dataset ID : 106

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 6 forest harvest allocation types (rndwd, fulwd, combf, pltns_bfuel, pltns_wdprd, addtc)

EBV class : Ecosystem Structure

Metric : Fertilization (kg ha-1 yr-1) rate applied per crop type per growing season

### Crop Management and Land-Use Intensity

chini_ecoser_id107_20260410.nc

Dataset ID : 108

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 6 crop types × 4 management intensity variables (c3ann, c3nfx, c3per, c4ann, c4per, flood) (fertl, irrig, cpbf1, cpbf2)

EBV class : Ecosystem Structure

Metric : Fraction (0-1) of harvested wood biomass carbon allocated to each forestry use type (rndwd, fulwd, combf, pltns_bfuel, pltns_wdprd).

### Secondary Vegetation State

chini_ecofun_id108_20260417.nc

Dataset ID : 109

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 1 entity (Secondary land)

EBV class : Ecosystem Functioning

Metric : Mean age of secondary land in each grid cell, tracking the time elapsed since the last human disturbance event. Secondary land starts at age zero at the moment of disturbance and increases by one each subsequent year. It can range from very young recovering vegetation to stands of very mature age similar to primary land of the same type.

## Naming Convention

<first_author>\_<ebv_class>*id*<ID>[scenario]<YYYYMMDD>.nc

## Technical Notes

Coordinate Reference System : EPSG:4326 (WGS84, geographic) Projection : None (unprojected lat/lon) Spatial extent : -180 to 180° lon, -90 to 90° lat Spatial dimensions : 720 rows × 1440 cols Temporal extent : 2022–2070 (4 time steps) Temporal units : Days since 1860-01-01 00:00:00.0
