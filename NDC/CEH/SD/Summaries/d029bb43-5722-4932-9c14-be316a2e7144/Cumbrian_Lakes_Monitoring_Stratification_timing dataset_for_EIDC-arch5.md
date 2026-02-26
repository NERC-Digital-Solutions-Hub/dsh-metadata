# Cumbrian Lakes Monitoring stratification dates dataset

- Provides onset (startstrat), end (endstrat), and duration (lengthstrat) of the main summer stratified period for each year and lake.
- Records the deepest point in four lakes: Blelham Tarn (BT), Esthwaite Water (EW), Windermere north basin (WNB), and Windermere south basin (WSB).

## What

- Stratification metrics: startstrat, endstrat, lengthstrat for each year/lake.
- Depth and location data: deepest point in each lake.

## Where

- Deepest sampling sites per lake: BT, EW, WNB, WSB.

## When

- Data collection periods by lake:
  - BT: 1963–2017
  - EW: 1957–2017
  - Windermere, north basin (WNB): 1951–2017
  - Windermere, south basin (WSB): 1967–2017

## How

- Data collection method: temperature profiles at the deepest site using a temperature–oxygen probe.
- Frequency: weekly or fortnightly profiles; years with insufficient profile data around onset/end are excluded.
- Data quality: remove individual dates with instrument error or poorly resolved data.
- Data processing:
  - Linearly interpolate temperature data to daily time steps and 1 m depth resolution (using akima package in R).
  - Convert temperature to water density (using RLakeAnalyzer) and compute top–bottom density difference.
  - Stratified if density difference > 0.1 kg m-3.
  - Start of main summer stratified period: latest day before day 200 with a prior stratified period duration > 14 days.
  - End of stratification: final day of stratification; duration = end − start.
- Documentation and references:
  - Akima, H. et al. (2016) package akima.
  - Read, J.S. et al. (2011) methodology for derivation of lake mixing/stratification indices.

## Why

- Part of the Cumbrian Lakes Long Term Monitoring programme, currently funded by the National Environment Research Council's UKSCaPE programme.

## Who

- Initial data collection: Freshwater Biological Association.
- Subsequent collection: Institute for Freshwater Ecology, Centre for Ecology & Hydrology; currently UK Centre for Ecology & Hydrology.
- Stratification calculations: Dr Eleanor Mackay.

## Completeness

- Some data excluded due to insufficient profile data around onset/end for each lake (BT=1, NBW=7, SBW=1).
- Additional exclusions: instrument errors or poorly resolved profiles (n = 7).

## Data provenance and governance notes for Data Stewards

- Metadata needs to document:
  - Sampling frequency, site locations, and deepest-point identifiers for each lake.
  - Criteria for excluding years and dates (insufficient data, instrument errors).
  - Processing steps (interpolation method, depth resolution, density calculation, stratification threshold).
  - Start/end definitions and duration calculations.
  - Data providers and changes in stewardship over time.
- Quality assurance considerations:
  - Maintain versioning and change logs for methodological updates.
  - Ensure reproducibility by recording software packages and versions (e.g., akima, RLakeAnalyzer) and the exact processing steps.
  - Clarify any ongoing or future updates to yearly stratification determinations and how updates propagate to metadata and downstream datasets.
- Interoperability and accessibility:
  - Use consistent lake identifiers (BT, EW, WNB, WSB) and time formats.
  - Provide clear data governance statements regarding embargoes, data sharing permissions, and any residual limitations due to incomplete data.