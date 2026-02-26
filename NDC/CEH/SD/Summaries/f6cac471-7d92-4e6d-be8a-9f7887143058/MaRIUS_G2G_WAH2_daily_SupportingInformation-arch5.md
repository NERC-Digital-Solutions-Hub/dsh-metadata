# Supporting information for Grid-to-Grid model estimates of daily mean river flow for gauged catchments in Great Britain: weather@home2 (climate model) driving data [MaRIUS-G2G-WAH2-daily]

## Overview
- MaRIUS (Managing the Risks, Impacts and Uncertainties of drought and water Scarcity) was a UK NERC-funded project (2014–2017) that developed a risk-based approach to drought and water scarcity.
- The MaRIUS-G2G-WAH2-daily dataset provides Grid-to-Grid (G2G) model estimates of daily mean river flow for 260 NRFA gauging stations across Great Britain.
- Key output variable: river flow (m3 s-1), daily mean (midnight–midnight) for historical (1900–2006), near-future (2020–2049), and far-future (2070–2099) periods.
- Driving data come from the MaRIUS weather@home2 (WAH2) regional climate model (RCM) dataset, which provides ensembles of historical and future climates to generate matching hydrological simulations.
- 100 ensemble members per period; four periods: HISTBS (1900–2006), BS (baseline 1975–2004), NF (2020–2049), FF (2070–2099).

## Data model and method
- Hydrological model: Grid-to-Grid (G2G) national-scale model for Great Britain, 1 km × 1 km grid, 15-minute time-step; includes urban/suburban runoff effects; calibrated primarily with spatial data rather than catchment-by-catchment calibration.
- Inputs: precipitation and potential evaporation (PE) from the MaRIUS WAH2 dataset. Snow module not used; precipitation treated as rain.
- Bias correction: applied to precipitation using a monthly multiplicative scheme; PE not bias-corrected.
- PE calculations: Penman–Monteith scheme; historical period uses stomatal resistance values from MORECS; future periods use adjusted rs values to account for CO2 effects.
- Re-projection: WAH2 data re-projected from 0.22° grid to 1 km × 1 km G2G grid; non-uniform precipitation distribution within each RCM box via spatial weights.
- Time periods and ensembles:
  - HISTBS: 1900–2006 (spin-up for first two years in analyses)
  - BS: 1975–2004 (baseline)
  - NF: 2020–2049 (near-future)
  - FF: 2070–2099 (far-future)
  - 100 ensemble members for each period; ensemble numbers are not meant to be compared across periods.
- Output scope: daily mean natural flows (m3 s-1) for 260 NRFA gauging stations; flows correspond to the 1 km grid cell closest to each NRFA station and validated to represent the correct contributing catchment (within ~8% of NRFA catchment areas on average).

## Data format and storage
- Format: CSV files, one per catchment; 30-day months due to the 360-day calendar of the climate model.
- Structure: each file has a single header row; first column is date, followed by 100 ensemble columns (1–100).
- Filenames:
  - Historical Baseline: G2G_WAH2_flow_HISTBS_*.csv (1900–2006; with spin-up years 1900–1901)
  - Baseline: G2G_WAH2_flow_BS_*.csv (1975–2004)
  - Near-Future: G2G_WAH2_flow_NF_*.csv (2020–2049; 2020–2021 spin-up)
  - Far-Future: G2G_WAH2_flow_FF_*.csv (2070–2099; 2070–2071 spin-up)
- Supporting metadata: MaRIUS_NRFAStationInfo.csv provides station details for the 260 NRFA gauging stations, including station ID, river name, location, G2G coordinates, catchment area, and data issues.

## Usage, interpretation, and governance
- Comparisons and benchmarking:
  - Compare G2G flows driven by WAH2 to observation-based G2G runs or NRFA observations only at a statistical level (not time-series level) due to biases and model structure.
  - For historical vs future analyses, compare distributions (differences in statistics) rather than individual ensemble members.
  - Do not directly pair ensemble member numbers across periods (e.g., BS1 with NF1).
  - For impacts analyses (economic, ecological, agricultural), interpret differences relative to the Baseline (BS) rather than to observed real-world time series.
- Spatial considerations:
  - Each NRFA station is represented by the closest matching 1 km G2G grid cell; occasional mismatches in the corresponding catchment area may occur, particularly for small catchments (typical discrepancy within 8%).
- Spin-up guidance:
  - First two years of HISTBS, NF, and FF should be treated as spin-up and not used for analysis unless explicitly intended for spin-up purposes.
- Data provenance and quality:
  - Data are produced under the MaRIUS project (funded by UK NE/NERC) with documented methodological choices (bias correction, PE treatment, CO2 adjustments, re-projection).
  - Documentation and references provide traceability for modelling approaches and data processing steps.

## Provenance, access, and references
- Provenance: MaRIUS project outputs, UK NERC funding (NE/L010208/1); part of the UK Drought and Water Scarcity programme.
- Access and documentation:
  - Data hosted in the NERC Environmental Information Data Centre (EIDC) and related CEH catalog entries.
  - Related methodological and validation references listed (e.g., Bell et al. 2007, 2009, 2016; Guillod et al. 2018; Kay et al. 2018; Rudd et al. 2017; Monteith 1965; MORECS references).
- Acknowledgements: thanks to individuals and teams contributing to data availability.