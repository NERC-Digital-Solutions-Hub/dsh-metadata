# Soil Organic Carbon changes of agricultural land areas under different land use and climate scenarios till 2100, globally

## Overview
- Global dataset estimating changes in soil organic carbon (SOC) for agricultural lands under various management and climate scenarios up to 2100.
- SOC changes are expressed as Mg C per ha per year (average over 10-year periods) and shown as differences from a business-as-usual (BAU) baseline.
- BAU assumes continuous tillage, no residue incorporation, and no added organic amendments.
- Climate scenarios include A1B and A2; management changes include practices such as no tillage, reduced tillage, residue incorporation, cover crops, and manure additions.

## Data contents and structure
- Files and scenarios
  - Files represent different management changes and climate scenarios (e.g., crop_notill_A1B.txt, crop_residincorp_A2.txt, crop_covercrop_residincorp_redtill_A1B.txt, etc.).
  - Each file corresponds to a specific combination of management change and climate scenario.
- Data columns (as described in Table 2)
  - Geographic: latitude, longitude, area_km2
  - Land use: LU_agr_nrs_grid_cell (agricultural land use count per aggregated grid cell)
  - SOC changes by period: SOC_20_30_MgC_ha_yr, SOC_30_40_MgC_ha_yr, SOC_40_50_MgC_ha_yr, SOC_50_60_MgC_ha_yr, SOC_60_70_MgC_ha_yr, SOC_70_80_MgC_ha_yr, SOC_80_90_MgC_ha_yr, SOC_90_100_MgC_ha_yr (annual average 2020–2100, presented as difference to BAU)
- Outputs and calculations
  - Modelling results produced with ECOSSE (monthly SOC) on a 0.5-degree grid, using site-specific inputs (yields, fertiliser, sowing/harvest dates, tillage, residue incorporation).
  - SOC change relative to BAU: SOCCH [kg C yr^-1] = SOC_BAU [kg C yr^-1] – SOC_SC [kg C yr^-1].
  - Final datasets report 10-year averaged SOC changes.
  - Outputs include global, regional, and local statistics and visual mappings, validated against literature ranges.

## Modelling approach
- Model: ECOSSE, version 6.2b (monthly SOC dynamics) applied on a 0.5-degree grid with site-specific management inputs.
- Data processing: Outputs converted to annual totals in kg C per year; SOC changes compared to BAU to show the impact of alternative management and climate scenarios.
- Validation: Global, regional, and local statistics generated and compared with existing literature to ensure results fall within expected ranges.
- Data processing tools: R (version 4.3.0) used to compute annual SOC totals and summarize results.

## Data inputs and sources
- Climate data: Climate Research Unit (CRU), University of East Anglia
  - Source: https://www.uea.ac.uk/web/groups-and-centres/climatic-research-unit/data
- Soil data: Harmonized World Soil Database (HWSD)
  - Source: https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/harmonized-world-soildatabase-v12/en/
- Land use data: Hilda land use map (2019), cropland
  - Source: https://doi.pangaea.de/10.1594/PANGAEA.921846
- Land management data:
  - Fertiliser inputs: https://doi.pangaea.de/10.1594/PANGAEA.861203
  - Wheat yields: FAOSTAT (FAO)
  - Sowing and harvest dates: https://luh.umd.edu/data.shtml
  - Additional context: Globally available land for soil-based GHG removal (catalogue CEH)
  - Manure application reference: Gerber et al. 2016
- References (foundational studies and model descriptions)
  - Gerber et al. 2016; Smith et al. 2010a, 2010b

## Data use and interpretation for monitoring
- Purpose: Provide a basis to evaluate how different soil-management practices and climate trajectories could affect SOC stocks globally over the long term.
- Applications for policy and monitoring
  - Compare SOC outcomes under alternative management scenarios (e.g., tillage changes, residue management, cover crops, manure amendments).
  - Assess potential policy benefits for soil carbon sequestration relative to BAU.
  - Identify regional hotspots or vulnerabilities where SOC gains or losses are most pronounced.
  - Support scenario analysis and reporting for environmental health monitoring frameworks.

## Data quality, access, and governance considerations
- Metadata and data accessibility
  - The dataset relies on multiple source datasets (climate, soils, land use, management) and modelling outputs; users should review underlying metadata for each input source.
  - Sharing and re-use of model inputs and outputs are essential for transparency, though data provenance and versioning should be maintained.
- Data gaps and barriers
  - Potential data gaps or inconsistencies in metadata can hinder verification and reuse.
  - Transformation and integration of diverse data sources may require careful handling to preserve comparability.
- Governance and updates
  - Documented model assumptions (BAU baseline, management changes, climate scenarios) underpin the governance of the monitoring outputs.
  - Regular updates would require re-running ECOSSE with updated inputs and climate projections.

## References
- Gerber JS, Carlson KM, Makowski D, Mueller ND, Garcia de Cortazar-Atauri I, Havlík P, et al. (2016) Spatially explicit estimates of N2O emissions from croplands suggest climate mitigation opportunities from improved fertilizer management. Global Change Biology 22(10): 3383-3394.
- Smith J, Gottschalk P, Bellarby J, Chapman S, Lilly A, Towers W, et al. (2010a) Estimating changes in Scottish soil carbon stocks using ECOSSE. I. Model description and uncertainties. Clim Res 45: 179-192.
- Smith J, Gottschalk P, Bellarby J, Chapman S, Lilly A, Towers W, et al. (2010b) Estimating changes in Scottish soil carbon stocks using ECOSSE. II. Application. Clim Res 45: 193-205.