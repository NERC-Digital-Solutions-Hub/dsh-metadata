# Field methods: recording of activity of free-living birds

- Objective and scope
  - Estimate timing of activity and overall activity levels in free-living birds using radio telemetry.
  - Comparative design across two urban (Glasgow) and two non-urban forest locations in Scotland.
  - Year range: 2020–2021, with fieldwork during pre-breeding (Feb–Apr) and post-breeding (Sept–Nov).
  - Target taxa: six passerine species (European robin, Eurasian blackbird, great tit, blue tit, dunnock, common chaffinch).

- Field sampling design
  - Capture and tagging: mist-netted birds marked with metal rings and radio tags (Lotek PicoPip/Pip), weight <5% of body weight.
  - Tags: lightweight (0.25–2.20 g) and emit unique radio frequencies.
  - Telemetry hardware: two to four automatic Lotek SRX800-D2 receivers per site with 2–3 uni-directional antennas each.
  - Receiver configuration: scans every 180 seconds; detections recorded with date/time stamps and signal strength.
  - Spatial setup: receivers installed on rooftops or 8–10 m masts at mean inter-receiver distance of ~239 m (range 65–697 m).

- Data generation and preprocessing
  - Produces a 3-minute interval time series of detections per bird and per receiver.
  - Signal differential: absolute difference in signal strength between consecutive intervals; used to infer movement/activation.
  - Activity inference: constant signal strength implies roosting; increasing signal differential suggests activity.

- Estimation of daily onset and end of activity
  - Two independent change-point approaches:
    - Frequentist behavioural change point analysis (bcpa) using two-block normal fits and log-likelihood comparison.
    - Bayesian broken-stick analysis (bbs) via R package mcp for a single change point.
  - Temporal constraints:
    - Onset: restricted to a 6-hour window around sunrise (4 hours before to 2 hours after sunrise).
    - End: restricted to an 8-hour window around sunset (4 hours before to 4 hours after sunset).
  - Relative timing: onset/end times adjusted by sunrise/sunset to yield relative onset/end; positive values indicate post-sunrise/sunset activity.
  - Diurnal activity duration: computed as end minus onset per individual per day.
  - Quality control: retained observations only if both methods agree sufficiently; yielded high-quality datasets:
    - Onset: 2,683 observations from 269 individuals (out of 5,679 total).
    - End: 2,219 observations from 256 individuals (out of 5,769 total).

- Estimation of activity levels
  - Pointwise activity classification: active if signal differential > 10 dB; otherwise inactive.
  - Metrics: proportion of active points during diurnal (10:00–16:00) and nocturnal (22:00–02:00) windows.
  - Fixed-time-window approach to minimize biases from changing day length and individual timing.

- Data quality control and management
  - Annual data checks with uploads to a central database.
  - Ensures consistent data handling and traceability across years and sites.

- Data structure and outputs
  - Three linked CSV data files:
    - Dominoni_highlight_topics_activity_amount.csv: daytime and nighttime activity counts and metadata.
    - Dominoni_Highlight_topics_onset.csv: onset times from bcpa and bbs analyses.
    - Dominoni_Highlight_topics_offset.csv: end times from bcpa and bbs analyses.
  - Key fields per dataset include: ID, date, time estimates (onset/offset), location, species, deployment date, ring number, age, sex, sunrise/sunset times, season, habitat (urban/forest), season_clean (pre_breeding/post-breeding), year, and, for onset/offset files, relative onset/offset measures and environmental covariates (rainfall, min_temperature).

- Location and species details
  - Locations: SCENE, Sallochy, Garscube, Kelvingrove Park (urban vs forest habitats).
  - Urban sites: within Glasgow city; forest sites: SCENE area and Sallochy near Loch Lomond.
  - Species coverage provides cross-site comparability of activity timing and levels.

- Relevance for monitoring and governance
  - Demonstrates end-to-end monitoring workflow: from field data collection to processing, quality control, and structured data outputs.
  - Uses objective, parallel analytical approaches (bcpa and bbs) to determine activity timing, enabling reproducibility and cross-study comparability.
  - Incorporates explicit metadata, standardized time windows, and central data storage to support data stewardship, transparency, and long-term monitoring viability.

- Considerations and limitations
  - Data gaps due to receiver range and bird detectability may affect continuity.
  - Fixed thresholds (e.g., 10 dB for activity) and time-window choices influence results and should be documented for interpretation.
  - Requires ongoing data governance to ensure metadata completeness and data accessibility across sites and years.