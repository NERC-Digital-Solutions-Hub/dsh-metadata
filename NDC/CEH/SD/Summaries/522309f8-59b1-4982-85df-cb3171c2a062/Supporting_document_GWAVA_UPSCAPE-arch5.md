# GWAVA Modelling- UPSCAPE

## Overview

- The GWAVA model (Global Water Availability Assessment) version 5.0 is a large-scale, semi-distributed gridded water resources model developed by the UK Centre for Ecology & Hydrology. It estimates local runoff using a lumped probabilistic soil moisture storage, surface storage, and groundwater storage framework, followed by a demand-driven routine to account for anthropogenic stresses.
- The Cauvery Basin was modeled at 0.125-degree resolution (444 modelling cells) and includes domestic, irrigation, industrial, and livestock water demands, major transfers, reservoirs, and agricultural areas.
- Outputs include ensemble climate data and socio-economic pathways to represent future climate and demand scenarios.

## Data content and structure

- Data are provided as seven CSV files with a consistent schema.
- Each file’s first four columns are:
  - xll: x coordinate of the lower left corner of the modelling grid square
  - yll: y coordinate of the lower left corner of the modelling grid square
  - year: calendar year
  - timestep: Julian day (1-366)
- Files and their contents:
  - Baseline_1986_2005.csv: baseline variables (Table 2) at a daily scale
  - Ensemble_climate_2041_2060.csv: ensemble climate for 2041-2060 under RCP4.5 and RCP8.5
  - Ensemble_climate_2061_2080.csv: ensemble climate for 2061-2080 under RCP4.5 and RCP8.5
  - SSPs_2041_2060.csv: socio-economic pathways SSP1, SSP2, SSP3 for 2041-2060
  - SSPs_2061_2080.csv: socio-economic pathways SSP1, SSP2, SSP3 for 2061-2080
  - Ensemble_climate_SSPs_2041_2060.csv: combinations of RCPs with SSPs for 2041-2060
  - Ensemble_climate_SSPs_2061_2080.csv: combinations of RCPs with SSPs for 2061-2080
- Variables (Table 2) include:
  - Total runoff (totQ, m3/s)
  - Aquifer level (aqlevel, m below ground level)
  - Domestic, rural domestic, livestock, industrial, irrigation demands (e.g., urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems) with corresponding unfulfilled demand counterparts (uf_*)
  - All values are means over the grid box and the day

## Temporal and scenario coverage

- Baseline period: 1986–2005 (daily scale)
- Future scenarios:
  - Ensemble climate data for 2041–2060 and 2061–2080 under RCP4.5 and RCP8.5
  - Socio-economic pathways: SSP1, SSP2, SSP3 for 2041–2060 and 2061–2080
  - Combined ensembles: ensembles of climate with SSPs for the respective periods

## Quality control and validation

- Model calibration at 14 gauging stations across the basin using the SIMPLEX auto-calibration routine, varying four parameters (surface and groundwater routing; PDM soil moisture capacity; rooting depth multiplier).
- Validation performed on the same 14 gauges (and 200 groundwater wells) using different time periods.
- Performance is reported as Kling-Gupta Efficiency (KGE) values (Table 3):
  - Examples include calibration KGE values ranging from 0.24 to 0.82 and validation KGE values from 0.16 to 0.68 for various sites; some validation KPGE values are negative (e.g., -1.27) in certain periods.
- These results indicate varying model performance across sites and periods, with generally higher calibration performance and more variable validation performance.

## Data provenance and modeling context

- GWAVA 5.0 configuration includes:
  - A probabilistic soil moisture component, surface storage, groundwater storage, and a demand-driven anthropogenic routine.
  - Disaggregation of the Cauvery Basin into 444 cells at 0.125-degree resolution.
  - Household (urban/rural) domestic demand, irrigation demand (crop-type and planting month), and other sectoral demands (industrial, livestock).
- Climate and socio-economic inputs come from multiple external sources:
  - Climate models: BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M
  - Scenarios: Shared Socio-economic Pathways (SSP1, SSP2, SSP3) and Representative Concentration Pathways (RCP4.5, RCP8.5)
  - Data provenance and acknowledgments reference CMIP and related modeling groups, with coordination and software infrastructure support noted.

## Data organization and access

- Data are organized for easy ingestion in GIS/analysis workflows:
  - Daily time-series data for each grid cell and variable, aligned to calendar year and Julian day
  - Baseline and future scenario partitions are clearly separated into respective CSV files
- Metadata and supporting documentation are provided, including variable descriptions, units, and data structure definitions to support proper interpretation and reuse.

## Governance considerations and caveats for data stewards

- Versioning and provenance:
  - Model version (GWAVA 5.0) and the specific basin configuration should be tracked for reproducibility.
  - Clear documentation of baseline vs. future scenario files and the scenario combinations used is essential.
- Metadata and interoperability:
  - Ensure consistent variable naming, units (m3/s for demands and runoff; meters for aquifer level), and daily aggregation conventions across files.
  - Maintain thorough metadata to support discovery, including spatial resolution (0.125-degree grid), grid cell indexing, and time coverage.
- Data volume and storage:
  - The daily, grid-based ensemble outputs across multiple scenarios generate large datasets; plan for scalable storage and efficient access.
- Quality and limitations:
  - Acknowledge variability in model validation performance across sites and time periods; include caveats about interpretability of certain outputs, particularly where validation metrics are low or negative.
- Citation and acknowledgments:
  - Cite GWAVA v5.0 outputs appropriately and acknowledge CMIP and climate modeling groups as per the document’s acknowledgments.
- Update and governance:
  - Establish processes for updating datasets with new model runs or improved calibrations, and ensure update histories are recorded.

## Acknowledgements

- Recognizes CMIP and the climate modeling groups for model outputs; notes support from the U.S. Department of Energy’s Program for Climate Model Diagnosis and Intercomparison and related software infrastructure developments.