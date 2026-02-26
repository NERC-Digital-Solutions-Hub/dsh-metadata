# GWAVA Modelling- SUNRISE1.5

## Overview
- GWAVA is a large-scale, semidistributed gridded water resources model developed by the UK Centre for Ecology & Hydrology.
- It integrates natural hydrological processes with anthropogenic demands to estimate local runoff and water use.
- Spatial scope: Upper Narmada Basin (0.125 degree grid); 318 cells for Upper Narmada and 653 cells for the whole Narmada.
- Core components: soil moisture storage, surface storage, groundwater storage, plus a demand-driven routine for domestic, industrial, and agricultural stresses.
- Demands are modeled as:
  - Domestic and livestock (user-defined and temporally static but spatially dynamic)
  - Irrigation (temporally and spatially dynamic, crop-type and planting month dependent)
- Outputs support policy and management with data on reservoirs, transfers, and agriculture within command and rural areas.

## Model Setup
- Integrated with the Global Water Availability Assessment (GWAVA) Version 5.0.
- Includes large-scale, semidistributed modelling with a lumped probability-distributed model (PDM) for runoff.
- Calibration and validation performed at sub-catchments and groundwater wells to assess performance.
- Validation framework and performance metric:
  - Kling-Gupta Efficiency (KGE) values reported for calibration and validation across multiple sub-catchments.

## Future Projections
- Ensemble climate dataset used to represent future climate for GWAVA runs.
- Climate model families included (e.g., ACCESS, BCC, CanESM, CESM, CNRM, CSIRO, GFDL, IPSL, MIROC, MPI, MRI, NorESM) across multiple modelling centers.
- Scenarios and periods covered:
  - Baseline/historical data and future projections under RCP4.5 and RCP8.5.
  - Specific future datasets span various time windows including 2028–2060 and 2021–2099, with daily totQ and other climate-driven variables.
- Outputs include total runoff (totQ) and climate-driven variants for aquifer levels and water demands under different RCPs.

## Quality Control
- Calibration at 13 gauging stations; used SIMPLEX auto-calibration with four parameters (surface and groundwater routing, PDM soil-moisture parameter, and rooting depth multiplier).
- Validation performed on the same 13 stations plus 100 groundwater wells.
- Model performance summarized by KGE values per sub-catchment, with calibration and validation results indicating generally good fit, though some sub-catchments show lower performance (range across sub-catchments from approximately 0.32 to 0.86).

## Data Structure and Files
- Data are organized into twelve CSV files, covering baseline, climate, and Paddy-crop scenarios.
- Baseline datasets (daily scale, 1981–2013):
  - Narmada_Baseline_1981_2013.csv: totQ, aquifer level (aqlevel), and various demand components (urban/rural, livestock, industrial, irrigation) and unfulfilled demand fields.
  - Narmada_Paddy_1981_2013.csv: baseline with Paddy crop adjustments (note: referenced as having a source error in the listing).
  - Upper_Narmada_Baseline_1970_2013.csv: total runoff for the Upper Narmada with daily scale data.
- Climate and scenario datasets:
  - Upper_Narmada_Climate_2028_2060.csv: totQ outputs for climate-modelled future period.
  - Narmada_climate_45_totQ_2021_2099.csv and Narmada_climate_85_totQ_2021_2099.csv: total runoff under RCP4.5 and RCP8.5, respectively, for 2021–2099 (daily, per grid cell).
  - Narmada_climate_paddy_45_totQ_2021_2099.csv and Narmada_climate_paddy_85_totQ_2021_2099.csv: same as above but with Paddy replacing wheat in future periods.
  - Narmada_climate_paddy_45_aqlevel_2021_2099.csv and Narmada_climate_paddy_85_aqlevel_2021_2099.csv: aquifer level outputs under Paddy-crop scenarios for 2021–2099.
  - Narmada_climate_45_aqlevel_2021_2099.csv and Narmada_climate_85_aqlevel_2021_2099.csv: aquifer level outputs under standard (non-paddy) scenarios for 2021–2099.
- File naming convention indicates grid-cell mean values (xll, yll coordinates, year, Julian day) and model-specific totQ or aqlevel values for each climate model and scenario combination.
- Notes:
  - Several datasets distinguish between baseline, climate projections (2028–2060; 2021–2099), RCP4.5 and RCP8.5, and Paddy-crop substitutions.
  - Data files include multiple model identifiers (e.g., ACCESS, BCC, CanESM, EC-Earth, INM, MPI, NorESM, etc.) corresponding to the respective climate model outputs.

## Acknowledgements
- Acknowledges CMIP6 and the World Climate Research Programme, the ESGF for data access and archiving, and supporting funding agencies.