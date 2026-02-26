# The data set contains soil organic carbon (SOC) changes of agricultural land areas under different land use and climate scenarios till 2100, globally.

## Overview
- Global dataset of SOC changes on agricultural land under various land-use and climate scenarios up to 2100.
- SOC changes are given as annual averages (Mg C ha-1 yr-1) for sequential decades (2020–2030, 2030–2040, ..., 2090–2100) and are presented as differences to a BAU baseline.
- BAU baseline assumes continuous tillage, no residue incorporation, and no added organic amendments.
- Outputs are designed to enable comparison of management scenarios (e.g., notill, reduced tillage, residue incorporation, cover crops, manure amendments) under different climate futures (A1B, A2).

## Data structure and files
- Multiple scenario-specific files (example names):
  - crop_notill_A1B.txt, crop_notill_A2.txt
  - crop_notill_residincorp_A1B.txt, crop_notill_residincorp_A2.txt
  - crop_redtill_A1B.txt, crop_redtill_A2.txt
  - crop_residincorp_A1B.txt, crop_residincorp_A2.txt
  - crop_covercrop_A1B.txt, crop_covercrop_A2.txt
  - crop_covercrop_residincorp_A1B.txt, crop_covercrop_residincorp_A2.txt
  - crop_covercrop_residincorp_redtill_A1B.txt, crop_covercrop_residincorp_redtill_A2.txt
  - crop_manure_A1B.txt, crop_manure_A2.txt
- Table 2 describes the data columns within each file: 
  - latitude, longitude
  - area_km2 (grid cell size)
  - LU_agr_nrs_grid_cell (agricultural land-use classification)
  - SOC_20_30_MgC_ha_yr … SOC_90_100_MgC_ha_yr (SOC change in Mg C ha-1 yr-1, difference to BAU; annual average for each decade)
- SOC columns are the difference to BAU (SOC_CH) and are reported as decade-averaged values from 2020 to 2100.
- Spatial resolution is 0.5 degree grid cells.

## Modelling approach
- ECOSSE model (version 6.2b) used to simulate SOC on a monthly basis.
- Runs at grid-cell level with site-specific inputs: crop yields (wheat), fertiliser inputs, sowing/harvesting dates, and soil management (tillage, residue practices).
- Spatial ECOSSE outputs are transformed into grid-specific SOC time series up to 2100.
- SOC changes for each scenario are calculated as SOC_CH = SOC_BAU – SOC_SC.
- Results are mapped, visually screened, and summarized with global, regional, and local statistics; cross-validated against literature ranges.

## Data inputs and sources
- Climate data: Climate Research Unit (CRU) data from the University of East Anglia (UEA).
- Soil data: Harmonized World Soil Database (HWSD).
- Land use data: Hilda global land-use map (2019) for cropland.
- Land management data: fertiliser inputs; wheat yields (FAOSTAT); sowing and harvest dates (various sources including LUH and other datasets).
- Manure application data: Gerber et al. (2016) dataset.
- References for modelling and methodology include:
  - Gerber et al. 2016 (N2O emissions and fertilizer management)
  - Smith et al. 2010a, 2010b (ECOSSE model descriptions and applications)

## Outputs and interpretation
- For each grid cell and scenario, SOC changes are provided as decade-averaged annual SOC differences relative to BAU (SOC_CH) for 2020–2100.
- Columns include SOC_20_30_MgC_ha_yr through SOC_90_100_MgC_ha_yr, representing 2020–2030 up to 2090–2100.
- The dataset enables identification of regions and management practices that increase or reduce SOC relative to BAU, under different climate futures.

## Validation and quality checks
- Model results were mapped and visually screened.
- Global, regional, and local statistics were calculated and compared with existing literature to ensure results fall within plausible ranges.

## Usage and applications for data support
- Data Support archetype can:
  - Understand the impact of different soil management practices on SOC under climate scenarios.
  - Combine with other data sources to assess policy-relevant outcomes (e.g., climate mitigation opportunities from soil carbon management).
  - Create dashboards or reports to enable self-service exploration of SOC changes by region, decade, and management practice.
  - Identify hotspots of SOC gain or loss and inform policy or planning at local to global scales.
  - Communicate complex SOC results simply by focusing on BAU vs scenario differences across decades.

## References
- Gerber JS, Carlson KM, Makowski D, Mueller ND, Garcia de Cortazar-Atauri I, Havlík P, et al. (2016). Spatially explicit estimates of N2O emissions from croplands suggest climate mitigation opportunities from improved fertilizer management. Global Change Biology.
- Smith J, Gottschalk P, Bellarby J, Chapman S, Lilly A, Towers W, et al. (2010a, 2010b). Estimating changes in Scottish soil carbon stocks using ECOSSE. Clim Res.