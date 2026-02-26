# The data set contains soil organic carbon (SOC) changes of agricultural land areas under different land use and climate scenarios till 2100, globally

## Aim and scope
- Global dataset of soil organic carbon changes on agricultural land under varying land-use practices and climate scenarios up to 2100.
- SOC changes are reported as differences from a BAU baseline (continuous tillage, no residue incorporation, no organic amendments).
- Outputs are annualized and averaged over 10-year periods (e.g., 2020–2030, 2030–2040, ..., 2090–2100) to support monitoring and policy evaluation.

## Data structure and content
- File set organized by management change and climate scenario (e.g., crop_notill_A1B.txt, crop_residincorp_A2.txt, crop_covercrop_residincorp_redtill_A1B.txt, etc.).
- Each file describes a specific management shift from BAU under a given climate scenario (A1B or A2).
- Table 2 header fields describe per-grid-cell data, including:
  - latitude, longitude
  - area_km2 (grid cell area)
  - LU_agr_nrs_grid_cell (agricultural land use per Hilda map)
  - SOC_20_30_MgC_ha_yr, SOC_30_40_MgC_ha_yr, ..., SOC_90_100_MgC_ha_yr (SOC change differences to BAU; annual average for the respective decade)
- All SOC change values are presented as differences to the BAU scenario and are averaged over 10-year periods.

## Modelling approach
- ECOSSE model (version 6.2b) used to simulate SOC dynamics on a monthly basis.
- Spatial application on a 0.5-degree grid; inputs include wheat yields, fertiliser inputs, sowing/harvesting dates, and soil management (tillage, residue incorporation).
- Outputs processed in R (R 4.3.0) to calculate annual SOC totals and SOC change relative to BAU:
  - SOCCH [kg C yr-1] = SOC_BAU [kg C yr-1] − SOC_SC [kg C yr-1]
- SOC changes are averaged over 10-year periods and mapped; global, regional, and local statistics are computed for validation against literature.

## Data inputs and sources
- Climate data: Climate Research Unit (CRU) from the University of East Anglia.
- Soil data: Harmonized World Soil Database (HWSD).
- Land use data: HILDA land use map (2019) for cropland identification.
- Fertiliser inputs: PANGAEA dataset.
- Yields: FAOSTAT (national statistics for wheat).
- Sowing and harvest dates:LUH-UMD data.
- Manure application: Gerber et al. (2016).
- References for model and methodology include Smith et al. (2010) and Gerber et al. (2016).

## Outputs and formats
- Model results expressed as SOC change relative to BAU for decadal periods, mapped and quality-checked.
- Data files are in text format with fields for location, land use, and SOC change values (kg C yr-1) across decades.
- The dataset includes explicit documentation in Tables 1 and 2 describing each file and header contents.

## Quality assurance and validation
- Outputs are visually screened and mapped; global/regional/local statistics are compared with existing literature to ensure consistency with predicted SOC changes.
- All results are derived from a standardized modelling workflow and documented data inputs.

## Relevance for monitoring and policy
- Provides a standardized, comparable framework to monitor soil carbon responses to management changes and climate scenarios over time.
- Facilitates assessment of environmental health and policy performance related to soil carbon sequestration and soil management practices.
- The clearly defined BAU baseline and multiple management scenarios enable trend analysis and scenario comparison.

## Access and reuse considerations
- Data are organized by scenario and management change, with explicit documentation of file contents (Tables 1 and 2 in the source).
- Underlying data sources (climate, soils, land use, yields, fertilisers) come from established public datasets, enabling integration with other environmental indicators.