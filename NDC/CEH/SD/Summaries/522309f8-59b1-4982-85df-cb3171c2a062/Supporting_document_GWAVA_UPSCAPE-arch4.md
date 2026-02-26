# GWAVA Modelling- UPSCAPE

## Overview
- GWAVA (Global Water Availability Assessment) Model 5.0 is a large-scale, semi-distributed gridded water resources model.
- Developed by UK Centre for Ecology & Hydrology; integrates natural processes and anthropogenic stresses.
- Estimates local runoff per grid cell using a lumped conceptual probability distribution model (PDM) with three storage components (soil moisture, surface, groundwater) plus a demand-driven routine for human stresses (domestic, industrial, agricultural, irrigation).
- Applied to the Cauvery Basin at 0.125-degree resolution, disaggregated into 444 modelling cells, including domestic, irrigation, industrial, livestock demands, reservoirs, and agriculture within command and rural areas.

## Data Generation and Model Setup
- Model configuration includes:
  - Probability-distributed soil moisture storage
  - Surface storage
  - Groundwater storage
  - A demand-driven routine for anthropogenic stresses
- Demands are user-defined and temporally static (domestic, industrial, livestock) or temporally/spatially dynamic (irrigation).
- The Cauvery Basin setup features integrated water transfers, major/minor reservoirs, and agricultural practices within command and rural areas.
- Climate inputs for future projections are drawn from an ensemble of climate models.

## Future Projections and Climate Scenarios
- Ensemble climate dataset used to represent future climate in GWAVA runs.
- Climate models included: BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M (with model centers listed).
- Socio-economic pathways (SSPs) used: SSP1 (SDG-oriented, low material growth), SSP2 (business as usual), SSP3 (policy-driven with rapid population growth and resource-intense systems).
- Scenarios cover combinations of RCPs (4.5 and 8.5) and SSPs for different periods (2041–2060, 2061–2080) and baseline (1985–2005).

## Variables and Units
- Key output variables are presented with short names, units, and descriptions, e.g.:
  - totQ: Total runoff, m3/s — water leaving land surface to rivers (mean over grid box/day)
  - aqlevel: Aquifer Level, m below ground level — depth to groundwater table (mean over grid box/day)
  - urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems — various water demands, in m3/s
  - uf_urban_dems, uf_rural_dems, uf_livestock_dems, uf_industrial_dems, uf_irrigation_dems — unfulfilled demands
- All variables are provided as daily means over grid boxes.

## Quality Control and Model Performance
- Calibrated at 14 gauging stations using SIMPLEX auto-calibration (four parameters: surface/GW routing, PDM soil moisture, rooting depth multiplier).
- Validated at the same 14 stations (different period) and 200 groundwater wells.
- Performance reported as Kling-Gupta Efficiency (KGE) with per-station results:
  - Calibration KGE values range from about 0.24 to 0.82 across stations.
  - Validation KGE values range from about -1.27 to 0.68, indicating mixed performance (some stations strong, others weaker or problematic).
- Indicates regional reliability varies by location and period; some stations show substantial predictive limitations.

## Data Structure and Access
- Outputs are distributed across seven CSV files.
- Each file begins with four grid descriptor columns: xll (lower-left x coordinate), yll (lower-left y coordinate), year, timestep (Julian day 1–366).
- File types include:
  - Baseline_1986_2005.csv — baseline daily-scale variables (1986–2005)
  - Ensemble_climate_2041_2060.csv — ensemble climate for RCP4.5 and RCP8.5 (2041–2060)
  - Ensemble_climate_2061_2080.csv — ensemble climate for RCP4.5 and RCP8.5 (2061–2080)
  - SSPs_2041_2060.csv — SSP1/2/3 (2041–2060)
  - Ensemble_climate_SSPs_2041_2060.csv — combined RCPs and SSPs (2041–2060)
  - Ensemble_climate_SSPs_2061_2080.csv — combined RCPs and SSPs (2061–2080)
- Variables in each file correspond to those described in the variable table (Table 2).
- Data providers acknowledge CMIP and supporting modeling communities; data is supported by UKCEH and partner institutions.

## Acknowledgements and Context
- Acknowledges CMIP World Climate Research Programme's modeling groups and the U.S. DOE’s Program for Climate Model Diagnosis and Intercomparison, plus infrastructure support for climate data portals.
- Supporting organizations include UK Centre for Ecology & Hydrology and Environment Centre Wales, with listed regional offices.