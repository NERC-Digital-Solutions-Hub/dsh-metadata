# Cumbrian Lakes Monitoring stratification dates dataset

## What
- Onset ('startstrat'), end ('endstrat'), and length ('lengthstrat') of the stratified period in each year for the dataset.
- Four lakes: Blelham Tarn (BT), Esthwaite Water (EW), Windermere north basin (WNB), Windermere south basin (WSB).
- Stratification calculations provide the main summer stratified period dates and duration.

## Where
- Stratification assessed at the deepest point in each lake (BT, EW, WNB, WSB).

## When
- Data collection years:
  - BT: 1963–2017
  - EW: 1957–2017
  - WNB: 1951–2017
  - WSB: 1967–2017

## How
- Data collection: weekly or fortnightly temperature profiles at the deepest site using a temperature-oxygen probe.
- Year eligibility: exclude years with insufficient profiles around onset/end of the main stratified period in summer.
- Data quality: remove profiles with instrument error or poor resolution due to missing data.
- Processing:
  - Interpolate temperature data to daily time steps and 1 m depth resolution (using Akima package).
  - Convert to water density (via RLakeAnalyzer) and compute top-bottom density difference.
  - Define stratified year if density difference > 0.1 kg m-3.
  - Start day: latest day before day 200 with a stratified period lasting >14 days.
  - End day: final day of the stratified period.
  - Duration: difference between start and end days.
- Tools referenced: Akima (Akima et al. 2016) and Read et al. 2011 for derivation of stratification indices.

## Why
- Part of the Cumbrian Lakes Long Term Monitoring programme, currently funded by the National Environment Research Council's UKSCaPE.

## Who
- Initial data collection: Freshwater Biological Association.
- Later collection: Institute for Freshwater Ecology, Centre for Ecology & Hydrology.
- Current stewardship: UK Centre for Ecology & Hydrology.
- Stratification calculations: Dr Eleanor Mackay.

## Completeness
- Some data excluded due to insufficient profiling around onset/end of the main stratified period (BT=1, NBW=7, SBW=1).
- Instrument errors or poorly resolved profiles led to removal of specific dates (n=7 dates referenced).