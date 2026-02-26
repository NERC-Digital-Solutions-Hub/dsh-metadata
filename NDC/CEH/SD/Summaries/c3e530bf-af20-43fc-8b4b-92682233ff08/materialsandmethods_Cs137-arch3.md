# Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic

## Overview
- Examines deposition rates of long-lived radionuclides (especially Cs-137) from atmospheric nuclear weapons tests and their correlation with precipitation.
- Aims to estimate UK-wide deposition of Cs-137 prior to the Chernobyl accident by linking local deposition records to UK precipitation data.
- Uses Milford Haven (Wales, UK) as the representative UK site for complete quarterly deposition records between 1955-1985.

## Data sources
- Cs-137 deposition records from the UK Atomic Energy Authority (AEA/AERE): 19 UK stations and 20 international stations (1955-1997); complete quarterly data for Gibraltar, Singapore, and Milford Haven (1955-85).
- Milford Haven deposition data combined with Milford Haven quarterly precipitation data (1955-85) to create deposition/precipitation ratios.
- UK precipitation data:
  - UK Met Office gridded precipitation data (baseline climate variables for 1961-1990; 5 × 5 km resolution) used to represent UK-wide spatial variability.
  - UKCIP2009 data referenced for precipitation information (monthly totals used to represent spatial variation).

## Method
- For each quarter, compute the 137 Cs deposition/precipitation ratio at Milford Haven.
- Apply this ratio to the UK terrestrial total precipitation to estimate UK spatial variability in quarterly 137 Cs input at 5 × 5 km resolution.
- Add the quarterly deposition to any pre-existing predicted deposition and apply decay correction for 137 Cs (half-life ≈ 30.2 years) to derive cumulative deposition from 1955-1985 at 5 × 5 km resolution.

## Key outputs
- Spatially resolved (5 × 5 km) estimates of 137 Cs deposition across the UK for 1955-1985.
- Temporal alignment to quarters, with a decay-corrected cumulative tally.

## Implications for monitoring frameworks
- Demonstrates a data-integrative approach combining legacy deposition records with gridded precipitation data to produce spatially explicit environmental contamination estimates.
- Shows how single-site proxies (Milford Haven) can be used to infer broader regional deposition patterns when coupled with precipitation data.
- Provides a reproducible methodology for retrospective assessment of radionuclide deposition and for informing long-term environmental monitoring strategies.

## Limitations and considerations
- Reliance on Milford Haven as representative UK deposition site; potential regional variability may not be fully captured.
- Assumes a stable deposition-precipitation relationship derived from a specific historical period and site.
- Dependence on historical datasets with inherent uncertainties and potential gaps in metadata.

## Reference
- Wright, S.M., Howard, B.J., Strand, P., Nylen, T., & Sickel, M.A.K. 1999. Prediction of 137 Cs deposition from atmospheric nuclear weapons tests within the Arctic. Environmental Pollution, 104, 131-143. DOI: 10.1016/S0269-7491(98)00140-7