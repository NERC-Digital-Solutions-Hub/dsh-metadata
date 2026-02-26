# A set of 14400 summaries of mainland GB peak river flow data describing widespread flooding events as modelled using the Grid-to-Grid hydrological model and UKCP18 meteorological data based on RCP8.5 for 12 ensemble members

## What this dataset is
- A collection of 14,400 event-based summaries of widespread flooding events across mainland Great Britain.
- Generated with the Grid-to-Grid hydrological model driven by UKCP18 12-member perturbed parameter ensemble (PPE) of the Hadley Centre 12 km Regional Climate Model (RCM).
- Two time-slice periods are analysed: present-day baseline (1981–2010) and future (2051–2080).

## Data content and event definition
- Events are national, multi-day flooding events defined by a threshold: at least 0.1% of the 1 km gridcells on the GB river network exceed a location-specific threshold T(x), twice a year on average.
- For each event, only the maximum flow value across the event duration is recorded at each river-network gridcell.
- Data include both maximum event flow (m3/s) and annual probability of exceedance; daily probabilities are empirical, with higher-end exceedances modeled by a Generalised Pareto distribution.
- Annual probabilities are derived from daily probabilities using a Poisson approximation.

## Data structure and organization
- For each of the 12 ensemble members and two time periods, a NetCDF file is provided:
  - File naming: G2G_events_RCMXX_YSTART_YEND.nc
  - XX: ensemble member (01–15, excluding 02, 03, 14)
  - YSTART/YEND: 198012/201011 for present-day; 205012/208011 for future
- Each file contains:
  - Flow: maximum river-flow (m3/s) observed for each gridcell during the event
  - Annual probability of exceedance (AoE) per gridcell
  - Daily probabilities (empirical); exceedances above T(x) modeled with Generalised Pareto; AoE derived via Poisson approximation
  - Location coordinates in Northings/Eastings (GB National Grid); flow data only on the river network; land cells coded as -1; sea missing
- NetCDF metadata includes specific model, period, event-threshold, and area coverage constraints
- A summary CSV (summary_RCM...12...11.csv) provides per-event statistics:
  - Nominal starting day (modelled in 30/360-day years)
  - Event ID
  - Event length (days)
  - Maximum AoE across the event
  - Area (km2) exceeding POT2 threshold (where flow exceeds the threshold at least twice per year during the event)
  - Nominal season (DJF, MAM, JJA, SON)

## Data quality, limitations, and governance
- Model calendar uses 360-day years in the underlying RCM, which affects date interpretation.
- Present-day and future slices are tied to a specific climate-perturbed ensemble, requiring careful interpretation when aggregating across members.
- Data are spatially complete only over the river network; non-river land areas are masked.
- Authors note related in-press and published works for methodological details and validation.

## Access, discoverability, and metadata considerations for data leaders
- Data are organized into clearly named NetCDF files by ensemble member and time-slice, with accompanying per-event summaries in CSV for quick interpretation.
- Global attributes include model configuration, period, event-threshold, and minimum area coverage, aiding reproducibility and metadata consistency.
- The dataset is part of AquaCAT, funded by UK Climate Resilience programme, with documented authorship and project references for traceability.

## Practical applications for decision-making and strategy
- Enables assessment of widespread flood risk under climate change scenarios across GB, through event-level statistics and spatial coverage.
- Supports sensitivity analysis across ensemble members and two time periods to inform adaptation planning and risk management.
- Facilitates cross-disciplinary engagement (data teams, policy colleagues, stakeholders) by providing explicit event definitions, thresholds, and summary metrics.

## References
- Griffin, A.; Stewart, E.; Kay, A.; Sayers, P.; Carr, S. (in prep). Widespread flooding events under climate change using a UKCP18 ensemble.
- Griffin, A.; Stewart, E.; Kay, A.; Sayers, P.; Carr, S. (in prep). Comparison of statistical simulation methods for widespread flooding events in the UK under climate change.
- Sayers, P.; Carr, S.; Griffin, A.; Stewart, E.; Kay, A.; Bell, V. (in prep). Event-based climate change risk assessment - Exploring the impact of changing spatial coherence in fluvial flood risk in the UK.
- Bell, V.A.; Kay, A.L.; Jones, R.G.; Moore, R.J.; Yamazaki, K. (2007). Use of a grid-based hydrological model and regional climate model outputs to assess changing flood risk.
- Murphy, J.; Harris, G.; Sexton, D.; Kendon, E.; Bett, P.; Clark, R.; Yamazaki, K. (2019). UKCP18 land projections: science report. Met Office.