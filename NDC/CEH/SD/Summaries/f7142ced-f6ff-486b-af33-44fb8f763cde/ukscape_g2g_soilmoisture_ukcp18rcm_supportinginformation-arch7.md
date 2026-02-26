# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Overview
- UK-SCAPE program, Work Package 2, investigates climate-change impacts on water quantity in Britain, using Grid-to-Grid (G2G) hydrological model outputs.
- Provides 1km x 1km grid monthly mean soil moisture across Great Britain (GB) and Northern Ireland (NI) for December 1980 to November 2080, driven by UKCP18 Regional (12km) projections.
- Utilizes a 12-member perturbed parameter ensemble (PPE) of the Met Office Hadley Centre Regional Climate Model (RCM) under RCP8.5.
- Includes a complementary dataset driven by observation-based data and related datasets for river flows; also includes spatial lake-identification grids for GB and NI.

## Hydrological model: Grid-to-Grid (G2G)
- National-scale hydrological model providing gridded estimates of natural river flows and soil moisture.
- Operates on a 1km x 1km grid (GB aligned) at a 15-minute time-step; extended to cover NI and sub-catchments in the ROI draining to NI rivers.
- Generally uses spatial data rather than catchment-specific calibration; uses nationally applicable parameter values where needed.
- Does not explicitly model lakes, reservoirs, abstractions, or discharges; lakes influence downstream flows are not accounted for (some soil moisture values are present within lake cells).

## Model inputs and processing
- Inputs: daily precipitation, daily min/max temperature, daily potential evapotranspiration (PE) derived from meteorological variables in UKCP18 PPE.
- Precipitation: bias-corrected using a monthly multiplicative scheme.
- PE: computed via Penman-Monteith, aligned with MORECS for stomatal resistance, adjusted for higher CO2 in future years.
- Downscaling: 12km UKCP18 data downscaled to 1km using:
  - Precipitation: spatial weighting from 1km rainfall patterns; temporally distributed evenly across model time-steps.
  - PE: copied to 1km grid and divided across time-steps.
  - Temperature: downscaled using elevation-based lapse rates; temporally refined with a sine curve to represent within-day variation.
- Spatial inputs (topography, soils) follow established G2G configurations.

## Soil moisture product
- Output: monthly averages of daily mean soil moisture in the unsaturated zone (m water/m soil), equivalent to volumetric soil moisture content θ (0 ≤ θ ≤ 1).
- Domain: 1km x 1km grid cells across GB and NI; includes cells within lakes (lake presence is identified in auxiliary data).
- Soil-moisture values are depth-integrated across the soil column, with soil depth varying spatially.

## Data formats and file structure
- Format: NetCDF4 files, one file per ensemble member, separate for GB and NI.
- File naming:
  - GB: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
- Temporal and spatial specifics:
  - 30-day months due to 360-day calendar in climate model data.
  - Time variable: days since 1900-01-01; monthly soil-moisture values nominally assigned to the first day of the month.
  - GB domain: 700 km × 1000 km on the GB National Grid (lower left 0,0 to upper right 700000,1000000 in metres).
  - NI domain: 187 km × 170 km on the GB National Grid (lower left -7000, 440000 to top right 180000, 610000 in metres).
- Ensemble members: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 are excluded). Use the same ensemble member for both baseline and future comparison.

## Supporting lake information
- To aid interpretation, two additional datasets identify majority lake cells:
  - GB: UKSCAPE_G2G_GB_SoilMoisture_LakeGrid.nc
  - NI: UKSCAPE_G2G_NI_SoilMoisture_LakeGrid.nc
- Lake cells are designated in the grid, with land vs lake classification (1 = land, 2 = lake, -9999 = sea) based on Land Cover Map 2015 data.

## Usage guidance
- Historical comparisons: G2G soil moisture driven by UKCP18 can be compared statistically to soil moisture driven by observation-based inputs; avoid direct point-by-point comparisons due to non-equivalence of weather features at the same date (multi-decadal statistical testing is recommended).
- Climate-change assessment: compare baseline and future periods statistically to explore potential impacts on soil moisture (e.g., trends, shifts in drying/wetting dates).
- Limitations: lakes and lake regulation are not modeled within G2G; lake areas are treated as rivers in the model outputs, so lake dynamics are not captured in the soil moisture estimates.

## Related datasets and cross-references
- Complementary dataset: G2G soil moisture driven by observation-based data (Kay et al., 2021b).
- Related outputs: G2G river flows for GB and NI datasets (references provided in the document).
- MaRIUS-G2G-WAH2 dataset analog: similar soil moisture outputs driven by weather@home climate data (for context).

## Acknowledgements
- Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCAPE programme delivering National Capability.

## References (selected)
- Bell et al. (2009, 2016, 2007, 2018), Kay et al. (2021a, 2021b), Rudd et al. (2017, 2016), Guillod et al. (2017, 2018), Hough & Jones (1997), Monteith (1965), Murphy et al. (2018), Rowland et al. (2017).