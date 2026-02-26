# Cumbrian Lakes Monitoring stratification dates dataset

## What
- Onset startstrat, end endstrat, and length lengthstrat of the stratified period in each year for each lake.
- Deepest point locations: Blelham Tarn (BT), Esthwaite Water (EW), Windermere – north basin (WNB), Windermere – south basin (WSB).
- Data collection periods:
  - BT: 1963–2017
  - EW: 1957–2017
  - WNB: 1951–2017
  - WSB: 1967–2017
- How data were collected:
  - Temperature profiles at the deepest site using a temperature-oxygen probe.
  - Weekly or fortnightly profiles; years with insufficient data around the main stratified period were excluded (BT=1, NBW=7, SBW=1).
  - Instrument errors or poorly resolved profiles (7 profiles) were removed.
  - Temperature data interpolated to a daily time step and 1 m depth resolution (akima package).
  - Temperature data converted to water density (RLakeAnalyzer); stratification determined from density difference between top and bottom (>0.1 kg m-3).
  - Stratified periods identified; start day is the latest day before DOY 200 with a stratified period lasting >14 days; end day is the final day of stratification; duration is the difference between start and end days.
- References for methods and tools:
  - Akima, H. et al. (2016) package 'akima'
  - Read, J.S. et al. (2011) Derivation of lake mixing and stratification indices from high resolution lake buoy data

## Why
- Part of the Cumbrian Lakes Long Term Monitoring programme, currently funded by the National Environment Research Council's UKSCaPE.

## Who
- Data collection history: Freshwater Biological Association (initial), later Institute for Freshwater Ecology, Centre for Ecology & Hydrology, now UK Centre for Ecology & Hydrology.
- Stratification calculations conducted by Dr Eleanor Mackay.

## Completeness
- Exclusions applied due to:
  - Insufficient profile data around the onset/end of the main stratified period.
  - Instrument errors or missing data leading to removal of certain profiles.