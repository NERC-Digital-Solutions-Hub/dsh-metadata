# What has been recorded and what form does the data take?

- What was recorded
  - Records of social aggregations among female cockroaches (Blaptica dubia).
  - Four groups per shelf in an incubator; each group monitored by four cameras.
  - Photos taken under shelters; identities extracted with the image_to_assoc machine vision algorithm.
  - Each aggregation (photograph) has a unique identifier; each cockroach within a group has a unique tag.

- Data collection design
  - Four replicates; each replicate includes four weeks: two weeks at 50% RH, one week at 40% RH, and one week at 30% RH, with each week lasting four days.
  - Groups of 24 cockroaches formed into four groups; four shelters per group; recorded for four hours per session across four days per humidity level.
  - After each set, individuals could be reassigned to new groups; if an individual died, a replacement was used.
  - Incubator conditions: 28°C with lights on; humidity levels as above.

- Data capture and processing
  - Cameras: four per group; a photograph taken every minute per shelter.
  - Identification: images processed with image_to_assoc (YOLOv5) to detect tag digits; detections filtered to confidence ≥ 0.95.
  - Sampling: to equalize data across cameras, only the first 200 photographs from each camera were used.
  - Aggregations: records from the four cameras per box are combined to yield aggregations for a group over a 3 hours 20 minutes period.

- Data organization and storage
  - Location: University of Aberdeen Zoology building ground floor insectary.
  - Data files: 192 CSV files total (four replicates, three weeks, four days per week, four groups per day).
  - File lengths: 1,378 to 3,719 lines (vary due to number of successful detections per photograph).

- Metadata and file structure
  - File naming: S1_R1_WK1_1_001.csv (S shelf, R replicate, WK week [1=50% RH, 2=40%, 3=30%], 1 day, 001).
  - Each CSV has three columns with headers V1, V2, V3:
    - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG)
    - V2: cockroach tag detected (one per line; blank if none)
    - V3: detection confidence (0.95–1.0); NA if no detection
  - Data structure: each line represents a single detection; a photograph with multiple individuals yields multiple lines; an individual can appear in up to 200 photographs over time.

- Data provenance and responsibility
  - Project aim: to study the evolution and plasticity of social networks traits and the plasticity of social network positions under different humidity conditions.
  - Responsible researchers: Callum McLean (Research Associate) and David Fisher (Principal Investigator) collected and interpreted the data.

- Data quality and caveats
  - Detections with confidence below 0.95 are excluded.
  - Some cameras may have failed; only the first 200 photographs per camera were retained to standardize across devices.
  - Metadata was primarily embedded in V1 (image/aggregation identifiers) and V2 (tags); additional derived fields (e.g., shelf, week, replicate, humidity) require parsing from file names or V1.