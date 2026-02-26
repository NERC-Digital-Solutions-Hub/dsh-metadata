# What has been recorded and what form does the data take?

- Overview
  - Dataset of social aggregations for female cockroaches (Blaptica dubia) across four groups placed in four shelters per box, monitored with cameras under varying humidity levels.
  - Purpose: study plasticity of social network traits in response to humidity.

- Experimental design
  - 96 adult females per group, forming four groups of 24.
  - Four replicates (Shelves 1–4; R1–R4).
  - Humidity conditions: 50% (Week 1), 40% (Week 2), 30% (Week 3).
  - Four boxes inside an incubator with controlled temperature and lighting.
  - Each group observed for four days per humidity setting; groups are re-assigned across replicates and humidity weeks.

- Data collection and structure
  - Four fixed shelters per box, each with a dedicated camera (Akaso V50) above it.
  - Cameras captured one photograph every minute; identities determined via a machine-vision program (image_to_assoc, YOLOv5-based).
  - Data captured at minute-level, aggregated per shelter per minute.
  - Records stored as one folder per shelf per day per week per replicate.

- Data format and contents
  - Total: 192 CSV files (4 replicates × 3 weeks × 4 days × 4 groups).
  - Each file contains three columns: V1, V2, V3.
  - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG) indicating camera, replicate, week, day, and aggregation number.
  - V2: cockroach tag detected in the photograph (digits/letters) or blank if none detected.
  - V3: detection confidence (0.95–1); 'NA' if no detections.
  - Each line represents a single detected individual; photos with multiple individuals yield multiple lines with the same aggregation identifier.

- Data processing and quality control
  - Detections with confidence below 0.95 removed (filtered).
  - To equalize across cameras, only the first 200 photographs per camera were used (covering the first 200 minutes of each trial).
  - Aggregations from four cameras of a box are combined for a group over a 3-hour 20-minute window.
  - If an individual died, it was replaced to maintain a group size of 24.

- Metadata and naming conventions
  - Files named: S1_R1_WK1_1_001.csv (S shelf, R replicate, WK week, day, 001 legacy).
  - Aggregation/photograph names (V1) follow: A1_R1_WK1_1_001.JPG, encoding camera, replicate, week, day, and aggregation number.
  - Data length per file varies by number of successful detections (1378–3719 lines).

- Provenance and people
  - Collected and interpreted by Callum McLean (Research Associate) and David Fisher (Principal Investigator).

- Location and timeframe
  - University of Aberdeen Zoology building insectary; data collected 12 June 2023 to 22 September 2023.

- GIS-relevant considerations and potential uses
  - Spatial units: shelters within each incubator box serve as discrete locations; cameras provide micro-spatial provenance.
  - Temporal resolution: minute-by-minute occupancy data; humidity condition and replicate provide experimental strata.
  - Potential map-based analyses: visualize shelter occupancy over time, construct time-sliced occupancy maps, or infer social networks by co-presence within shelters.
  - Data preparation needs for GIS: assign explicit coordinates or layout map for shelves and shelters; align humidity week factor and replicate IDs to metadata; consider transforming to time-series point events or shelter-level occupancy attributes.
  - Limitations: no explicit geographic coordinates beyond shelter IDs; potential biases due to camera failures, strict confidence filtering, and the 200-minute window; per-photo detections may require aggregation to robust social-network metrics.