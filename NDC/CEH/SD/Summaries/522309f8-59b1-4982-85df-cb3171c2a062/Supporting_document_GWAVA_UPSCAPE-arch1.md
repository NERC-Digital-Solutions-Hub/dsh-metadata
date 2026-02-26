# GWAVA Modelling- UPSCAPE

- The GWAVA5.0 model is a large-scale, semi-distributed gridded water resources tool developed by the UK Centre for Ecology & Hydrology. It estimates local runoff using a probability-distributed soil moisture storage (PDM) framework and accounts for surface and groundwater storage, followed by a demand-driven routine that represents anthropogenic stresses on the system (domestic, industrial, agricultural, and irrigation).  

- Study area and setup
  - Cauvery Basin modelled at 0.125-degree resolution, disaggregated into 444 modelling cells.
  - Includes domestic, irrigation, industrial, and livestock demands; large and minor reservoirs; and agriculture within command and rural areas.

- Climate and future projections
  - Ensemble climate dataset used to represent future climate for GWAVA runs.
  - Climate models included: BCC-CSM1-1, IPSL-CM5A-LR, MIROC-ESM, MIROC-ESM-CHEM, NorESM1-M.
  - Socio-economic and scenarios: Shared Socio-economic Pathways (SSP1, SSP2, SSP3) and Representative Concentration Pathways (RCP4.5, RCP8.5).
  - Time periods covered: Baseline (1985/1986–2005); ensembles for 2041–2060 and 2061–2080.

- Variables and units (Table 2)
  - TotQ (Total runoff): m3/s; mean over grid cell and day.
  - Aquifer Level (aqlevel): m below ground level; mean over grid cell and day.
  - Urban domestic demand (urban_dems): m3/s; domestic demand (urban).
  - Rural domestic demand (rural_dems): m3/s; livestock and domestic demand subsets.
  - Livestock demand (livestock_dems1–3): m3/s; includes different livestock categories.
  - Industry demand (industrial_dems): m3/s; includes industrial demand.
  - Irrigation demand (irrigation_dems): m3/s; derived from irrigated crops and irrigation efficiency; includes urban demand components.
  - Unfulfilled demand variables (uf_…): corresponding unfulfilled urban, rural, livestock, industrial, and irrigation demands (m3/s).
  - All variables are presented as daily means per grid cell.

- Quality control and model performance
  - Calibration performed at 14 gauging stations using SIMPLEX auto-calibration with four parameters (surface and groundwater routing, PDM soil-moisture capacity variation, rooting depth multiplier).
  - Validation conducted at the same 14 stations (different period) and at 200 groundwater wells.
  - Performance shown via Kling-Gupta Efficiency (KGE) values (calibration and validation) across sites; calibration KGE ranges roughly from 0.24 to 0.82 across sites; validation KGE ranges from approximately -1.27 to 0.68, indicating varying skill across locations and periods.

- Data structure and access
  - Data delivered in seven CSV files.
  - Common header: first four columns are xll (lower-left x-coordinate of grid), yll (lower-left y-coordinate), year, timestep (Julian day 1–366).
  - Files and coverage:
    - Baseline_1986_2005.csv: baseline variables, daily scale (1986–2005).
    - Ensemble_climate_2041_2060.csv: ensemble climate for 2041–2060 under RCP4.5 and RCP8.5.
    - Ensemble_climate_2061_2080.csv: ensemble climate for 2061–2080 under RCP4.5 and RCP8.5.
    - SSPs_2041_2060.csv: SSP1, SSP2, SSP3 for 2041–2060 daily scale.
    - Ensemble_climate_SSPs_2041_2060.csv: combination of RCPs, SSP1/SSP3 for 2041–2060 daily scale.
    - SSPs_2061_2080.csv: SSP1, SSP2, SSP3 for 2061–2080 daily scale.
    - Ensemble_climate_SSPs_2061_2080.csv: combination of RCPs, SSP1/SSP2/SSP3 for 2061–2080 daily scale.
  - Terminology in files: BL = baseline; ENA = ensemble climate data; SSP = socio-economic pathways; RCP = climate concentration pathway.
  - Coverage is daily scale across specified periods.

- Acknowledgements
  - Recognizes CMIP and climate modeling groups for model outputs; references CMIP collaboration and supporting organizations (e.g., U.S. Department of Energy contributions).