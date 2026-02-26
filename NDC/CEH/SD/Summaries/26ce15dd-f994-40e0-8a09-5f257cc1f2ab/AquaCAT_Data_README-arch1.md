A set of 14400 summaries of mainland GB peak river flow data describing widespread flooding events as modelled using the Grid-to-Grid hydrological model and UKCP18 meteorological data based on RCP8.5 for 12 members of a perturbed parameter ensemble.

## Overview
- Describes 14400 summaries of mainland Great Britain peak river flow events.
- Generated with the Grid-to-Grid hydrological model driven by UKCP18 meteorological data (RCP8.5) using a 12-member perturbed parameter ensemble (PPE).
- Time periods: baseline 1981-2010 and future 2051-2080.
- Events are national, multi-day flooding episodes; inputs include gridded precipitation, temperature, and potential evaporation.

## Event generation and extraction
- Grid-to-Grid uses daily gridded precipitation, temperature, and PE from UKCP18 PPE (Hadley Centre 12 km RCM) to produce daily gridded flow.
- An event is selected if at least 0.1% of the GB river-network gridcells exceed a location-specific threshold T(x) at least twice per year on average.
- Each event is a sequence of consecutive days; only the maximum flow across the event duration is stored for each gridcell.
- For each location x, records include flow maxima across the event; events across all 12 ensemble members and two periods are included.

## Data structure and NetCDF details
- For each of 12 ensemble members and two time periods, a netCDF file named G2G_events_RCMXX_YSTART_YEND.nc contains:
  - XX: ensemble member (01–15, excluding 02, 03, 14)
  - YSTART/YEND: 198012/201011 (present) or 205012/208011 (future)
- File contents:
  - Flow value: maximum flow (m3/s) observed at a location over the event duration.
  - Annual probability of exceedance: probability that a given flow value is exceeded in any year (daily-based; Poisson approximation for annual probabilities).
  - Probabilities are derived from daily distributions; for flows above threshold a Generalised Pareto distribution is used.
  - Location coordinates are Northings/Eastings (GB National Grid); flow recorded only on the river network; -1 on land; missing on sea.

## NetCDF metadata and access
- NetCDFs include specific tows/wgs84 placeholders and four global attributes:
  - RCM: 04
  - period: 198012_201011 or 205012_208011
  - event_threshold: Annual prob of exceedence < 0.865
  - area_lower_limit: 0.1% minimum coverage

## Summary information
- Summary CSV: summary_RCM**_****11.csv (and related) provides key statistics per event, including:
  - Nominal starting day (modelled on 30/360-day years)
  - Event ID
  - Event length (days)
  - Maximum annual probability of exceedance across the event
  - Area (km2) exceeding the POT2 threshold (flow > threshold and exceeded twice yearly at some point)
  - Nominal season: DJF, MAM, JJA, SON

## Thresholds and definitions
- event_threshold: Annual probability of exceedance < 0.865
- area_lower_limit: 0.1% minimum area coverage required for inclusion

## References
- In-prep papers detailing widespread flooding events under climate change and methodological comparisons.
- Foundational references for the grid-based model and UKCP18 land projections, including a 2007 International Journal of Climatology study.

## Authors and funders
- Authors: Alison Kay, Vicky Bell, Adam Griffin, Lisa Stewart (UK Centre for Ecology & Hydrology); Paul Sayers, Sam Carr (Sayers and Partners LLP)
- Funders: UK Climate Resilience AquaCAT project; UKCEH and Vivid Economics
- Related project information: AquaCAT project page (Sayers and Partners) with project details.