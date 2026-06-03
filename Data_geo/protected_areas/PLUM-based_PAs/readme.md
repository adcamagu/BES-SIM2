# LandSyMM-PLUM protected area layers

------------------------------------------------------------------------

# Code folder

This folder contains the code developed to integrate the original ascii files into an EBVcube.

------------------------------------------------------------------------

# Cube folder

This folder contains the resulting EBVcubes

------------------------------------------------------------------------

# Raw folder

These datasets were shared with us by Jay Burns ([jay.burns\@ed.ac.uk](mailto:jay.burns@ed.ac.uk){.email}) by email to Andres Marmol on the 05.02.2026

Original datasets where stored in: "`I:/biocon/Projects/BES-SIM 2/Data_geo/protected_areas/PLUM-based_PAs`".

## Protected area datasets by scenario

All scenario-specific protected area (PA) datasets share a common grid specification, summarised below:

| Parameter    | Value                            |
|--------------|----------------------------------|
| Resolution   | 0.5 degrees                      |
| CRS          | WGS 84 (EPSG:4326)               |
| NCOLS        | 720                              |
| NROWS        | 360                              |
| XLLCORNER    | -180                             |
| YLLCORNER    | -90                              |
| Cell values  | 0-1 (fraction of cell protected) |
| NODATA value | -999                             |

Cell values represent the **fraction of each grid cell that falls within a protected area**, ranging from 0 (no protection) to 1 (fully protected).

------------------------------------------------------------------------

## Dataset Overview

| \# | Scenario | File | Interpolation Period |
|----------------|----------------|----------------|-------------------------|
| 1 | BAU / Starting point (all NFF-based scenarios) | `WDPA_Jul025.asc` | \- |
| 2 | Nature for Nature (`NfN_NfN` and `NfN_SSP2`) | `PLUM_mask_NfN_merge.asc` | 2025-2040 |
| 3 | Nature for Society (`NfS_NfS` and `NfS_SSP2`) | `PLUM_mask_NfS_merge.asc` | 2025-2030 |
| 4 | Nature as Culture (`NaC_NaC` and `NaC_SSP2`) | `PLUM_mask_NaC_merge.asc` | 2025-2030 |

The WDPA dataset represents the current distribution of protected areas and serves as the common starting point from which all NFF-based scenario PA maps are interpolated.

------------------------------------------------------------------------

## Methodological Notes

**Fractional land cover.** PLUM operates at 0.5° resolution with fractional land cover, meaning multiple land cover types can co-exist within a single grid cell.

**Temporal interpolation.** PA maps are linearly interpolated from the common WDPA starting distribution to the scenario-specific target PA map over the period indicated in the table above.

**Land cover prioritisation.** Based on the total fraction of a cell to be protected at a given timestep, PLUM prioritises land cover classes in the following order: barren and natural classes first, followed by forest classes, and finally agricultural classes.

**Management intensity constraints.** For the NfS and NaC variants, management intensity constraints are parameterised separately from PA status and interpolated over the period 2025â€“2040. For NfN variants, management constraints are directly tied to PA status.

------------------------------------------------------------------------

# Code

This folder contains the code developed to integrate the original ascii files into an EBVcube.

------------------------------------------------------------------------

# Cube

This folder contains the resulting EBVcubes
