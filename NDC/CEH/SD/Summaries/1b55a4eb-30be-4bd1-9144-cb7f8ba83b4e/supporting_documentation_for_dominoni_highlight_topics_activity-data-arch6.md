# Field methods: recording of activity of free-living birds

## Overview
- Objective: estimate timing (onset/end) and levels of activity in free-living birds using radio telemetry.
- Species and sites: six passerines (European robin, Eurasian blackbird, great tit, blue tit, dunnock, Common chaffinch) at two urban (Glasgow) and two non-urban forest locations in Scotland.
- Time frame: pre-breeding (Feb–Apr) and post-breeding (Sep–Nov) in 2020 and 2021.
- Data products aim: enable data-driven insights into daily activity patterns and support data reuse across topics.

## Study design and sites
- Urban sites: within Glasgow city boundaries (Kelvingrove Park; Garscube Campus) with non-native trees, impervious surfaces, and high human presence.
- Non-urban sites: SCENE and Sallochy forest near Loch Lomond, forests with native tree species.

## Data collection methods
- Methods: mist-netting to capture birds; tagging with Lotek PicoPip and Pip radio transmitters (weights 0.25–2.20 g, <5% of body weight) mounted on backs with non-toxic glue.
- Tracking setup: two to four automatic Lotek SRX800-D2 receivers per site, scanning each tag every 3 minutes; antennas mounted on rooftops or masts.
- Data captured: date, time, receiver signal strength (dB); potential multiple receivers detecting the same tag.

## Data processing
- Output: 3-minute interval time series of radio detections per bird (tag) and per receiver.
- Signal interpretation: absolute differences in signal strength between consecutive intervals (signal differential); higher values indicate increased movement/activation.
- Aggregation: average signal differential across receivers per site to derive daily activity indicators.

## Estimation of daily onset and end of activity
- Two statistical approaches:
  - bcpa: frequentist behavioural change point analysis; tests for a break in a two-block normal fit, with blocks constrained to at least 30 minutes.
  - bbs: Bayesian regression with one change point, using the R package mcp.
- Temporal constraints:
  - Onset: analyzed within a 6-hour window around sunrise (4 hours before to 2 hours after sunrise).
  - End: analyzed within an 8-hour window around sunset (4 hours before to 4 hours after sunset).
- Relative timing: onset/end times are expressed relative to sunrise/sunset; positive values indicate after, negative values indicate before these events.
- Daily activity duration: computed as end time minus onset time.
- Quality control: required agreement between bcpa and bbs estimates to retain observations.
- Outcome: 2,683 high-quality onset observations from 269 birds; 2,219 high-quality end observations from 256 birds (out of larger totals with lower-quality data).

## Estimation of activity levels throughout the day
- Classification: each 3-minute point labeled as active if signal differential > 10 dB; otherwise inactive.
- Proportion calculations:
  - Diurnal phase: 10:00–16:00 hours.
  - Nocturnal phase: 22:00–02:00 hours.
- Rationale: fixed-time windows to avoid biases from seasonal day-length changes and variable onset/offset times.

## Quality control and data management
- Yearly data checks and upload to a central database.
- Data records linked across files by a unique ID.

## Data structure and files
- Data files:
  - Dominoni_highlight_topics_activity_amount.csv: daytime and nighttime activity amounts.
  - Dominoni_Highlight_topics_onset.csv: onset times from bcpa and bbs.
  - Dominoni_Highlight_topics_offset.csv: offset times (end of activity) from bcpa and bbs.
- Common linkage: all records connected by the ID column.
- Key context fields across files:
  - date, location (SCENE, sallochy, garscube, kelvingrove_park), species, deployment_date, ring_number, age, sex, habitat (urban/forest), season (Winter2020, Autumn2020, Winter2021, Autumn2021), year.
- Onset/offset-specific fields:
  - Onset: bcpa_onset_time, bbs_onset_activity_cp, relative_onset_bbs, relative_onset_bcpa, sunrise, sunrise_time, min/max temperatures, rainfall (for offset: relative_offset_bbs, relative_offset_bcpa).
  - Offset: bcpa_offset_time, bbs_offset_activity_cp, relative_offset_bbs, relative_offset_bcpa, sunset, rainfall, min_temperature.

## Data fields and units (highlights)
- Activity amount file: date, sunrise_time_dec, sunset_time_dec, total_obs_day, non_missing_obs_day, active_day, total_obs_night, non_missing_obs_night, active_night, location, species, deployment_date, ring_number, age, sex, sunrise, season, habitat, year.
- Onset/Offset files: date, onset/offset times from bcpa and bbs, location, species, deployment_date, ring_number, age, sex, sunrise/sunset, season, habitat, year, and supplementary environmental variables (rainfall, min_temperature) with relative timing fields.

## Potential data use and data-support considerations
- Reusability: dataset structured for time-series analyses of diurnal/nocturnal activity and for cross-site or cross-species comparisons.
- Data integration: clear metadata and standardized fields facilitate combining with environmental data or other telemetry datasets.
- Data quality considerations: presence of missing 3-minute intervals when birds are out of range; reliance on agreement between two statistical methods to ensure reliable onset/end estimates.
- Accessibility: central database logging and explicit data structure support sharing outputs as dashboards or reports for broader audiences.