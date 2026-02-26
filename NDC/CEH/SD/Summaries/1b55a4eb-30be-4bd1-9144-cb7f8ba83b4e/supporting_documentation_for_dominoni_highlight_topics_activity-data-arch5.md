# Field methods: recording of activity of free-living birds

- A study using radio telemetry to estimate timing of activity and activity levels in free-living birds
- Species: six passerines (European robin Erithacus rubecula, Eurasian blackbird Turdus merula, great tit Parus major, blue tit Cyanistes caureuleus, dunnock Prunella modularis, Common chaffinch Fringilla coelebs)
- Timeframe: February–April (pre-breeding) and September–November (post-breeding) in 2020 and 2021
- Locations: two urban sites in Glasgow (Kelvingrove Park; Garscube Campus) and two non-urban forest sites near SCENE and Sallochy Forest, approx. 45 km north of Glasgow
- Data governance context: dataset collection and processing designed to enable consistent recording, storage, and discovery across multiple sites and years

## Data collection and provenance

- Capture and tagging:
  - Mist-nets used; individuals marked with metal ring and radio tagged
  - Tags: Lotek PicoPip and Pip (weight 0.25 g–2.20 g), mounted on back with non-toxic glue and cotton fabric
  - Tag weight < 5% of bird’s body weight
- Receivers and sensing:
  - 2–4 automatic Lotek SRX800-D2 receivers per site
  - Each receiver scans each tag every 180 seconds
  - 2–3 uni-directional Yagi antennas per receiver, positioned on rooftops or 8–10 m masts
  - Mean receiver separation: 239 m (range 65–697 m)
- Data captured:
  - 3-minute interval time series of detections per bird (per receiver)
  - Each detection includes date/time stamp and signal strength (dB)
  - Birds may be out of range or detected by multiple receivers
- Data storage:
  - Data checked yearly and uploaded to a central database

## Data processing and analysis

- Signal changes to infer activity:
  - Compute signal differential: absolute difference in signal strength between consecutive 3-minute intervals
  - Average differential across receivers per site to obtain a 3-minute time series per bird
  - Static roosting yields near-zero differential; increasing differential indicates activity
- Estimation of daily onset and end of activity:
  - Methods used:
    - Frequentist behavioural change point analysis (bcpa)
    - Bayesian single-change-point (Broken-Stick) using R package mcp (bbs)
  - Time-window constraints:
    - Onset: within six-hour window around sunrise (four hours before to two hours after sunrise)
    - End: within eight-hour window around sunset (four hours before to four hours after sunset)
  - Relative timing:
    - Onset/end times adjusted by sunrise/sunset times
    - Positive values: activity begins/ends after sunrise/sunset; negative values: before
  - Quality control:
    - Require agreement between bcpa and bbs estimates
    - Resulting high-quality observations: 2,683 onset observations from 269 individuals (out of 5,679 total); 2,219 end observations from 256 individuals (out of 5,769 total)
- Estimation of daily activity levels:
  - Classification per time point: active if signal differential > 10 dB; inactive if < 10 dB
  - Compute proportions of active points during:
    - Diurnal phase: 10:00–16:00
    - Nocturnal phase: 22:00–02:00
- Data quality and validation:
  - Additional quality control steps to ensure reliability of onset/end estimates
  - All data points are aligned with consistent 3-minute intervals and site-specific contexts

## Data products and structure

- Three main data files:
  - Dominoni_highlight_topics_activity_amount.csv: activity amount during day and night
  - Dominoni_Highlight_topics_onset.csv: onset of daily activity
  - Dominoni_Highlight_topics_offset.csv: end of daily activity
- Shared linking field:
  - ID column links records across files
- Core fields and metadata (examples):
  - ID, date, sunrise_time_dec, sunset_time_dec, total_obs_day, non_missing_obs_day, active_day, nonactive_day, total_obs_night, non_missing_obs_night, active_night, nonactive_night, location, species, deployment_date, ring_number, age, sex, sunrise, season, habitat, season_clean, year
  - Onset file includes bcpa_onset_time, bbs_onset_activity_cp, relative_onset_bbs, relative_onset_bcpa, location, species, deployment_date, ring_number, age, sex, sunrise, season, habitat, season_clean, year, etc.
  - Offset file includes bcpa_offset_time, bbs_offset_activity_cp, relative_offset_bbs, relative_offset_bcpa, sunset, season, habitat, season_clean, year, etc.
- Data fields describe:
  - Temporal context (date, times, sunrise/sunset, season)
  - Spatial context (location, habitat)
  - Biological context (species, ring number, age, sex)
  - Recording context (deployment date, year)
  - Derived metrics (onset/end times, relative timing, activity amount, diurnal/nocturnal activity)

## Data governance, quality, and reuse considerations

- Provenance and lineage:
  - Data originate from field tagging, receiver-based detections, and two statistical methods for onset/end estimation
  - Central database houses yearly quality checks and consolidated records
- Standards and interoperability:
  - Consistent 3-minute resolution and standardized computations of signal differentials
  - Use of two independent methods for onset/end to improve reliability
  - Metadata-rich fields for location, habitat, season, and individual biology
- Quality and limitations:
  - Data gaps due to receiver range limitations; some 3-minute intervals missing when birds out of range
  - Potential biases from definitional thresholds (e.g., 10 dB for activity) and fixed time windows relative to sunrise/sunset
  - Relationships across years and sites captured through explicit deployment dates and site metadata
- Governance and sustainability:
  - Regular data checks and uploads to a central repository support data discoverability and reuse
  - Rich data dictionary via the detailed field definitions facilitates proper interpretation and integration with other datasets
- Practical implications for data stewards:
  - Enforce consistent data dictionaries, unit conventions, and coding schemes for location, habitat, season, and sex
  - Maintain clear provenance, versioning, and update schedules for the central database
  - Consider documenting data limitations and assumptions (e.g., detection gaps, threshold choices) for downstream users
  - Facilitate data discovery by preserving cross-file linkages through the ID field and providing end-user guidance on interpreting relative onset/end times

## Summary implications for use

- Provides a detailed, multi-site dataset of diurnal and nocturnal activity patterns across six bird species, with robust onset/end detection using two complementary methods
- Enables analyses of temporal activity patterns relative to sunrise/sunset and habitat type (urban vs. forest)
- Supports research on activity budgets, behavioral ecology, and responses to urbanization, with a well-documented data processing pipeline suitable for data stewardship and reuse across organizations.