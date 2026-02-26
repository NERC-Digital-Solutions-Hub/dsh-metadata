# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Purpose and scope
- Provides time series data for reservoir releases (including spills), net evaporation loss, and rule curves for the Pong and Bhakra reservoirs in Northern India.
- Rule curves serve as guides for reservoir operation, indicating target storage levels at the start of each month to avoid unmet demand.

## Data files and contents
- ReservoirData.csv
  - Monthly inflows, net-evaporation loss, and releases (all in million cubic metres, x10^6 m^3).
  - Periods: baseline (1989–2008), mid-century (2032–2050), end-century (2082–2100).
  - Future inflows produced by WEAP model forced with climate projections from the GFDL-CM3 CMIP model.
  - Includes spills.
- RuleCurve.csv
  - Optimised monthly rule curve ordinates for Pong and Bhakra:
    - Smax: Maximum storage level (capacity)
    - URC: Upper Rule Curve target storage (January–December)
    - CRC: Critical Rule Curve (rationing trigger) storage (January–December)
    - LRC: Lower Rule Curve target storage (January–December)
    - DS: Dead storage
  - Also includes rationing ratios (RR) applicable to gross demand when rationing is indicated.
  - When rationing is triggered, releases toward demand are capped at RR × D (D = gross demand for the period).

## Data sources and modeling approach
- Uses WEAP (Water Evaluation And Planning) model for simulations.
- Climate forcing derived from the GFDL-CM3 CMIP model for future inflows.

## Units and temporal scope
- All values expressed in million cubic metres (x10^6 m^3).
- Monthly resolution across the three time horizons: baseline, mid-century, end-century.

## Intended use
- Supports reservoir operation analysis and planning by providing standardized data and optimized storage/rationing targets.
- Enables assessment of how inflows, evaporation, and rule-curves influence releases and demand satisfaction over time.

## Access and contact
- Data accompany the associated reservoir operation research.
- Corresponding author: a.j.adeloye@hw.ac.uk