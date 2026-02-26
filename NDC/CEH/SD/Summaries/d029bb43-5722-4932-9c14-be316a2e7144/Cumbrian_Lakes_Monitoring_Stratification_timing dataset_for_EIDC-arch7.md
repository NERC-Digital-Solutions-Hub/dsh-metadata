# Cumbrian Lakes Monitoring stratification dates dataset

## Overview
- Dataset of stratified period dates for four Cumbrian lakes: Blelham Tarn (BT), Esthwaite Water (EW), Windermere north basin (WNB), and Windermere south basin (WSB).
- For each year, records onset (startstrat), end (endstrat), and duration (lengthstrat) of the main summer stratified period.

## Spatial and temporal scope
- Lakes and deepest points:
  - BT, EW, WNB, WSB (deepest site per lake)
- Temporal coverage by lake:
  - BT: 1963–2017
  - EW: 1957–2017
  - Windermere, WNB: 1951–2017
  - Windermere, WSB: 1967–2017

## Data collection and processing
- Data collected as temperature profiles at the deepest site using a temperature-oxygen probe.
- Sampling frequency: weekly or fortnightly temperature profiles.
- Yearly data curation: exclude years with insufficient data around onset/end of main stratified period; remove instrument-error or poorly resolved profiles (specific exclusions noted per lake).
- Data processing:
  - Interpolate water temperature to a daily time step and depth resolution of 1 m (using the Akima R package).
  - Convert to water density (via RLakeAnalyzer) and compute the density difference between top and bottom.
  - Stratified if density difference > 0.1 kg m^-3.

## Stratification criteria and definitions
- Startstrat: the latest day before day of year 200 where a stratified period had duration > 14 days.
- Endstrat: the final day of stratification for that stratified period.
- Lengthstrat: duration between startstrat and endstrat.

## Data provenance and authorship
- Why: part of the Cumbrian Lakes Long Term Monitoring Programme, funded by UKSCaPE (UK National Capability programme).
- Who collected: initially Freshwater Biological Association; later Institute for Freshwater Ecology, Centre for Ecology & Hydrology; currently UK Centre for Ecology & Hydrology.
- Stratification calculations: Dr Eleanor Mackay.

## Data quality and completeness
- Completeness notes: some years excluded due to insufficient profile data around onset/end; instrument errors or missing data in individual profiles.
- Overall quality controlled through data exclusions and standardized processing steps.

## References and methods
- Akima, H., Gebhardt, A., Petzold, T., Maechler, M. (2016). Package 'akima'.
- Read, J.S. et al. (2011). Derivation of lake mixing and stratification indices from high-resolution lake buoy data. Environmental Modelling Software.