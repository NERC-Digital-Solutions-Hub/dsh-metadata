# Supporting information for Grid-to-Grid model estimates of river flow for Northern Ireland driven by observed data (1980 to 2011)

## Purpose and scope
- Provide grid-to-grid (G2G) hydrological model estimates of natural river flows for Northern Ireland (NI) driven by observed meteorological data.
- Outputs cover:
  - Monthly mean river flow (m3 s-1)
  - Annual maxima of daily mean river flow (m3 s-1)
  - Annual minima of 7-day mean river flow (m3 s-1)
- Spatial and temporal coverage:
  - 1 km x 1 km grid across NI
  - Time period: 1980–2011 (water years and monthly alignment as specified)
- Data are designed to support comparisons with observed NRFA data and with datasets driven by UKCP18 regional climate projections.

## Dataset context and components
- Part of UK-SCAPE programme (UK Status, Change And Projections of the Environment).
- Work Package 2 focuses on climate-change impacts on water quantity, providing NI-specific G2G outputs and complementary datasets for GB.
- Additional spatial datasets provided to aid interpretation:
  - Digitally-derived catchment areas on a 1 km grid
  - Majority lake cells grid (1 km)
  - Estimated locations of flow gauging stations on a 1 km grid (NRFA-compatible)
- Related NI and GB datasets exist for cross-region analysis (e.g., NI flows under UKCP18 projections).

## Model and inputs
- Model: Grid-to-Grid (G2G) hydrological model (1 km grid; 15-minute time-step), configured for NI and adjacent catchments draining to NI rivers.
- Key characteristics:
  - Outputs natural river flows for gauged and ungauged rivers.
  - Prefers gridded data over local calibration; uses broadly applicable parameter values where needed.
  - Urban/sub-urban land-cover effects represented; lake/reservoir impacts not explicitly modelled (lake cells treated as rivers).
  - Calibration not performed for individual catchments; performance generally good for natural-flow regimes; caveats where regulation or complex subsurface hydrology prevail.
- Required inputs:
  - Precipitation: daily 1 km grids (CEH-GEAR)
  - Potential evaporation: monthly 40 km grids (MORECS)
  - Temperature: daily min/max grids (Met Office) for optional snow module
- Data handling:
  - Precip and PE re-projected to the GB 1 km grid; temporal downscaling and infilling applied where coverage is incomplete.
  - Additional land and soil data used to configure the model follow established references.

## Data formats and structure
- Gridded outputs stored as NetCDF4 files, one per variable:
  - Monthly mean river flow: G2G_NI_mmflow_obs_1980_2011.nc
  - Annual maxima of daily mean river flow: G2G_NI_amaxflow_obs_1980_2011.nc
  - Annual minima of 7-day mean river flow: G2G_NI_aminflow_obs_1980_2011.nc
- Domain and resolution:
  - NI dataset on a 1 km x 1 km grid, within a NI-specific spatial domain on the GB National Grid.
  - Non-tidal river cells with catchment area >= 50 km2 are included; others are set to missing (-9999).
- Time conventions:
  - Monthly means assigned to the first day of each month.
  - Annual maxima/minima aligned to the start of the corresponding 12-month period (water-year definitions noted in documentation).
- Supporting files:
  - Catchment area grid (km2) for each 1 km cell
  - Lake grid identifying majority lake cells
  - NRFA gauging station locations grid and CSV, to facilitate comparison with observed data
- Data quality and caveats:
  - Lakes/reservoirs not explicitly modeled; lake storage effects on downstream flows are neglected in the NI G2G outputs.
  - Some NRFA catchment areas may differ from discretised 1 km grid catchments, especially for smaller basins.
  - Acknowledge potential discrepancies with observed NRFA data due to grid-scale representation and data sources.

## How to use the datasets
- Baseline comparisons:
  - Compare G2G NI outputs with observed NRFA river flows (e.g., from NRFA database).
  - Analyze alongside parallel dataset of flows driven by UKCP18 Regional (12 km) climate projections.
- Data interpretation and caveats:
  - Recognize non-accounted lake regulation effects; interpret outputs as natural-flow estimates.
  - Consider potential misalignment between NRFA catchments and the 1 km G2G grid cells, particularly for smaller catchments.
- Data governance and stewardship:
  - Documented metadata and file conventions support discoverability and reuse within data-sharing networks and across partner organizations.

## Accessibility and references
- Acknowledgements:
  - Funded by Natural Environment Research Council (NE/R016429/1) under UK-SCAPE National Capability.
- References for model inputs and performance:
  - Bell et al. (2009, 2016), Davies and Bell (2009), Kay et al. (2021), Rudd et al. (2017), Formetta et al. (2018), Hough and Jones (1997), Met Office HadUK-Grid data (2019), Rowland et al. (2017), Tanguy et al. (2016).
- Related dataset links and DOIs provided in the dataset documentation for broader context and cross-comparisons.