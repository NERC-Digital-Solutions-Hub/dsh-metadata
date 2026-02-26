# Supporting document for 'Reservoir inflows and release data, and optimised monthly rule curve ordinates (upper, lower and critical) for Pong and Bhakra reservoirs in Northern India' data

## Overview
- Provides a time series of reservoir releases (including spills), evaporation loss, and rule curves for the Pong and Bhakra reservoirs in Northern India.
- Rule curves define target storage levels to maintain month-by-month to meet demand and avoid shortfalls.

## Data Files
- ReservoirData.csv
  - Contains monthly inflows, net-evaporation loss, and releases (in million cubic metres, x 10^6 m^3).
  - Scenarios: baseline (1989–2008), mid-century (2032–2050), end-century (2082–2100).
  - Future inflows driven by forcing the WEAP basin model with GFDL-CM3 CMIP climate projections.

- RuleCurve.csv
  - Contains optimised rule curve ordinates (storage levels, x 10^6 m^3) for Pong and Bhakra:
    - Smax: maximum storage level (capacity)
    - URC: Upper Rule Curve (monthly targets January–December)
    - CRC: Critical Rule Curve (monthly trigger for water rationing)
    - LRC: Lower Rule Curve (monthly target minimum storage)
    - DS: Dead storage
  - Includes associated rationing ratios (RR) to apply to gross demand when rationing is required.
  - When rationing occurs, releases to meet demand are capped at RR × D (D = gross demand for the period).

## Data Scope and Modeling
- Reservoirs: Pong and Bhakra, located in Northern India.
- Data resolution: monthly time steps.
- Modeling framework: WEAP (Water Evaluation And Planning system).
- Climate forcing: GFDL-CM3 CMIP projections drive future inflows for mid-century and end-century scenarios.

## Usage and Governance Considerations for Data Leaders
- Data provenance and traceability: clearly linked to the researchers Dau, Q and Adeloye, A.J., with corresponding author provided.
- Data quality and suitability: includes multiple temporal scenarios (historical and future) and clearly defined variables (inflows, evaporation, releases, and rule-curve storages).
- Metadata and discoverability: two CSV files with explicit variable definitions and units; future inflows linked to a defined climate model forcing.
- Data integration potential: enables assessment of reservoir operation under climate change, optimization of monthly rule curves, and planning for rationing strategies.
- Collaboration and reuse: suitable for cross-referencing with regional water demand data and other reservoir systems to support broader water-management analyses.
- Practical considerations: future projections depend on model assumptions and climate projections; users should consider scenario uncertainty and sensitivity analyses.

## Contact
- Corresponding author: a.j.adeloye@hw.ac.uk

## Key Takeaways for Data Strategy
- The dataset provides a structured, monthly view of reservoir dynamics under historical and projected climates, paired with optimized rule curves and rationing rules.
- It supports evaluation and optimization of reservoir operations and policy planning, with attention to data provenance, model-based projections, and governance around data quality and reuse.