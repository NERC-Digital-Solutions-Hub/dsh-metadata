# Cumbrian Lakes Monitoring stratification dates dataset

## Overview
- Catalogues the onset (startstrat), end (endstrat), and duration (lengthstrat) of each year’s main stratified period for four Cumbrian lakes.
- Also records the deepest point locations for BT, EW, Windermere North Basin (WNB), and Windermere South Basin (WSB).
- Data span across multiple decades, with lake-specific collection years.
- Stratification is determined from daily-interval density differences derived from temperature profiles.

## Lakes and deepest points
- Lakes: Blelham Tarn (BT), Esthwaite Water (EW), Windermere North Basin (WNB), Windermere South Basin (WSB).
- Deepest points used for profiling to assess stratification.

## Temporal coverage
- BT: 1963–2017
- EW: 1957–2017
- Windermere North Basin (WNB): 1951–2017
- Windermere South Basin (WSB): 1967–2017

## Data collection methods
- Temperature profiles collected at the deepest site of each lake using a temperature–oxygen probe.
- Frequency: weekly or fortnightly during the monitoring windows.
- Data quality control: years with insufficient profiles around the onset/end of the main stratified period are excluded (BT=1, NBW=7, SBW=1). Individual date profiles with instrument errors or poor resolution are removed (n = 7).
- Interpolation: water temperature was interpolated to a daily time step with 1 m depth resolution (using the akima package).

## Data processing and stratification calculation
- Temperature data converted to water density (using RLakeAnalyzer) and the difference between top and bottom densities computed.
- Stratified if density difference > 0.1 kg m-3 between top and bottom.
- Start of the main summer stratified period: the latest day before DOY 200 when a stratified period had duration >14 days.
- End of the stratified period: the final day of stratification for that period.
- Duration: end day minus start day.

## Data quality and completeness
- Some data excluded due to insufficient profile data around stratification onset/offset.
- Instrument errors or poorly resolved profiles led to removal of specific dates (7 profiles removed).

## Purpose and provenance
- Purpose: part of the Cumbrian Lakes Long Term Monitoring Programme, currently funded by the NERC UKSCaPE programme.
- Data origin: originally collected by the Freshwater Biological Association; later by the Institute for Freshwater Ecology and Centre for Ecology & Hydrology; presently by the UK Centre for Ecology & Hydrology.
- Stratification calculations performed by Dr. Eleanor Mackay.

## Data storage and access
- Created datasets are stored and uploaded to appropriate data portals as part of the monitoring workflow.

## References (methodology and tools)
- Akima, H., Gebhardt, A., Petzold, T., Maechler, M. (2016). Package 'akima'.
- Read, J.S. et al. (2011). Derivation of lake mixing and stratification indices from high-resolution lake buoy data. Environmental Modelling Software, 26, 1325e1336.