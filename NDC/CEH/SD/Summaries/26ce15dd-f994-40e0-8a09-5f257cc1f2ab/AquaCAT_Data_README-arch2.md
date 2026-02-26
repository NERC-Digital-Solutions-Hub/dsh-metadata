# Widespread flooding events under climate change using a UKCP18 ensemble

## Aim and context for analysts
- Provides standardized, modelled summaries of widespread flooding events to monitor environmental health and policy performance under climate change.
- Generated as part of the UK Climate Resilience programme, AquaCAT project led by Sayers & Partners with UKCEH and Vivid Economics.

## Data and modelling overview
- 14,400 event summaries describing peak river flows across mainland Great Britain.
- Modelling chain:
  - Grid-to-Grid hydrological model driven by UKCP18 12-member perturbed parameter ensemble (PPE) from Hadley Centre 12 km Regional Climate Model (RCM).
  - Baseline period: 1981/12 to 2010/11; Future period: 2050/12 to 2080/11.
- Each event is a national, grid-based, multi-day flooding episode captured as a sequence of consecutive days meeting a threshold.

## Event generation and extraction (how events are defined)
- Threshold criterion:
  - At least 0.1% of the GB river-network gridcells exceed a location-specific threshold T(x) on a given day, which is exceeded on average twice per year (≈ 0.16% quantile).
- An event:
  - A sequence of consecutive days where the threshold criterion holds.
  - For each event, only the maximum daily flow over the event duration is kept per gridcell on the river network.
  - Flow is recorded for all river-network gridcells, not only those exceeding the threshold.
- Outputs include maxima and the spatial footprint across the river network.

## Data structure and files
- For each of 12 ensemble members and two time periods, one netCDF file:
  - Filename format: G2G_events_RCMXX_YSTART_YEND.nc
  - XX: ensemble member number (01–15, excluding 02, 03, 14)
  - YSTART, YEND: 198012–201011 (present), 205012–208011 (future)
- Contents per file:
  - Flow: maximum river-flow (m3/s) observed for each location over the event duration.
  - Annual probability of exceedance (APoE): probability a given flow value is exceeded in any year.
  - Daily probabilities for threshold exceedances (based on empirical daily distribution; GP distribution used for exceedances).
  - Annual probabilities derived via Poisson approximation.
  - Locations described by Northings/Eastings (GB National Grid). Flow recorded only on the river network; land gridcells marked -1; sea values missing.

## NetCDF and metadata
- Global attributes:
  - RCM: 04
  - period: 198012_201011
  - event_threshold: Annual prob of exceedence < 0.865
  - area_lower_limit: 0.1% minimum coverage
- Basic metadata included in each NetCDF to support interoperability and reproducibility.

## Summary information and outputs
- Summary CSVs (summary_RCM**_****12_****11.csv) provide key statistics for each event:
  - Nominal starting day (modelled with 360-day year assumption)
  - Event ID
  - Event length (days)
  - Maximum annual probability of exceedance across the event
  - Area (km2) exceeding the POT2 threshold (i.e., area where flow exceeded at least twice per year during the event)
  - Nominal season: DJF (Winter), MAM (Spring), JJA (Summer), SON (Autumn)

## Data provenance, validation, and references
- Documentation and validation are described across three in-press papers and project reports:
  - Widespread flooding events under climate change using a UKCP18 ensemble (in prep)
  - Comparison of statistical simulation methods for UK flooding under climate change (in prep)
  - Event-based climate change risk assessment – spatial coherence in UK fluvial flood risk (in prep)
- Foundational methodology references include: Grid-to-Grid model (Bell et al. 2007) and UKCP18 land projections (Murphy et al. 2019).

## Access and use considerations for analysts
- Datasets are designed for standardised monitoring, quality assurance, and reuse alongside other environmental data.
- Encourages linking the event-based outputs with additional environmental, societal, or policy datasets to enhance data value and accessibility.
- Suitable for population-wide risk assessment, policy performance monitoring, and scenario analysis over time.