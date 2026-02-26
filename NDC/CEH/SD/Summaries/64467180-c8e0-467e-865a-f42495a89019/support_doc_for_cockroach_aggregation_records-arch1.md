# What has been recorded and what form does the data take?

- The dataset records social aggregations of female cockroaches (Blaptica dubia) across four groups placed on four shelves in an incubator, monitored by cameras and identified via a machine vision algorithm (image_to_assoc).
- Each photograph (aggregation) is associated with one or more cockroach tags, with each detected individual represented by a separate line in the data.
- Four replicates were run, each spanning three weeks with four days per week, and four groups per day, under three humidity conditions (50%, 40%, 30% RH) across different weeks.
- The core output is 192 CSV files (four replicates × three weeks × four days × four groups), containing detections of cockroaches in shelter usage across time.

- Project purpose: to study the plasticity of social network positions in response to humidity, as part of the broader project “The evolution and plasticity of social networks traits.”

- Data collection setting: University of Aberdeen, Zoology building, ground floor insectary.

- Temporal scope: 12 June 2023 to 22 September 2023.

- Experimental setup:
  - 96 adult female cockroaches formed into four groups of 24.
  - Each cockroach weighed and tagged with a unique dorsum tag (digits/letters).
  - Four shelters per group, each shelter monitored by a fixed camera (Akaso V50).
  - Incubator conditions: 28°C with humidity cycles of 50%, 40%, and 30% RH.
  - Each group observed for four hours per trial, with up to 240 photographs per camera (some failures reduced totals).
  - Groups were randomly reassigned to new groups and the process repeated; if a cockroach died, it was replaced to maintain group size.

- Data capture and processing:
  - The custom program image_to_assoc (based on YOLO v5) detects tag digits in photographs to determine which cockroaches used each shelter at each minute.
  - Detections with confidence below 0.95 were removed.
  - To standardize across cameras, the first 200 photographs from each camera (first 200 minutes) were used.
  - Records from the four cameras of a box were combined to produce aggregations for a three-hour twenty-minute period.

- Data structure and metadata:
  - File naming: S1_R1_WK1_1_001.csv (shelf 1, replicate 1, week 1, day 1, aggregation 001); shelves 1–4, replicates 1–4, weeks 1–3 (humidity levels), days 1–4.
  - Each CSV has three columns: V1, V2, V3.
    - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG) corresponding to camera, replicate, week, day, and aggregation number.
    - V2: tag of the cockroach detected (one per line; blank if no detection).
    - V3: detection confidence (0.95–1); NA if no detection.
  - Each line represents a single cockroach detected in an aggregation; an aggregation with multiple individuals results in multiple lines with the same V1 value.
  - The number of lines per file ranges from 1,378 to 3,719 due to varying numbers of successful detections.

- Completeness and data quality notes:
  - 192 CSV files total; line counts vary by successful detections per photograph.
  - Some photographs yielded no detections (V2 blank; V3 NA).
  - Detection reliability depends on camera performance; some cameras failed, affecting the number of usable photographs.
  - The dataset captures up to 200 appearances per individual across the study period.

- Roles and provenance:
  - Data collection and interpretation led by Callum McLean (research associate) and David Fisher (principal investigator).
  - Data intended to be used for analyzing social network traits and their plasticity under varying humidity.

- Practical considerations for analysts:
  - Data are stored in a per-shelf/per-day/per-replicate structure, with a clearly defined naming convention for both files and aggregations.
  - To replicate analyses, be mindful of the 200-minute window used for standardization and the confidence threshold applied during detections.
  - Metadata and provenance enable traceability of each aggregation to its experimental conditions (shelf, replicate, week/humidity, day).