# Field methods: recording of activity of free-living birds

## Objective
- Estimate timing and levels of activity in free-living birds using radio telemetry.
- Study six passerine species across two urban and two non-urban forest locations during pre-breeding and post-breeding phases (2020–2021).

## Study design and locations
- Urban sites: Glasgow city boundaries (Kelvingrove Park; Garscube Campus).
- Non-urban sites: SCENE and Sallochy forest near Loch Lomond.
- Species: European robin, Eurasian blackbird, great tit, blue tit, dunnock, Common chaffinch.
- Timeline: February–April (pre-breeding) and September–November (post-breeding) in 2020 and 2021.
- Animals: Individually marked with metal rings and radio tags; tags weighed 0.25–2.20 g (≤5% of body weight).

## Field methods
- Capture: Mist nets; tags affixed with non-toxic glue and fabric.
- Tagging equipment: Lotek PicoPip and Pip tags; unique RF signals; receiver network: two to four SRX800-D2 receivers per site with 2–3 Yagi antennas.
- Data collection: Receivers scan each tag every 180 seconds; recordings include date/time and signal strength (dB); birds may be detected by multiple receivers or be out of range.

## Data processing: signal differentials
- Create a 3-minute time series of detections per bird per receiver.
- Compute signal differential: absolute difference in signal strength between consecutive 3-minute intervals; average across receivers per site to obtain a per-bird daily signal differential time series.
- Interpretation: low differential indicates inactivity; higher differential indicates activity.

## Estimation of daily onset and end of activity
- Two statistical approaches applied to 3-minute time series per bird:
  - Frequentist behavioural change point analysis (bcpa): two-block log-likelihood change-point with blocks of at least 30 minutes; sliding window across time.
  - Bayesian break-stick analysis (bbs) using R package mcp with one change point.
- Windows for daily timing:
  - Onset of activity: within 4 hours before to 2 hours after sunrise (6-hour window; relative onset = onset minus sunrise).
  - End of activity: within 4 hours before to 4 hours after sunset (8-hour window; relative end = end minus sunset).
- Relative metrics: positive values = activity after sunrise/sunset; negative values = before.
- Duration: end time minus onset time per day per individual.
- Quality control: require agreement between bcpa and bbs methods to deem observations reliable.
- Outcomes: 2,683 high-quality onset observations (269 individuals) and 2,219 high-quality end observations (256 individuals) from larger initial datasets.

## Estimation of activity levels throughout the day
- Classification: time point labeled as 'active' if signal differential > 10 dB; 'inactive' if < 10 dB.
- Activity metrics: proportion of time points active during:
  - Diurnal window: 10:00–16:00.
  - Nocturnal window: 22:00–02:00.

## Data quality control
- Annual verification of data; yearly data upload to a central database.

## Data structure and files
- Data are organized into three CSV files linked by ID:
  - Dominoni_highlight_topics_activity_amount.csv: daytime and nighttime activity amounts, counts of observations, active/inactive bouts, location, species, tagging details, sex, season, habitat, year, and related metadata.
  - Dominoni_Highlight_topics_onset.csv: onset times from bcpa and bbs, location, species, tagging details, sun times, season, habitat, year, and environmental variables (rainfall, min temperature), plus relative onset values.
  - Dominoni_Highlight_topics_offset.csv: offset times from bcpa and bbs, location, species, tagging details, sunset times, season, habitat, year, environmental variables, plus relative offset values.
- Key fields include date, sunrise/sunset times, deployment details, age/sex, habitat (urban/forest), season (pre/post-breeding), year, and environmental variables (rainfall, min_temperature).
- Records are connected via the ID column.

## Relevance for environmental monitoring
- Produces standardised, codified measures of daily activity timing and levels across multiple sites and species.
- Data can support monitoring of environmental health indicators, urban–rural contrasts, and responses to climate-related variables (rainfall, temperature).
- Clear pathways to combine with other datasets and share underlying data to enhance environmental monitoring and policy evaluation.