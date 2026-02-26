# GWAVA Modelling- UPSCAPE

- A large-scale, semi-distributed gridded water resources model (GWAVA) developed by the UK Centre for Ecology & Hydrology to assess water availability and the impact of anthropogenic stresses.
- The Cauvery Basin is modeled at 0.125-degree resolution, disaggregated into 444 cells, incorporating domestic, irrigation, industrial, livestock demands, large-scale transfers, reservoirs, and agriculture.

## Model Setup and Domain

- GWAVA version 5.0 configured with three components: soil moisture storage (PDM), surface storage, and groundwater storage, followed by a demand-driven routine.
- Domestic, industrial, and livestock demands are user-defined and temporally static, while irrigation demand is dynamic by crop type and planting month.
- The model accounts for urban/rural domestic demand, irrigation, industry, livestock, and unfulfilled demand across the basin, including large transfers and reservoirs.

## Future Projections and Scenarios

- Climate projections are sourced from multiple CMIP5 models to form an ensemble representing future climate for GWAVA runs.
- Climate models used include BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, and NorESM1-M.
- Socio-economic pathways and scenarios:
  - SSP1: Sustainable development with low material growth and lower resource intensity.
  - SSP2: Business-as-usual with no major changes to current behavior.
  - SSP3: Sector-centric policies with rapid population growth and resource intensification.
- Scenarios are paired with RCPs (4.5 and 8.5) for 2041–2060 and 2061–2080 and are provided as daily-scale ensemble data.

## Variables and Units

- Total runoff (totQ): m3/s; mean over grid cell and day; water leaving land to rivers.
- Aquifer Level (aqlevel): m below ground level; mean over grid cell and day.
- Domestic, Rural, and Livestock Demands:
  - Urban domestic demand (urban_dems): m3/s.
  - Rural domestic demand (rural_dems): m3/s (livestock/demand context provided).
  - Livestock demand (livestock_dems): m3/s (subcategories for cattle/goats/sheep).
  - Industrial demand (industrial_dems): m3/s (including irrigation-related components).
  - Irrigation demand (irrigation_dems): m3/s (includes irrigation efficiency).
- Unfulfilled demand variables (e.g., uf_urban_dems, uf_rural_dems, uf_livestock_dems, uf_industrial_dems, uf_irrigation_dems): m3/s; daily mean per grid cell.
- Data are organized for baseline (1986–2005) and ensembles for future periods (2041–2060, 2061–2080) under various SSPs and RCPs, at daily resolution.

## Quality Control and Validation

- Calibration performed at 14 gauging stations using SIMPLEX auto-calibration with four parameters (surface and groundwater routing, PDM soil moisture, rooting depth multiplier).
- Validation conducted at the same 14 stations (different period) plus 200 groundwater wells.
- Model performance reported as Kling-Gupta Efficiency (KGE) with site-specific values:
  - Examples range from moderate (e.g., KGE ~0.24–0.82 during calibration) to lower in some validation periods (e.g., KGE as low as -1.27).
- Validation results indicate varying model skill across sites and periods, informing interpretation of projected outputs.

## Data Structure and Access

- Outputs are provided as seven CSV files with common spatial-temporal headers:
  - Each file includes xll, yll (lower-left grid cell coordinates), year, and timestep (Julian day).
  - Baseline_1986_2005.csv: daily variables for 1986–2005.
  - Ensemble_climate_2041_2060.csv and Ensemble_climate_2061_2080.csv: daily variables for RCP4.5 and RCP8.5 periods.
  - SSPs_2041_2060.csv and SSPs_2061_2080.csv: daily variables for SSP1, SSP2, SSP3.
  - Ensemble_climate_SSPs_2041_2060.csv and Ensemble_climate_SSPs_2061_2080.csv: daily variables for combinations of RCPs and SSPs.
- Variables are described in Table 2 (e.g., totQ, aqlevel, urban_dems, rural_dems, livestock_dems, industrial_dems, irrigation_dems, unfulfilled_*).
- Data are structured for daily scale analysis within each grid cell, enabling temporal trend assessment and scenario comparison.

## Acknowledgements

- Acknowledges CMIP and the World Climate Research Programme’s Working Group on Coupled Modelling, climate modeling groups, and the U.S. Department of Energy’s Program for Climate Model Diagnosis and Intercomparison for coordinating support and software infrastructure.