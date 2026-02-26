# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Overview
- Data accompany the research on reservoir operation for the Pong and Bhakra reservoirs in Northern India.
- Authors: Dau, Q and Adeloye, A.J. Corresponding author: a.j.adeloye@hw.ac.uk
- Contains time series of reservoir releases (including spills), evaporation loss, and rule curves used to guide monthly reservoir operation.

## Data Files
- ReservoirData.csv
  - Monthly inflows, net-evaporation loss, and releases (in million cubic metres, x10^6 m^3) for Pong and Bhakra.
  - Periods: baseline (1989–2008), mid-century (2032–2050), end-century (2082–2100).
  - Future inflows derived by forcing the WEAP model with GFDL-CM3 CMIP climate projections.
- RuleCurve.csv
  - Optimised rule-curve ordinates (monthly storage targets) for Pong and Bhakra:
    - Smax: Maximum storage level (capacity)
    - URC: Upper Rule Curve (monthly target storage)
    - CRC: Critical Rule Curve (monthly trigger for water rationing)
    - LRC: Lower Rule Curve (monthly target storage)
    - DS: Dead storage
  - Also includes associated reservoir rationing ratios (RR) applicable to gross demand (D) when rationing is triggered.
  - When rationing is triggered, releases to meet demand are capped at RR × D.

## Data Content and Units
- All values in million cubic metres (x10^6 m^3).
- ReservoirData.csv covers inflows, net-evaporation, and releases (including spills).
- RuleCurve.csv provides monthly (January–December) target storage levels and rationing parameters.

## Temporal Coverage and Forcing
- Baseline period: 1989–2008
- Mid-century scenario: 2032–2050
- End-century scenario: 2082–2100
- Climate forcing: WEAP model driven by GFDL-CM3 CMIP projections

## Purpose and Applications
- Supports analysis and optimization of reservoir operation for Pong and Bhakra.
- Enables evaluation of rule-curve strategies and potential rationing scenarios under climate change.
- Provides data suitable for informing monitoring frameworks, data governance, and transparent decision-support tools.

## Data Management and Accessibility
- Data are provided to accompany the research publication.
- Corresponding author contact is available for further information or access.