# Soil organic carbon changes of agricultural land areas under different land use and climate scenarios till 2100

## Scope and key metric
- Global dataset tracking soil organic carbon (SOC) changes on agricultural land under various land-use and climate scenarios up to 2100.
- SOC changes are reported as Mg C ha^-1 yr^-1 and presented as the average over 10-year periods.
- Baseline scenario (BAU) represents continuous tillage, no residue incorporation, and no added organic amendments.
- Outputs express SOC change relative to BAU (SOC_CH = SOC_BAU - SOC_SC).

## Modelling approach
- Modelling tool: ECOSSE, version 6.2b, run on a monthly timescale with a 0.5-degree grid.
- Site-specific inputs include:
  - Crop yields (wheat)
  - Fertiliser inputs
  - Sowing and harvesting dates
  - Soil management details (tillage practices, residue incorporation)
- Spatially explicit input files are generated per grid cell; ECOSSE runs to 2100.
- Data processing in R (v4.x): annual SOC totals converted to kilograms C per year; SOC change per scenario computed against BAU.
- Outputs are mapped and screened; global, regional, and local statistics are calculated and compared with literature to validate ranges.

## Data files and structure
- Table 1: Files represent different management changes from BAU under specific climate scenarios (A1B or A2), including:
  - crop_notill, crop_residincorp, crop_redtill, crop_covercrop, crop_covercrop_residincorp, crop_covercrop_residincorp_redtill, crop_manure, and combinations thereof.
- Table 2: File content and headers describe grid-cell attributes and SOC change bands:
  - Latitude/Longitude, area_km2
  - LU_agr_nrs_grid_cell (agricultural land use per 0.01° grid, aggregated)
  - SOC_20_30_MgC_ha_yr through SOC_90_100_MgC_ha_yr: SOC change relative to BAU, annual average for 2020–2100, stored as decade-wide averages.
  
## Data inputs and sources
- Climate data: Climate Research Unit (CRU) data from University of East Anglia (UEA).
- Soil data: Harmonized World Soil Database (HWSD).
- Land use data: HILDA land use map (2019) for cropland identification.
- Fertiliser inputs: PANGAEA dataset.
- Yields: FAOSTAT (country/region-level wheat yields).
- Sowing and harvest dates: LUH/UMD data resource.
- Additional reference datasets:
  - Globally available land for soil-based GHG removal (2000–2014)
  - Manure application: Gerber et al. 2016.

## Outputs and data processing
- SOC outputs are calculated as annual totals (kg C yr^-1) and compared to BAU to yield SOC_CH.
- Results are averaged across 10-year periods (e.g., 2020–2030, 2030–2040, etc.) per grid cell.
- Quality checks include visual mapping and comparison with published ranges to ensure plausibility.

## Data use and interpretation
- Analysts can use the dataset to:
  - Identify correlations between management changes (e.g., tillage, residue incorporation, cover crops, manure) and SOC changes under different climate trajectories (A1B, A2).
  - Quantify potential SOC sequestration or emissions reductions associated with specific agronomic practices.
  - Assess regional and global patterns in SOC response to management under future climate scenarios.
- The dataset supports scenario analysis for policy and decision-making related to soil carbon management and climate mitigation.

## Accessibility, provenance, and quality assurance
- Outputs are mapped and subjected to statistical and literature-based validation to align with expected ranges.
- Datasets are documented with metadata and can be uploaded to data portals to ensure discoverability and reuse.
- Provenance traces back to ECOSSE model inputs (yields, fertilisers, sowing/harvest), soil, climate, and land-use data sources, ensuring reproducibility.

## Considerations and caveats
- BAU assumptions (continuous tillage, no residues, no organic amendments) may influence SOC baseline and inferred benefits of practices.
- Spatial resolution (0.5-degree grid) and global input datasets introduce uncertainties; interpretation should consider model and data limitations.
- While extensive, the data are model-generated projections and should be integrated with other socio-economic and policy analyses for comprehensive decision-making.