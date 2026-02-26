# Field methods: recording of activity of free-living birds

- Objective
  - Estimate timing of activity, daily onset and end of activity, and activity levels in six passerine species using radio telemetry across urban and non-urban forest sites during pre- and post-breeding phases in 2020 and 2021.

- Study design and locations
  - Species: European robin, Eurasian blackbird, great tit, blue tit, dunnock, common chaffinch.
  - Sites: two urban (Glasgow city—Kelvingrove Park; Garscube Campus) and two non-urban forests (SCENE and Sallochy) in Scotland.
  - Sampling periods: pre-breeding (Feb 2–Apr 16) and post-breeding (Sept 30–Nov 5).
  - Habitat categories: urban vs forest.

- Data collection (tagging and telemetry)
  - Birds captured with mist nets, marked with metal rings, and fitted with Lotek PicoPip or Pip radio tags (weight 0.25–2.20 g; <5% of body weight).
  - Receivers: two to four automatic Lotek SRX800-D2 receivers per site, scanning each tag every 180 seconds; each receiver with two to three uni-directional Yagi antennas.
  - Data recorded per detection: date/time stamp and radio signal strength (dB); birds may be detected by multiple receivers or be out of range.

- Data processing and activity signals
  - Generated 3-minute interval time series of detections per tag and per receiver.
  - Calculated signal differential as the absolute change in signal strength between consecutive 3-minute intervals; averaged across receivers per site.
  - Active vs inactive classification: activity inferred when signal differential > 10 dB; inactive when ≤ 10 dB.
  - Missing data: due to range limitations when birds are out of range of receivers.

- Estimation of daily onset and end of activity
  - Methods used:
    - bcpa: frequentist behavioural change point analysis (two-block normal fits; 30-minute minimum block; 3-minute step).
    - bbs: Bayesian Broken-Stick analysis using R package 'mcp' (one change point).
  - Temporal constraints:
    - Onset: within six hours around sunrise (four hours before to two hours after sunrise); relative onset = onset time − sunrise.
    - End: within eight hours around sunset (four hours before to four hours after sunset); relative end = end time − sunset.
  - Activity duration: difference between onset and end times for each individual-day.
  - Quality control: only observations with agreement between bcpa and bbs methods retained for downstream use; results include a dataset of high-quality onset and end observations.

- Quality control and data management
  - Annual data checks and uploading to a central database.
  - Two independent methods used to assess reliability; agreement between methods governs data inclusion.

- Data structure and variables
  - Three CSV files:
    - Dominoni_highlight_topics_activity_amount.csv: daytime and nighttime activity counts; includes ID, date, sunrise/sunset times, total/non-missing datapoints, active/non-active bouts, location, species, deployment details, sex, habitat, season, year, and other metadata.
    - Dominoni_Highlight_topics_onset.csv: onset times from bcpa and bbs; includes ID, date, onset times, location, species, deployment details, age, sex, sunrise, season, habitat, year, and environmental covariates (rainfall, min_temperature); relative onset to sunrise provided for bcpa and bbs.
    - Dominoni_Highlight_topics_offset.csv: offset (end) times from bcpa and bbs; similar fields as onset, plus sunset and relative offsets.
  - Key fields and units:
    - Time data: hours after midnight (e.g., bcpa_onset_time, bbs_onset_activity_cp).
    - Dates: dd/mm/yyyy; times for sunrise/sunset in hours.
    - Environment: rainfall (mm), min_temperature (°C).
    - Metadata: location (SCENE, sallochy, garscube, kelvingrove_park); habitat (urban, forest); season (Winter2020, Autumn2020, Winter2021, Autumn2021); year (yyyy).
  - Linkage: records connected by ID across files.

- Key findings and data yields
  - After quality filtering, 2,683 high-quality onset observations from 269 individuals (out of 5,679 total observations) and 2,219 high-quality offset observations from 256 individuals (out of 5,769 total observations) are available for analyses.

- Relevance for data governance and strategy (Data Leaders perspective)
  - Demonstrates end-to-end data lifecycle: from field collection and tagging to centralized storage, processing, and multi-method validation.
  - Highlights importance of metadata richness (location, habitat, season, deployment details, demographic info) for cross-site analyses and reuse.
  - Emphasizes data quality and reliability through dual-method validation and explicit inclusion criteria, aligning with standards for data accuracy and reproducibility.
  - Provides a structured data model with clear data products (onset, offset, activity amount) that supports discoverability, interoperability, and potential sharing across networks.
  - Illustrates challenges common to data ecosystems: data fragmentation across habitats/sites, missing data due to receiver range, and need for consistent metadata and standardized units.