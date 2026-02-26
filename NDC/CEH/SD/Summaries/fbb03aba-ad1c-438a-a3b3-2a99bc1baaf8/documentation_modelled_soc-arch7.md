# General description

- Global dataset of soil organic carbon (SOC) changes on agricultural land under different land-use and climate scenarios up to 2100.
- SOC changes are reported as annual Mg C ha-1 yr-1 differences relative to a BAU baseline (continuous tillage, no residue incorporation, no organic amendments) and averaged over 10-year periods.
- Modelling uses a spatial version of ECOSSE (Estimating Carbon in Organic Soils Sequestration and Emissions), with monthly simulations on a grid.

## Data structure and variables

- Outputs are provided per grid cell with the following fields:
  - latitude, longitude: location of grid cell
  - area_km2: size of grid cell
  - LU_agr_nrs_grid_cell: agricultural land use per aggregated grid cell (based on the Hilda map; up to 2500 sub-cells of 0.01° each)
  - SOC_20_30_MgC_ha_yr … SOC_90_100_MgC_ha_yr: SOC changes (difference to BAU) for 2020–2030 through 2090–2100, in Mg C ha-1 yr-1, averaged annually within each 10-year window
- File naming conventions reflect management changes and climate scenarios (e.g., crop_notill_A1B.txt, crop_residincorp_A2.txt, crop_covercrop_residincorp_A1B.txt).
- Table 2 describes the header contents, including a grid- and scenario-specific structure.

## Modelling approach

- ECOSSE model, version 6.2b, run at 0.5-degree grid scale with site-specific inputs (crop yields, fertiliser inputs, sowing/harvesting dates, tillage and residue practices).
- Spatial ECOSSE runs generate grid-specific input files; SOC changes are computed against the BAU scenario.
- Outputs processed in R (R 4.3.0) to obtain annual SOC totals (kg C yr-1) and SOCCH = SOCBAU − SOCSC.
- Results are mapped and visually screened; global, regional, and local statistics are calculated for validation against literature.

## Scenarios and data coverage

- Climate scenarios: A1B and A2.
- Management changes (relative to BAU): 
  - no tillage (notill)
  - reduced tillage (redtill)
  - residue incorporation (residincorp)
  - use of cover crops (covercrop)
  - addition of organic amendments (manure)
- Combinations include: 
  - notill with residue incorporation, cover crops with residue incorporation, reduced tillage with cover crops and residue incorporation, etc.
- Each file provides SOC changes under a specific management change and climate scenario, averaged over 2020–2100 in 10-year periods.

## Data inputs and sources

- Climate data: Climate Research Unit (CRU) data from the University of East Anglia.
- Soil data: HWSD – Harmonized World Soil Database.
- Land use data: Global Hilda land use map (2019) for cropland delineation.
- Fertiliser inputs: Pangaea dataset.
- Crop yields: FAOSTAT (national/ regional statistics).
- Sowing and harvesting dates: LUH/UMD data sources.
- Additional context: Globally available land for soil-based GHG removal practices (CEH), manure application reference (Gerber et al. 2016).

## Spatial resolution and data packaging

- Modelling grid: 0.5-degree grid for ECOSSE simulations.
- Input data at finer 0.01° sub-grid resolution aggregated into the 0.5-degree grid (LU_agr_nrs_grid_cell describes the number of 0.01° cells per aggregated grid cell; max 2500).
- Outputs provide 10-year averaged SOC changes, enabling map-based visualisation and comparison across regions and scenarios.

## GIS usage and considerations

- Designed for map-based data products to help audiences understand SOC responses to management and climate scenarios.
- Suitable for creating thematic maps of SOC change, hotspot identification, and scenario comparison.
- Important to acknowledge data challenges typical for GIS work: multiple data sources, varying resolutions, and the need to harmonise standards across data layers.

## Quality assurance and validation

- Model results are visually screened and statistically compared with existing literature to ensure plausibility and alignment with published ranges.
- Global, regional, and local statistics are produced to assess model outcomes.

## References

- Gerber et al. (2016) on N2O emissions and fertilizer management.
- Smith et al. (2010a, 2010b) on ECOSSE model descriptions and applications.