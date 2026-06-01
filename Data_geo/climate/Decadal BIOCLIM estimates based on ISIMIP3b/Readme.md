------------------------------------------------------------------------

# Readme

Downloaded from: <https://doi.org/10.5281/zenodo.20446984> on the 01.06.2026 by Andrés Mármol

## Decadal BIOCLIM estimates based on ISIMIP3b climatic forcing data globally for the terrestrial realm

Authors/Creators Jung, Martin (Producer)

ORCID: <https://orcid.org/0000-0002-7569-1390>

##Description

This dataset contains BIOCLIM variables (plus gdd5 and gsl5) which have been prepared and calculated from the original ISIMIP3b bias-adjusted climate forcing data from 4 (for ssp119), respectively 5 GCM models (obtained on 2024-03-24).

For more information on the original data and its properties, please see the ISIMIP3b modelling protocol and here specifically the climate forcing section <https://protocol.isimip.org/#/ISIMIP3b/31-forcing-data> and Frieler et al. (2024).

The original climate forcing data (global extent, daily temporal grain) were masked to a global land mask and spatial-temporally aggregated. Here 10 year (decadal) steps were chosen as target climatology.

For each time slot (e.g. 10 years) and scenario (historical or ssps) the following 21 variables were calculated:

bioclim01 = Annual Mean Temperature

bioclim02 = Mean Diurnal Range (Mean of monthly (max temp - min temp))

bioclim03 = Isothermality (BIO2/BIO7) (×100)

bioclim04 = Temperature Seasonality (standard deviation ×100)

bioclim05 = Max Temperature of Warmest Month

bioclim06 = Min Temperature of Coldest Month

bioclim07 = Temperature Annual Range (BIO5-BIO6)

bioclim08 = Mean Temperature of Wettest Quarter

bioclim09 = Mean Temperature of Driest Quarter bioclim10 = Mean Temperature of Warmest Quarter

bioclim11 = Mean Temperature of Coldest Quarter

bioclim12 = Annual Precipitation

bioclim13 = Precipitation of Wettest Month

bioclim14 = Precipitation of Driest Month

bioclim15 = Precipitation Seasonality (Coefficient of Variation)

bioclim16 = Precipitation of Wettest Quarter

bioclim17 = Precipitation of Driest Quarter

bioclim18 = Precipitation of Warmest Quarter

bioclim19 = Precipitation of Coldest Quarter

GDD5 = Mean annual growing degree days above 5C using daily mean temperature ((tasmax + tasmin) / 2)

GSL5 = Mean annual longest consecutive run of days with daily mean temperature above 5C

------------------------------------------------------------------------

##Data properties:

|  |  |
|-----------------------------|-------------------------------------------|
| Shared Socioeconomic Pathways (SSP) | SSP1-1.9, SSP1-2.6, SSP2-4.5, SSP3-7.0, SSP5-8.5 |
| General circulation models (GCMs) | GFDL-ESM4, IPSL-CM6A-LR, MPI-ESM1-2-HR, MRI-ESM2-0, UKESM1-0-LL |
| Spatial grain | 0.5 degree (\~50km²) |
| Geographic projection | WGS 84 |
| Temporal grain | 10 year steps |
| Spatial extent | Global (see screenshot) |
| Temporal extent | 1850 to 2010 (Historical), 2010 - 2100 (Future) |
| Number of variables | 21 |

All files are provided in netCDF (nc) format. The preprocessed datasets are provided as it and the author takes no responsibility for errors or misuse.
