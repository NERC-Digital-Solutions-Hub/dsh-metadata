# Cumbrian Lakes Monitoring stratification dates dataset

## What
- Documents the onset (startstrat), end (endstrat), and duration (lengthstrat) of each year’s main stratified period for four Cumbrian lakes.
- Provides the deepest measurement points for each lake: Blelham Tarn (BT), Esthwaite Water (EW), Windermere north basin (WNB), and Windermere south basin (WSB).
- Includes data collection periods: BT (1963–2017), EW (1957–2017), Windermere NW (1951–2017), Windermere SB (1967–2017).
- Details data handling: temperature profiles from deepest site using a temperature-oxygen probe; data cleaned for insufficient profile coverage, instrument errors, and poorly resolved profiles; daily interpolation from weekly/fortnightly data; density derived from temperature via RLakeAnalyzer; stratification determined when top-bottom density difference > 0.1 kg m-3; start and end of each stratified period defined as described.

## Where and When
- Location: four Cumbrian lakes as above.
- Timeframe: long-term historical records spanning mid-20th century to 2017 (varying by lake).
- Data source for processing: temperature profiles and related measurements at the deepest lake point.

## How
- Data collection: weekly or fortnightly temperature profiles at the deepest site; instrument reliability checked; years with insufficient data around stratification windows excluded.
- Data processing:
  - Interpolate water temperature to a daily time step with 1 m depth resolution (using Akima package).
  - Convert temperatures to water density (via RLakeAnalyzer) and identify stratification by density difference > 0.1 kg m-3.
  - Identify all stratified periods each year; define main summer stratified period with start as the latest day before day 200 where a stratified period lasted >14 days; end as the final day of the stratified period; duration as the difference.
- Tools and references: Akima (2016) package; Read et al. (2011) developed indices for lake mixing/stratification.

## Why
- Part of the Cumbrian Lakes Long-Term Monitoring Programme funded by the National Environment Research Council’s UKSCaPE programme.
- Aims to support ongoing environmental health monitoring and understanding of lake stratification dynamics over time.

## Who
- Data origination: Freshwater Biological Association (initially), later Institute for Freshwater Ecology, Centre for Ecology & Hydrology, and now UK Centre for Ecology & Hydrology.
- Computational work: stratification calculations performed by Dr. Eleanor Mackay.

## Completeness
- Data completeness affected by:
  - Exclusion of years with insufficient profile data around stratification windows.
  - Removal of certain profiles due to instrument error or poor resolution.
- Notes indicate specific exclusions and quality checks applied to ensure reliable stratification dating.