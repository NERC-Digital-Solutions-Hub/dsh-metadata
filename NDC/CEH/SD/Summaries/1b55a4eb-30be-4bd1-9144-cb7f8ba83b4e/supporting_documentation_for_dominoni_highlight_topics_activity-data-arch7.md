# Field methods: recording of activity of free-living birds

## Overview
- Study to estimate timing, duration, and levels of activity in six passerine species using radio telemetry.
- Data collected in 2020–2021 at two urban and two forest locations around Glasgow, Scotland.
- Birds were tagged with lightweight radio transmitters and tracked with ground receivers to generate 3-minute detection time series.

## Study sites and subjects
- Urban sites: Kelvingrove Park and Garscube Campus (Glasgow), characterized by non-native trees, high impervious surface, and strong human presence.
- Non-urban sites: SCENE and Sallochy forest near Loch Lomond, dominated by native trees.
- Target species (six passerines): European robin, Eurasian blackbird, great tit, blue tit, dunnock, common chaffinch.
- Tags: Lotek PicoPip and Pip tags (0.25–2.20 g; <5% of body weight) mounted on backs with non-toxic glue.
- Receivers: 2–4 Lotek SRX800-D2 per site, scanning every 180 seconds, with 2–3 uni-directional Yagi antennas each; typical inter-receiver distance ~239 m.

## Data collection and hardware configuration
- Each receiver logged date/time and signal strength (dB) when a tag was detected.
- Birds could be detected by multiple receivers; terrain and range affected data completeness.
- Automatic time-series of detections created per bird and per receiver (3-minute intervals).

## Data processing and activity inference
- Calculated signal differential: absolute difference in signal strength between consecutive 3-minute intervals; averaged across receivers per site.
- Generated daily activity indicators: onset of activity, end of activity, and daily activity levels inferred from signal differential changes.
- Non-detection periods (birds out of range) treated as missing observations.

## Estimation of daily onset and end of activity
- Two independent methods:
  - Frequentist change-point analysis (bcpa) using two blocks with minimum 30 minutes per block.
  - Bayesian break-stick analysis (bbs) via the R package mcp with one change point.
- Temporal windows:
  - Onset: within six hours around sunrise (4 hours before to 2 hours after sunrise).
  - End: within eight hours around sunset (4 hours before to 2 hours after sunset).
- Relative timings: onset/end times adjusted by sunrise/sunset to produce relative onset/end of daily activity.
- Agreement between methods used to flag high-quality observations.
- Results (high-quality subset):
  - 2,683 onset observations from 269 individuals (out of 5,679 total observations).
  - 2,219 offset observations from 256 individuals (out of 5,769 total observations).

## Estimation of activity levels throughout the day
- Classification per time point: active if signal differential > 10 dB; inactive if < 10 dB.
- Calculated proportion of active points for two windows:
  - Diurnal: 10:00–16:00
  - Nocturnal: 22:00–02:00
- Fixed time windows were used to minimize bias from seasonal day-length changes.

## Quality control and data management
- Yearly quality checks of collected data before uploading to a central database.
- Data files are linked via a common ID and stored as three CSVs:
  - Dominoni_highlight_topics_activity_amount.csv: daytime and nighttime activity counts and rates, location, species, deployment details, sex, habitat, season, year, and related metadata.
  - Dominoni_Highlight_topics_onset.csv: onset times from bcpa and bbs analyses, plus metadata and environmental variables.
  - Dominoni_Highlight_topics_offset.csv: offset times from bcpa and bbs analyses, plus metadata and environmental variables.

## Data structure and key fields (examples)
- Activity amount file: date, sunrise/sunset times, observed vs missing data counts for day/night, active/non-active bout counts, location, species, deployment details, sex, habitat, season, year.
- Onset file: date, bcpa onset time, bbs onset time, location, species, deployment details, sunrise, weather variables (rainfall, min temperature), relative onset times, season coding.
- Offset file: date, bcpa offset time, bbs offset time, location, species, deployment details, sunset, weather variables (rainfall, min temperature), relative offset times, season coding.

## GIS relevance and potential uses
- Spatial coverage across urban-forest gradient enables mapping of diurnal activity patterns by species and site.
- Relative timing to sunrise/sunset supports integration with environmental layers (vegetation, anthropogenic features, light pollution).
- 3-minute resolution provides fine-scale temporal GT data for time-series GIS analyses and visualization.
- Data can support:
  - Heatmaps or choropleth maps of activity timing by site and species.
  - Temporal animated maps showing daily onset/end of activity.
  - Modelling of activity in relation to weather variables (rainfall, temperature) and habitat type.
  - Linking activity data to other GIS datasets (land cover, road density, urban green spaces).

## Limitations and considerations for GIS workflows
- Data fragmentation across three CSV files; requires careful joins by ID to create unified records.
- Incomplete data due to receiver range limitations; quality filtering reduces the available observations.
- Coding schemes (sex, age, season) may require standardization before integration with other datasets.
- Temporal alignment relies on sunrise/sunset times, which may vary by date and location; ensure accurate solar times for relative measures.

## Summary for GIS practitioners
- The dataset provides richly annotated, high-resolution spatiotemporal records of motor activity in six bird species across urban and forest habitats.
- It combines precise receiver deployments, robust dual-method onset/offset estimation, and clear activity-state classifications suitable for map-based analytics and ecological modelling.
- Managed in a centralized database with standardized CSV schemas, enabling GIS workflows for visualization, spatial analysis, and integration with environmental attributes.