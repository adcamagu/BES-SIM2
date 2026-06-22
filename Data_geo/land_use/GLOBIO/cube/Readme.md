# Readme

## EBV Data Portal Datasets — GLOBIO / BES-SIM2

Readme Author: Andrés Mármol, Emmanuel Oceguera-Conchas

Date: 22.06.2026

This folder contains finalised EBV Cube NetCDF datasets derived from GLOBIO (BES-SIM2) land-use and land-cover outputs, organised by EBV type and ready for integration into the EBV Data Portal.

Source data : GLOBIO4 / BES-SIM2 land-use projections — ESA-CCI land cover, processed through the IMAGE model and the GLOBIO land use allocation module

Scenarios : NfN  = Nature for Nature 
            NaC  = Nature as Culture
            NfS  = Nature for Society
            SSP2-Baselin
            — author: Rob Alkemade (PBL Netherlands Environmental Assessment Agency)

## Datasets

### Land Cover (10 arcseconds)

alkemade_ecostr_id98_20260223.nc

Dataset ID : 98

Spatial resolution : ~300 m (10 arcseconds)

Temporal coverage : 2020, 2030, 2050, 2070

Content : 12 terrestrial land-cover classes (urban, cropland, potential secondary vegetation, agroforestry, pasture, rangeland, forestry, secondary vegetation, unmanaged forest, shrubland/grassland, other, bare areas). Water bodies and permanent snow/ice excluded.

EBV class : Ecosystem Structure

Metric :
- Land cover (presence/absence) — binary value (0/1) recording whether each land-cover class occurs within a grid cell for a given scenario and time step. Units: Binary (0-1)

Fill value : -1

Data type : byte (INT1S)

### Upscaled Land Cover (0.5 degrees)

alkemade_ecostr_id103_20260216.nc

Dataset ID : 103

Spatial resolution : 0.5° (~55 km at equator)

Temporal coverage : 2020, 2030, 2050, 2070

Content : 12 terrestrial land-cover classes, aggregated from ~300 m to 0.5°. Each class fraction represents the proportion of a 0.5° grid cell occupied by that land-cover class.

EBV class : Ecosystem Structure

Metric :
- Land cover — fraction of each 0.5° grid cell occupied by each land-cover class for a given scenario and time step. Units: Fraction (0-1)

Fill value : -3.4e+38

Data type : float

## Naming Convention

```
<first_author>_<ebv_class>_id<ID>_<YYYYMMDD>.nc
```
## Technical Notes

Coordinate Reference System : EPSG:4326 (WGS84, geographic) Projection : None (unprojected lat/lon) Standard : EBV Cube NetCDF (ebvcube R package)
