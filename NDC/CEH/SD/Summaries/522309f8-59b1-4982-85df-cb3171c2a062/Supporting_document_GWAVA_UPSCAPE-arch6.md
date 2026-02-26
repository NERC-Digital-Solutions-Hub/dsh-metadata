# GWAVA Modelling- UPSCAPE

- The GWAVA (Global Water Availability Assessment) Model 5.0 is a large-scale, semi-distributed gridded water resources model developed by the UK Centre for Ecology & Hydrology.
- Purpose: estimate local runoff and account for anthropogenic water demands to assess water availability and use.
- Domain and resolution: Cauvery Basin modeled at 0.125-degree resolution, disaggregated into 444 grid cells.
- Core approach: uses a lumped probability distribution model (PDM) for runoff with three components—soil moisture storage, surface storage, and groundwater storage—plus a demand-driven routine to represent domestic, industrial, agricultural, and livestock water stresses, including irrigation with crop-type and planting-month dynamics.
- Outputs are designed for end-user self-service via dashboards, reports, or charts, with potential for sharing early prototypes and promoting better data creation.

## Data generation and model setup

- Model name and version: GWAVA Model 5.0.
- Implementation: integrates natural processes and anthropogenic factors to produce daily, grid-mean values for the Cauvery Basin.
- Demands modeled: domestic (urban and rural), industrial, and livestock; irrigation demand is dynamic with crop type and planting schedule.
- Data coverage: includes large-scale water transfers, reservoirs (major and minor), and agricultural areas within command and rural zones.

## Climate scenarios and projections

- Ensemble climate dataset used to represent future climate for GWAVA runs.
- Climate models included: BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M.
- Socio-economic pathways: SSP1 (SDG-focused, low material growth), SSP2 (business-as-usual), SSP3 (sector-centric policies, rapid population growth, environmental degradation).
- Scenarios/time windows:
  - Baseline: 1986–2005.
  - Ensemble climate scenarios for 2041–2060 and 2061–2080 under RCP4.5 and RCP8.5.
  - SSPs for 2041–2060 and 2061–2080.
  - Combined ensemble scenarios (SSP-RCPs) for 2041–2060 and 2061–2080.
- Data labeling:
  - BL = Baseline (1985–2005)
  - ENA = Ensemble climate
  - SSP = Socio-economic Pathway
  - RCP = Representative Concentration Pathway

## Variables and units (Table overview)

- TotQ: Total runoff; Units = m3/s; description: runoff from land to rivers; daily grid-mean values.
- Aquifer level: aqlevel; Units = meters below ground level; daily grid-mean values.
- Urban domestic demand: urban_dems; Units = m3/s; domestic demand for urban population.
- Rural domestic demand: rural_dems; Units = m3/s; domestic demand for rural population and livestock.
- Livestock demand: livestock_dems; Units = m3/s; livestock water demand.
- Industrial demand: industrial_dems; Units = m3/s; industrial water demand.
- Irrigation demand: irrigation_dems; Units = m3/s; irrigation demand (includes irrigation efficiency).
- Unfulfilled demands: various uf_* variables (e.g., uf_urban_dems, uf_rural_dems, uf_livestock_dems, uf_industrial_dems, uf_irrigation_dems); daily grid-mean values indicating unmet demand.
- Descriptions are provided for each variable and are presented daily for each grid cell.

## Data quality and validation

- Calibration: performed at 14 gauging stations using SIMPLEX auto-calibration (four parameters: surface/groundwater routing, PDM soil-moisture variation, rooting-depth multiplier).
- Validation: applied to the same 14 stations (different period) and 200 groundwater wells.
- Performance metric: Kling-Gupta Efficiency (KGE) values reported per station and period.
- Observed performance: KGE values vary by station and period (range includes roughly 0.16 to 0.82 during calibration; validation values typically around 0.3–0.7, with some lower or negative values at certain stations/periods).
- Indicates spatially variable model performance across stations and timeframes.

## Data structure and files

- Data format: seven CSV files containing daily, grid-mean variables.
- Shared file structure: first four columns are xll (lower-left x coordinate), yll (lower-left y coordinate), year, timestep (Julian day 1–366).
- Files and contents:
  - Baseline_1986_2005.csv: baseline variables (1986–2005) at daily scale.
  - Ensemble_climate_2041_2060.csv: ensemble climate for 2041–2060 under RCP4.5 and RCP8.5.
  - Ensemble_climate_2061_2080.csv: ensemble climate for 2061–2080 under RCP4.5 and RCP8.5.
  - SSPs_2041_2060.csv: SSP1, SSP2, SSP3 for 2041–2060 at daily scale.
  - SSPs_2061_2080.csv: SSP1, SSP2, SSP3 for 2061–2080 at daily scale.
  - Ensemble_climate_SSPs_2041_2060.csv: combinations of RCPs (4.5/8.5) with SSPs for 2041–2060.
  - Ensemble_climate_SSPs_2061_2080.csv: combinations of RCPs with SSPs for 2061–2080.
- Variable references: each file lists the variables described in Table 2.
- Time and space: daily data for each grid cell across the specified periods.

## Using the dataset (data support perspective)

- The dataset enables comparison of baseline versus future scenarios and across multiple climate and socio-economic pathways.
- Useful for water balance studies, planning, and policy support in contexts similar to multi-sector water demand and supply.
- Given calibration/validation variability, users should consider uncertainty across stations and time periods when interpreting results.
- Data access is via seven CSV files with clearly labeled structure and daily resolution, suitable for integration into dashboards, reports, or reproducible analyses.

## Acknowledgements

- Acknowledges CMIP (World Climate Research Programme) and climate modeling groups for model outputs.
- Recognizes U.S. Department of Energy’s Program for Climate Model Diagnosis and Intercomparison for coordinating support and software infrastructure.