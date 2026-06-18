# Readme

## EBV Data Portal Datasets — LUH3 v1.1 / H-GCAM + VL-MAgPIE (Chini)

Readme Author: Andrés Mármol, Emmanuel Oceguera-Conchas

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

CContent : 15 entities — 13 land-cover classes (c3ann, c3nfx, c3per, c4ann, c4per, pastr, range, urban, primf, primn, secdf, secdn, pltns) plus secondary mean age (secma) and secondary mean biomass carbon density (secmb)

EBV class : Ecosystem Structure

Metric : Land cover type — fraction (0-1) of the grid cell occupied by each land cover class.

### Crop Management and Land-Use Intensity

chini_ecoser_id107_20260410.nc

Dataset ID : 107

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 6 crop types × 4 management intensity variables (c3ann, c3nfx, c3per, c4ann, c4per, flood) (fertl, irrig, cpbf1, cpbf2)

EBV class : Ecosystem Structure

Metric :
- Fertilization (fertl) — fertilization rate applied per crop type per growing season. Units: kg ha-1 yr-1
- Irrigation (irrig) — fraction of each crop type area that receives irrigation water. Units: Fraction (0-1)
- Crop biofuel 1st generation (cpbf1) — fraction of each crop type area dedicated to 1st generation biofuel production, where conventional food crops are converted to fuel. Units: Fraction (0-1)
- Crop biofuel 2nd generation (cpbf2) — fraction of each crop type area dedicated to 2nd generation biofuel production. Units: Fraction (0-1)

Note : The flood entity (flood_c3ann) is the fraction of C3 annual crop area under permanent flooding (paddy rice). It is included under the irrigation metric due to its comparable definition (the flood prefix is kept to avoid confusion) and inserted as an empty entity (fill value -3.4e+38) in the fertilization and biofuel metrics, since these are undefined for flooded cultivation in the source dataset.

### Secondary Vegetation State

chini_ecofun_id108_20260417.nc

Dataset ID : 108

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 1 entity (Secondary land)

EBV class : Ecosystem Functioning

Metric :
- Mean age — Mean age of secondary land in each grid cell, tracking the time elapsed since the last human disturbance event. Secondary land starts at age zero at the moment of disturbance and increases by one each subsequent year. It can range from very young recovering vegetation to stands of very mature age similar to primary land of the same type. Units: years
- Mean biomass carbon density — Mean biomass carbon density of secondary land in each grid cell, representing the accumulated carbon stock during vegetation recovery from human disturbance. Secondary land starts at zero at the moment of disturbance and accumulates carbon each subsequent year according to the underlying potential biomass density and regrowth rate, up to values similar to primary land of the same type. Units: kg m-2

### Forestry Management

chini_ecoser_id109_20260325.nc

Dataset ID : 109

Spatial resolution : 0.25° (\~28 km at equator)

Temporal coverage : 2022, 2030, 2050, 2070

Content : 5 harvested-wood biomass allocation entities (rndwd, fulwd, combf, pltns_bfuel, pltns_wdprd)

EBV class : Ecosystem Structure

Metric : Allocation of harvested biomass — fraction of harvested wood biomass carbon allocated to each forestry use type (rndwd, fulwd, combf, pltns_bfuel, pltns_wdprd). Units: Fraction (0-1)

Note : pltns_bfuel and pltns_wdprd are included as entities but contain no data — LUH3 v1.1 does not yet provide spatially explicit plantation forest information, although the underlying IAM scenarios may include it. Added tree cover (addtc) is excluded, as it is 0 across all years and scenarios and uses a different unit (fraction of grid cell).

## Naming Convention

<first_author>\_<ebv_class>*id*<ID>[scenario]<YYYYMMDD>.nc

## Technical Notes

Coordinate Reference System : EPSG:4326 (WGS84, geographic) Projection : None (unprojected lat/lon) Spatial extent : -180 to 180° lon, -90 to 90° lat Spatial dimensions : 720 rows × 1440 cols Temporal extent : 2022–2070 (4 time steps) Temporal units : Days since 1860-01-01 00:00:00.0
