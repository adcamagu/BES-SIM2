# Readme

## EBV Data Portal Datasets — PLUM / BES-SIM2 (LandSyMM-PLUM)

Readme Author: Andrés Mármol, Emmanuel Oceguera-Conchas

Date: 22.06.2026

This folder contains finalised EBV Cube NetCDF datasets derived from LandSyMM-PLUM (BES-SIM2) land-use outputs, organised by EBV type and ready for integration into the EBV Data Portal.

Source data : Parsimonious Land Use Model (PLUM) / LandSyMM — BES-SIM2. Follows the global narratives of the Nature Futures Framework; land use, land management, and demands estimated using historical and potential yields from LPJ-GUESS.

Scenarios : NfN  = Nature for Nature (RCP 4.5)
            NfNl = Nature for Nature, local (RCP 4.5)
            NaC  = Nature as Culture (RCP 4.5)
            NfS  = Nature for Society (RCP 4.5)
            BAU  = Business as Usual, SSP2 (RCP 4.5)
            — author: Peter Alexander (University of Edinburgh)

## Datasets

### Land Cover

alexander_ecostr_id99_20260217.nc

Dataset ID : 99

Spatial resolution : 0.5° (native PLUM grid)

Temporal coverage : 2020, 2030, 2040, 2050, 2060, 2070

Content : 7 of the 10 HILDA+ land-cover classes after harmonisation (urban, cropland, pasture, forest managed, forest unmanaged, grass/shrubland, other land). Oceans, water and no-data classes excluded.

EBV class : Ecosystem Structure

Metric :
- Land cover — records whether a given land-cover type occurs within each grid cell for a given scenario and time step. Units: Binary (0 or 1)

### Forest Management

alexander_croscut_id100_20260204.nc

Dataset ID : 100

Spatial resolution : 0.5° (native PLUM grid)

Temporal coverage : 2020, 2030, 2040, 2050, 2060, 2070

Content : Forest management projections. Forestry protection is scenario-dependent — management is allowed only in unprotected areas under NfN, NfNl and BAU, while NaC and NfS permit management within protected areas.

EBV class : Cross-cutting (driver of biodiversity change)

Metric :
- Rotation intensity — wood harvest intensity; fraction of area harvested each year, or equivalently the frequency of harvest. Units: frequency of harvest · yr⁻¹
- Timber forest area — area of forest managed for wood production. Units: million hectares
- Yield — annualised wood production. Units: m³ · ha⁻¹ · yr⁻¹

Note : Forest rotation is calculated endogenously by PLUM using cost optimisation, incorporating timber costs and yields as inputs. The reciprocal of rotation intensity gives the rotation length (e.g. an intensity of 0.02 implies a 50-year rotation). At PLUM's spatial scale this represents mixed-age stands — roughly 2% of forested area harvested each year — rather than simultaneous clear-cutting of an entire grid cell (Jay Burns, co-author).

### Crop Areas and Intensities

alexander_croscut_id101_20260202.nc

Dataset ID : 101

Spatial resolution : 0.5° (native PLUM grid)

Temporal coverage : 2020, 2030, 2040, 2050, 2060, 2070

Content : Crop types × farming type (conventional, restricted, agrivoltaics). Crop types: wheat (wheat, barley, oats, other C3 cereals), maize (maize, sorghum, millet, other C4 cereals), rice, oilcropsNFix (soybeans, groundnuts), oilcropsOther (oil palm, rapeseed, coconut, other oil crops), pulses, fruitveg, starchyRoots, sugar (sugar cane and beet), energycrops (Miscanthus).

EBV class : Cross-cutting (driver of biodiversity change)

Metric :
- Area — area covered by a crop type. Units: million hectares
- Fertiliser intensity — Units: 0 to 1
- Fertiliser quantity — Units: kg (N) · ha⁻¹
- Irrigation intensity — Units: 0 to 1
- Irrigation quantity — Units: L · m⁻²
- Other management intensity — Units: 0 to 1
- Yield — Units: tonnes · ha⁻¹

Note : Protection level varies between scenarios. NfN, NfNl and BAU contain no restricted crop types, so those entities appear blank for consistancy. 

### Land-Cover Area (Native 0.5°)

alexander_ecostr_id102_20260204.nc

Dataset ID : 102

Spatial resolution : 0.5° (native PLUM grid)

Temporal coverage : 2020, 2030, 2040, 2050, 2060, 2070

Content : 10 native PLUM land-cover classes — Cropland, Pasture, TimberForest (managed for timber), CarbonForest (managed for carbon sequestration), UnmanagedForest, OtherNatural, Agrivoltaics, Photovoltaics, Barren, Urban.

EBV class : Ecosystem Structure

Metric :
- Protected proportion — percentage of a grid cell occupied by a given land-cover type that is protected, relative to the combined protected + unprotected area. Units: % (0–100)
- Unprotected proportion — as above, for the unprotected portion. Units: % (0–100)
- Total proportion — protected + unprotected coverage of a given land-cover type within the grid cell. Units: % (0–100)

## Naming Convention

```
<first_author>_<ebv_class>_id<ID>_<YYYYMMDD>.nc
```
## Technical Notes

Coordinate Reference System : EPSG:4326 (WGS84, geographic) Projection : None (unprojected lat/lon) Standard : EBV Cube NetCDF (ebvcube R package)
