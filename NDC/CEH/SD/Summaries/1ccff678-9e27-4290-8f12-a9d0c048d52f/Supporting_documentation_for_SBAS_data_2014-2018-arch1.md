# Surface temperature, surface oxygen, water clarity, water chemistry and phytoplankton chlorophyll a data from South Basin of Windermere 2014 to 2018

- A long-running monitoring dataset capturing key limnological variables from the South Basin of Windermere, Cumbria, England, collected 2014–2018.
- Aims to support analysis of how physical, chemical, and biological parameters relate and change over time, with potential for modelling and forecasting impacts of environmental drivers.

## Sampling regime and collection methods

- Fortnightly sampling as part of ongoing monitoring.
- Location and depth: measurements taken from a boat at a marked buoy in the deepest part of the lake (0–7 m integrated water sample).
- Variables collected (with units as recorded): 
  - TEMP: surface temperature in degrees Celsius
  - OXYG: surface oxygen saturation in % air-saturation
  - SECC: Secchi depth in metres
  - ALKA: alkalinity in µg CaCO3 per litre
  - pH
  - NH4N: ammonium in µg N per litre
  - NO3N: nitrate in µg N per litre
  - PO4P: soluble reactive phosphate in µg P per litre
  - TOTP: total phosphorus in µg P per litre
  - SIO2: dissolved reactive silicon in µg per litre
  - TOCA: phytoplankton chlorophyll a in µg per litre
- Data coded with a “Sign (if<LOD)” indicator if values are below detection limits.

## Data quality and structure

- Data are raw and have not yet undergone final quality control or calibration.
- Double entered and visually checked; missing data attributed to weather or staff shortages.
- Data provided as a comma-separated values (CSV) file with fields:
  - Date, Description (variable), Value, Description (units/notes)
  - Sign (if<LOD) to indicate below detection limit.

## Temporal and spatial scope

- Timeframe: January 2014 through the end of 2018.
- Spatial scope: South Basin of Windermere, the deepest part of the lake, sampled from a fixed buoy location.

## Data accessibility and format

- CSV data structure with explicit variable descriptions and units.
- Includes metadata notes on sampling method, detection limits, and data limitations (raw status, QC pending).

## Funding and provenance

- Funded by Natural Environment Research Council (NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.
- Dataset has supported numerous publications and climate- and ecology-focused research.

## Notable uses and publications (examples)

- State of the Climate in 2018 (Bulletin of the American Meteorological Society), highlighting climate-related context.
- The extent and variability of storm-induced temperature changes in lakes (Limnology & Oceanography, 2021).
- Temporal and spatial distribution studies related to fish environmental DNA in large lakes (Environmental DNA, 2019).
- Physical and chemical impacts of major storms on temperate lakes (Climatic Change, 2018).
- Broader ecological and climate-change context across lakes and ecosystems (e.g., Nature 2016, Journal of Applied Ecology 2016; other related ecologic/informatics works listed in accompanying overview).

## Implications for data analysis and modelling

- Useful for investigating correlations between physical (temperature, oxygen, Secchi depth) and chemical/biological parameters (nutrients, chlorophyll a).
- Supports detection of seasonal and storm-driven anomalies and their cascading effects on lake chemistry and productivity.
- Data are raw; users should account for lack of QC/calibration and potential missing values when building predictive models.
- The structured, time-series nature facilitates calibration/validation of hydrological, biogeochemical, and ecological models for Windermere or comparable freshwater systems.