# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Overview
- Provides data accompanying research on reservoir operation for Pong and Bhakra in Northern India.
- Contains time series of reservoir releases (including spills), evaporation losses, and rule curves used to guide monthly reservoir management.
- Rule curves indicate target storage levels at the start of each month to avoid failing to meet demand.

## Data files included
- ReservoirData.csv
  - Monthly inflows, net-evaporation loss, and releases (all in million cubic metres, x10^6 m^3).
  - Periods: baseline (1989–2008); mid-century (2032–2050); end-century (2082–2100).
  - Future inflows produced by forcing the WEAP model with GFDL-CM3 CMIP projections.
- RuleCurve.csv
  - Optimised monthly rule curve ordinates (storage levels) for Pong and Bhakra.
  - Variables:
    - Smax: Maximum storage level (capacity)
    - URC: Upper Rule Curve (monthly target storage)
    - CRC: Critical Rule Curve (triggers water rationing)
    - LRC: Lower Rule Curve (minimum target storage)
    - DS: Dead storage
  - Includes associated reservoir rationing ratios (RR) to apply to gross demand when rationing occurs.
  - When rationing is triggered, release towards demand is capped at RR × D (D = gross demand).

## Data definitions and units
- All storage, inflow, release, and related values are in million cubic metres (x10^6 m^3).
- Monthly values cover the full yearly cycle across the specified timeframes.

## Modelling approach
- Future inflows derived from the WEAP model driven by GFDL-CM3 CMIP climate projections.

## Temporal coverage and scenarios
- Baseline: 1989–2008
- Mid-century scenario: 2032–2050
- End-century scenario: 2082–2100

## Applications and implications
- Supports reservoir operation planning and analysis under current and future climate conditions.
- Enables assessment of water supply reliability and the impact of rationing policies.
- Useful for policy planning, risk assessment, and developing self-serve data products (dashboards, charts) for stakeholders.

## Notes and contact
- Corresponding author: a.j.adeloye@hw.ac.uk