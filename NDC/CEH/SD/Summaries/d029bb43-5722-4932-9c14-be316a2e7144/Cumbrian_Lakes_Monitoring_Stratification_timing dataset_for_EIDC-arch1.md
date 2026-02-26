# Cumbrian Lakes Monitoring stratification dates dataset

- This dataset records the onset (startstrat), end (endstrat), and length (lengthstrat) of each year’s stratified period for four Cumbrian lakes, plus the deepest-point locations used for data collection.
- Lakes covered: Blelham Tarn (BT), Esthwaite Water (EW), Windermere north basin (WNB), Windermere south basin (WSB).
- Data span per lake:
  - BT: 1963–2017
  - EW: 1957–2017
  - WNB: 1951–2017
  - WSB: 1967–2017

## How data were collected

- Method: temperature profiles at the deepest site in each lake using a temperature–oxygen probe.
- Sampling cadence: weekly or fortnightly profiles; years with insufficient data around the main stratified period were excluded.
- Data cleaning: profiles with instrument errors or poor resolution due to missing data were removed (up to 7 profiles per dataset).
- Processing:
  - Temperature data interpolated to daily time steps with 1 m depth resolution (using the akima R package).
  - Temperature profiles converted to water density (via RLakeAnalyzer).
  - Stratification determined by density difference between top and bottom greater than 0.1 kg m-3.

## How stratified periods were identified

- Start day: the latest day before day 200 where a stratified period had duration >14 days.
- End day: the final day of the stratified period.
- Duration: end day minus start day.
- Stratified periods identified for each year and lake.

## Software and references

- Interpolation: akima package (Akima et al. 2016).
- Density/stratification derivation: Read et al. 2011 (Derivation of lake mixing and stratification indices from high resolution lake buoy data).

## Why the data were collected

- Collected as part of the Cumbrian Lakes Long Term Monitoring Programme, currently funded by the UK National Capability programme UKSCaPE.

## Who collected and who did the analysis

- Data collection history: Freshwater Biological Association; later Institute for Freshwater Ecology, Centre for Ecology & Hydrology; currently UK Centre for Ecology & Hydrology.
- Stratification calculations: Dr Eleanor Mackay.

## Completeness and quality

- Exclusions due to insufficient data around the onset/end of summer stratification (example exclusions: BT=1; NBW=7; SBW=1).
- Additional exclusions: individual date profiles removed due to instrument error or poor resolution.
- Overall orientation: data quality checks and documentation of exclusions are noted to ensure transparency.