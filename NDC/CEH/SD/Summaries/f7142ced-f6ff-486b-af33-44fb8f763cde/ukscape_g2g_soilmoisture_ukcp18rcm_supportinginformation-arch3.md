# Supporting information for: Grid-to-Grid model estimates of soil moisture for Great Britain and Northern Ireland driven by UK Climate Projections 2018 (UKCP18) Regional (12km) data (1980 to 2080)

## Purpose and scope
- Provides Grid-to-Grid (G2G) soil moisture estimates on a 1km x 1km grid across Great Britain (GB) and Northern Ireland (NI) driven by UKCP18 Regional (12km) projections.
- Uses a 12-member perturbed parameter ensemble (PPE) from the Met Office Hadley Centre Regional Climate Model (RCM), covering December 1980 to November 2080 under RCP8.5.
- Part of UK-SCAPE, a five-year NERC-funded program focused on climate change impacts on water quantity and related hydrology.

## Model and driving data
- Hydrological model: Grid-to-Grid (G2G), providing gridded, spatially consistent estimates of soil moisture (and river flows) at 1km resolution.
- For G2G inputs: daily precipitation, daily min/max temperature, and daily potential evaporation (PE) derived from meteorological variables; PE calculated with Penman-Monteith approach; bias correction applied to precipitation.
- Spatial downscaling: 12km PPE data downscaled to 1km using spatial weighting; PE downscaled to 1km, and temperature downscaled with elevation-based lapse rates and daily sine-time scaling.
- Temporal framing: 30-day months due to a 360-day calendar in the climate model.
- Output units: soil moisture in the unsaturated zone (m water per m soil), equivalent to volumetric moisture content (θ) in [0,1]; soil-depth is regionally variable; results are depth-integrated for the whole soil column.

## Data products and formats
- Gridded datasets: one NetCDF4 file per ensemble member, separately for GB and NI.
- File naming:
  - GB: G2G_GB_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
  - NI: G2G_NI_mmsoil_UKCP18RCM_ensnum_1980_2080.nc
- Spatial domains:
  - GB: 700 km x 1000 km on the GB National Grid
  - NI: 187 km x 170 km on the GB National Grid
- Temporal reference: days since 1900-01-01; monthly mean soil moisture values assigned to the first day of each month.
- Auxiliary files: lake grids identifying majority lake cells (to indicate lakes vs. land in the 1km grid).

## Ensemble and usage guidance
- Ensemble members included: 01, 04, 05, 06, 07, 08, 09, 10, 11, 12, 13, 15 (02, 03, 14 omitted).
- Consistent ensemble usage: when comparing periods (baseline vs future), use the same ensemble member across periods.
- Comparisons: historical G2G outputs driven by UKCP18 PPE can be compared statistically to those driven by observation-based inputs (for context), but not point-by-point time-matching; statistical comparisons are valid over multi-decadal scales.
- Relation to other datasets: complementary dataset exists with G2G soil moisture driven by observed data; related datasets cover river flows across GB and NI.
- Interpretation caveats: lakes and reservoirs are not dynamically modeled in G2G; lake cells are treated as rivers, and lake storage impacts on downstream flows are neglected.

## Interpretation and caveats
- The G2G model emphasizes land-only hydrology with natural flow tendencies; anthropogenic influences (abstractions, discharges) and complex subsurface hydrology can affect performance in certain catchments.
- Users should be aware that comparisons across time rely on the same ensemble member and that the calendar and bias-correction schemes introduce nontrivial methodological differences when interpreting trends.

## Data governance, provenance and accessibility
- Metadata and data provenance rely on originators and datasets linked to the UK-SCAPE program; public sharing of underlying data is a consideration in data governance.
- Acknowledgements: supported by the Natural Environment Research Council (award NE/R016429/1) as part of UK-SCAPE.

## Acknowledgements and references
- References include key methodological papers and related UKCP18, MaRIUS, and G2G model literature that underpin the dataset’s development and usage.