# Field methods: recording of activity of free-living birds

- Objective: Estimate timing of activity and levels of activity in six passerine species using radio telemetry; capture via mist-nets, tag birds, and monitor activity patterns across urban and non-urban forest locations over 2020–2021 to support analyses of diurnal/nocturnal activity and onset/offset timings.

- Study design
  - Species: European robin (Erithacus rubecula), Eurasian blackbird (Turdus merula), great tit (Parus major), blue tit (Cyanistes caeruleus), dunnock (Prunella modularis), Common chaffinch (Fringilla coelebs).
  - Locations: Two urban sites in Glasgow (Kelvingrove Park; Garscube Campus) and two non-urban forest sites near SCENE and Sallochy forest (Loch Lomond area).
  - Deployment: February–April (pre-breeding) and September–November (post-breeding) in 2020 and 2021.
  - Tags: Lotek PicoPip and Pip radio tags (0.25–2.20 g), affixed with non-toxic glue; tags emit unique radio frequencies.
  - Receivers: Two–four Lotek SRX800-D2 receivers per site with 2–3 uni-directional Yagi antennas; receivers scanned each tag every 180 seconds; mean inter-receiver distance ~239 m (range 65–697 m).

- Field methods
  - Capture and tagging: Birds caught via mist-nets, individually marked with metal rings and radio-tagged; tag weight kept below 5% of body weight.
  - Data collection: Each detection logged with date, time, and signal strength (dB); detections may come from multiple receivers if birds are within range of more than one.
  - Data structure: Data generated as a 3-minute interval time series of detections per bird and per receiver; processed to derive activity metrics.

- Data processing and activity estimation
  - Signal processing: Compute absolute difference in radio signal strength between consecutive 3-minute intervals (signal differential); average across receivers for each site per bird to obtain a 3-minute time series of activity signals.
  - Onset and end of daily activity: Use two statistical approaches on the 3-minute time series per bird
    - Frequentist behavioural change point analysis (bcpa): Split time series into two blocks, fit normals, compute log-likelihoods, and identify change points with blocks lasting at least 30 minutes; window limited to six hours around sunrise for onset.
    - Bayesian broken-stick analysis (bbs) via R package mcp: One-change-point regression model; onset constrained similarly to around sunrise.
    - Relative timing: Subtract sunrise/sunset times to obtain relative onset (positive = after sunrise; negative = before) and relative end (positive = after sunset); compute diurnal duration as end minus onset.
    - Quality control: Require agreement between bcpa and bbs estimates; retain only high-quality onset (2,683 observations from 269 birds) and end (2,219 observations from 256 birds) data.
  - Activity levels throughout the day: Classify each 3-minute point as active if signal differential > 10 dB, otherwise inactive; compute:
    - Proportion of active points during diurnal window (10:00–16:00).
    - Proportion of active points during nocturnal window (22:00–02:00).
  - Temporal consistency: Fixed windows used to avoid biases from variable day length and onset/end timing.

- Quality control and data management
  - Annual data checks and uploading to a central database.
  - Data files produced:
    - Dominoni_highlight_topics_activity_amount.csv: daily daytime/nighttime activity totals and bouts; fields include date, sunrise/sunset times, observed vs missing data, counts of active/inactive bouts, location, species, deployment details, sex/age, season, habitat, and year.
    - Dominoni_Highlight_topics_onset.csv: onset times estimated by bcpa and bbs; fields include date, onset times, location, species, deployment, age/sex, sunrise, season, habitat, year, and derived relative onset.
    - Dominoni_Highlight_topics_offset.csv: offset times estimated by bcpa and bbs; fields include date, offset times, location, species, deployment, age/sex, sunset, season, habitat, year, rainfall, min_temperature, and relative offset.

- Data structure and units
  - ID: unique record identifier; date in dd/mm/yyyy format.
  - Times: hours after midnight; sunrise/sunset times included; relative onset/offset times expressed relative to sunrise/sunset.
  - Locations: SCENE, sallochy, garscube, kelvingrove_park.
  - Habitat: urban or forest.
  - Seasons: pre_breeding (winter/autumn labels apply to season field), post-breeding; year-specific labeling (Winter2020, Autumn2020, Winter2021, Autumn2021).
  - Additional fields: deployment_date, ring_number, age code, sex (unknown/male/female), rainfall, min_temperature, and season_clean (pre_breeding/post_breeding).

- Notable considerations and limitations
  - Data gaps: Some 3-minute intervals are missing when birds are out of receiver range.
  - Detection variability: Range of receivers and environmental factors can influence detectability and signal strength.
  - Thresholds and windows chosen to align with diurnal patterns and to minimize biases due to seasonal day-length changes.
  - Data sensitivity: While not a primary focus here, potential data access challenges and domain expertise may be necessary for deeper interpretation and synthesis across sites or species.