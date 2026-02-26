# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Overview
- Provides a time series of reservoir releases (including spills), evaporation loss, and rule curves for Pong and Bhakra reservoirs in Northern India.
- Rule curves guide reservoir operation, showing monthly target storage levels to maintain to meet demand and avoid shortfalls.

## Datasets included
- ReservoirData.csv
  - Monthly inflows, net-evaporation loss, and release (million m³, i.e., x10^6 m³) for Pong and Bhakra.
  - Periods: baseline (1989–2008), mid-century (2032–2050), end-century (2082–2100).
  - Future inflows produced by forcing the WEAP model with GFDL-CM3 CMIP climate projections.
- RuleCurve.csv
  - Optimised monthly rule-curve ordinates (storage levels, x10^6 m³) for Pong and Bhakra:
    - Smax: Maximum storage level (capacity)
    - URC: Upper Rule Curve (monthly target storage)
    - CRC: Critical Rule Curve (monthly storage that triggers water rationing)
    - LRC: Lower Rule Curve (monthly target storage)
    - DS: Dead storage
  - Includes associated rationing ratios (RR) applied to gross demand when rationing is indicated.
  - When rationing is triggered, release toward demand is capped at RR × D (D = gross demand).

## Data specifics
- Units: million cubic meters (10^6 m³)
- Temporal resolution: monthly
- Model context: WEAP-based projections; climate forcing from GFDL-CM3 CMIP

## Purpose for analysts
- Detect correlations among inflows, evaporation, releases, and rule-curve targets across baseline and future climate periods.
- Develop predictive models of reservoir operations under climate change; assess risk of hitting CRC and triggering rationing.
- Compare historical and future scenarios to support water supply planning and reliability assessments.
- Facilitate integration with other datasets (e.g., demand, boundaries) through accompanying metadata and documented variables.

## Access and context
- Corresponding author: a.j.adeloye@hw.ac.uk
- Related research: Reservoir operation study by Dau, Q and Adeloye, A.J.