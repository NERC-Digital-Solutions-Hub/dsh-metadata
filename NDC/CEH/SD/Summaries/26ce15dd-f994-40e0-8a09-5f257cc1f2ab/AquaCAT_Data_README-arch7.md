# A set of 14400 summaries of mainland GB peak river flow data describing widespread flooding events as modelled using the Grid-to-Grid hydrological model and UKCP18 meteorological data based on RCP8.5 for 12 members of a perturbed parameter ensemble.

## Authors and funding
- Alison Kay, Vicky Bell, Adam Griffin, Lisa Stewart - UK Centre for Ecology & Hydrology
- Paul Sayers, Sam Carr - Sayers and Partners LLP (SPL) - Applied research consultancy
- Funded by the UK Climate Resilience programme; AquaCAT project led by Sayers and Partners with UKCEH and Vivid Economics

## Date of upload
- 2022-01-20 - Version 0.2

## Overview of data
- Contains 14,400 event summaries describing widespread flooding events across mainland Great Britain.
- Events are modelled using the Grid-to-Grid hydrological model driven by UKCP18 12-member perturbed parameter ensemble (PPE) of the Hadley Centre 12km Regional Climate Model (RCM) under RCP8.5.
- Time slices:
  - Present-day: December 1980 to November 2010 (198012_201011)
  - Future: December 2050 to November 2080 (205012_208011)
- Event definition:
  - A national, pointwise summary of multi-day flooding events.
  - An event is recorded if at least 0.1% of the GB river network's 1 km grid cells exceed a location-specific threshold T(x) on a given day, and this condition is exceeded on average twice per year.
  - Each event is a sequence of consecutive days; only the maximum flow value across the event duration is kept for each location.
  - Flow values are recorded for river-network grid cells; land grid cells are set to -1; sea cells are missing.
- Outputs and units:
  - Flow: maximum river flow (m3/s) within the event.
  - Annual probability of exceedance: probability that a given flow would be exceeded in any given year.
  - Daily probabilities use empirical distributions; for exceedances above T(x), a Generalised Pareto distribution is used.
  - Location coordinates are GB National Grid (Northings/Eastings).

## Data structure and files
- For each of 12 ensemble members and two time periods, a netCDF file is provided:
  - Filename pattern: G2G_events_RCMXX_YSTART_YEND.nc
  - XX: ensemble member (01–15, excluding 02, 03, 14)
  - YSTART/YEND: 198012/201011 (present) or 205012/208011 (future)
- Each file contains:
  - Flow: maximum flow (m3/s) seen at a location over the event duration.
  - Annual probability of exceedance: likelihood of exceedance in any given year.
  - Daily probabilities based on daily flow; annual probabilities derived via Poisson approximation.
  - Locations described by Northings/Eastings (m) on GB National Grid.
  - Flows only on the river network; other land cells are -1; sea cells are missing.

## NetCDF metadata (highlights)
- Four global attributes:
  - RCM: 04
  - period: 198012_201011
  - event_threshold: Annual prob of exceedence < 0.865
  - area_lower_limit: 0.1% minimum coverage
- Data is structured to support analyses of widespread flooding events under climate change scenarios.

## Summary information and statistics
- Summary CSV: summary_RCM**_****12_****11.csv
- Key statistics provided for each event:
  - Nominal starting day (modelled with 30/360-day years)
  - Event ID
  - Event length (days)
  - Maximum annual probability of exceedance across the event
  - Area (km2) exceeding POT2 threshold (flow above threshold exceeded twice a year during the event)
  - Nominal season: DJF (Winter), MAM (Spring), JJA (Summer), SON (Autumn)

## Practical relevance for GIS specialists
- Enables map-based visualization of rare, nationwide flood events under present and future climate scenarios.
- Supports spatial analysis of event frequency, extent, and risk by ensemble member, period, and season.
- Data can be integrated with other GIS layers (hydrology, land cover, infrastructure) to assess exposure and inform resilience planning.
- Large, multi-dimensional dataset requiring careful data management and possible downscaling or subsetting for typical GIS workflows.

## Additional notes and references
- Event-based climate risk context and methodological references are provided in the accompanying papers (in prep) and project reports:
  - Grifﬁn et al., in prep. Widespread flooding events under climate change using a UKCP18 ensemble.
  - Grifﬁn et al., in prep. Comparison of statistical simulation methods for widespread flooding events under climate change.
  - Sayers et al., in prep. Event-based climate change risk assessment.
  - Bell et al., 2007. Use of a grid-based hydrological model and regional climate model outputs to assess changing flood risk.
  - Murphy et al., 2019. UKCP18 land projections: science report.