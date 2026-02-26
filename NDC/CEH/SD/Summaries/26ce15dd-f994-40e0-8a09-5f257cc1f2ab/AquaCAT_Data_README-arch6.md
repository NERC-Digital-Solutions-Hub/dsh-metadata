# A set of 14400 summaries of mainland GB peak river flow data describing widespread flooding events as modelled using the Grid-to-Grid hydrological model and UKCP18 meteorological data based on RCP8.5 for 12 members of a perturbed parameter ensemble

- Purpose: Provide national, event-based summaries of widespread flooding events for mainland Great Britain, derived from a gridded hydrological model fed by UKCP18 meteorology under a high-emissions scenario.
- Coverage: Two time-slices — present-day (1980-12 to 2010-11) and future (2050-12 to 2080-11) — across 12 PPE ensemble members.
- Output scale: 14,400 event summaries (600 events per ensemble per period).

## Data generation and event extraction

- Model chain: Grid-to-Grid hydrological model driven by UKCP18 12-member perturbed parameter ensemble (PPE) from the Hadley Centre 12 km Regional Climate Model (RCM) outputs.
- Time resolution and year length: Daily flows; RCM uses 360-day years.
- Event definition: National, pointwise flooding events identified when at least 0.1% of GB river network gridcells exceed a location-specific threshold T(x) (approximately the 0.16% daily quantile) and this condition occurs twice per year on average; events are sequences of consecutive days meeting the criterion.
- Output per event: Maximum flow across the duration for every gridcell on the river network (not limited to cells exceeding the threshold).
- Data interpretation: Daily exceedance probabilities are derived from empirical daily-flow distributions; for flows above the threshold, probabilities use a Generalised Pareto distribution; annual exceedance probabilities use a Poisson approximation.

## Data structure and file formats

- Per ensemble member and period: one netCDF file named G2G_events_RCMXX_YSTART_YEND.nc
  - XX: ensemble member number (01-15, excluding 02, 03, and 14)
  - YSTART_YEND: 198012_201011 for present-day; 205012_208011 for future
- Contents per file:
  - Flow: maximum river-flow (m3/s) for each location during the event
  - Annual probability of exceedance: probability that a given flow value would be exceeded in any year
  - Note: Daily probabilities are based on daily flow; flows exceeding T(x) use Generalised Pareto; annual probabilities use Poisson approximation
- Spatial reference:
  - Locations indexed by Northings and Eastings (in meters) on the GB National Grid
  - Flow values are only recorded on the river network; land cells are -1; sea cells are missing

## NetCDF specifics and metadata

- Global attributes include:
  - RCM: 04
  - period: 198012_201011
  - event_threshold: Annual prob of exceedence < 0.865
  - area_lower_limit: 0.1% minimum coverage
- Summary information files (per ensemble and period):
  - summary_RCM**_****12_****11.csv provides, for each event:
    - Nominal starting day (modelled with 30/360-day years)
    - Event ID
    - Event length (days)
    - Maximum annual probability of exceedance across the event
    - Area (km2) exceeding the POT2 threshold (flows above threshold occur twice yearly at some point during the event)
    - Nominal season: DJF (Winter), MAM (Spring), JJA (Summer), SON (Autumn)

## How to use (data support perspective)

- Access and filter by ensemble member, time period, or season to explore how widespread flooding events may evolve under climate change scenarios.
- Compare present-day vs future event characteristics (frequency, intensity, spatial extent) using the per-event summaries and spatially explicit maximum-flow data.
- Build self-serve data products, dashboards, or reports by leveraging:
  - netCDF event fields (maximum flow by location, exceedance probabilities)
  - per-event metadata (start day, duration, season, area above threshold)
- Consider limitations and interpretation notes:
  - Output is aggregated to event maxima and probabilities derived from model ensembles, with uncertainties reflected by ensemble spread.
  - The definition of a "widespread" event relies on a fixed percentile threshold and annual exceedance criteria, which influences event counts and sizes.
  - Geography is defined on the GB river network; non-river areas are not central to the event sums.

## References

- In-prep and related methodology papers on widespread flooding events under UKCP18 and climate-change risk assessments, and the Grid-to-Grid model framework, providing further detail on methods and validation.