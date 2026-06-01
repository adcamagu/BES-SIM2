# GLOBIO protected area layers

------------------------------------------------------------------------

# Code

This folder contains the code developed to integrate the original ascii files into an EBVcube.

------------------------------------------------------------------------

# Cube

This folder contains the resulting EBVcubes

------------------------------------------------------------------------

# Raw folder

These datasets were provided by Michel Bakkanes ([Michel.Bakkenes\@pbl.nl](mailto:Michel.Bakkenes@pbl.nl){.email}) by email to Andres Marmol on the 16.01.2026.

The datasets were downloaded from the following link: <https://filesender.surf.nl/?s=download&token=33f03ddb-c0ce-4eb3-acf1-ee87494800eb>

Original datasets where stored in: "I:/biocon/Projects/BES-SIM 2/Data_geo/protected_areas/GLOBIO-based_PAs/raw".

The datasets are the same as those used in Kok et al. (2023). Conservation Biology. <https://doi.org/10.1016/j.biocon.2023.110068>

## Dataset Overview

| Scenario | File | Description |
|----|----|----|
| Nature for Nature (NfN) | `pa_reduce_HE_70.tif` | Half Earth-based PA layer |
| Nature for Society (NfS) | `pa_reduce_WE.tif` | Whole Earth / Sharing the Planet-based PA layer |
| Nature as Culture (NaC) | — | No PA layer applied for this scenario |

------------------------------------------------------------------------

## Dataset Descriptions

### Nature for Nature — Half Earth-based (`pa_reduce_HE_70.tif`)

This raster contains three distinct cell values that act as suitability multipliers:

| Value | Meaning |
|----|----|
| `0` | Protected area — suitability of the grid cell is multiplied by 0 (fully suppressed) |
| `0.95` | Partial reduction — suitability is slightly reduced within the grid cell |
| `1` | Unprotected area — no reduction in suitability applied |

> **Note:** The 0.95 value introduces a slight suitability reduction for certain grid cells. Contact Rob Alkemade ([rob.alkemade\@pbl.nl](mailto:rob.alkemade@pbl.nl)) for further details on its parameterisation.

------------------------------------------------------------------------

### Nature for Society — Whole Earth / Sharing the Planet-based (`pa_reduce_WE.tif`)

This raster contains two cell values:

| Value | Meaning          |
|-------|------------------|
| `0`   | Protected area   |
| `1`   | Unprotected area |

------------------------------------------------------------------------

### Nature as Culture (NaC)

No protected area layer was applied for this scenario.
