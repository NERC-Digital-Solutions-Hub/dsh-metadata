# What has been recorded and what form does the data take?

## Overview
- Dataset documenting social aggregations of female cockroaches (Blaptica dubia) to study the plasticity of social network positions in response to humidity.
- Four groups of 24 individuals per box, monitored over multiple humidity conditions (50%, 40%, 30%) across replicates.
- Data collected via fixed cameras capturing one-minute photographs, with automated tag identification to determine groupings (aggregations) each minute.

## Data collection context
- Location: University of Aberdeen Zoology building ground floor insectary.
- Timeframe: 12 June 2023 to 22 September 2023.
- Research purpose: Part of the project "The evolution and plasticity of social networks traits."

## Experimental design
- Subjects: 96 adult female cockroaches, divided into four groups of 24.
- Setup: Four boxes (456mm x 356mm x 120mm) with four shelters; fixed cameras above each shelter (Akaso V50) taking photos every minute.
- Conditions: Incubator at 28°C with 50%, 40%, or 30% relative humidity; four-hour trials per humidity level.
- Replication: Four replicates in total; individuals randomly reassigned to new groups; process repeated to complete four replicates.
- Tagging: Each cockroach tagged on the dorsum with paper tags carrying digits/letters for identification.
- Data generation: Custom image_to_assoc (YOLOv5-based) to extract which cockroaches used which shelter in each minute; detections with confidence below 0.95 are removed.

## Data structure and content
- Records: 192 CSV files total (four replicates, three humidity weeks, four days per week, four groups per day).
- File naming: S1_R1_WK1_1_001.csv format; S = shelf/box, R = replicate, WK = humidity week (1=50%, 2=40%, 3=30%), D = day, 001 = aggregation/photograph index.
- Columns per file:
  - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG) indicating camera, replicate, week, day, and aggregation number.
  - V2: cockroach tag detected in the photograph (24-character set); blank if no individuals detected.
  - V3: detection confidence (0.95–1); NA if no detect.
- Data relationships: Each line is a single detection; an aggregation (photograph) may include multiple lines if multiple individuals are present.
- Coverage: Each camera may contribute up to 200 photographs per trial; some cameras failed, so first 200 minutes were used to standardize across cameras.
- Data volume: Line counts per file range from 1,378 to 3,719 due to varying successful detections.

## Data processing and quality control
- Detection pipeline: image_to_assoc, based on YOLOv5, identifies tags in photos.
- Filtering: only detections with confidence ≥ 0.95 retained.
- Data integration: records from four cameras of a single box are combined to form a single three-hour twenty-minute aggregation window per group per replication.
- Provenance: data collected by Callum McLean (Research Associate) and David Fisher (Principal Investigator); they also interpret the data.

## Completeness and metadata
- Completeness: 192 CSV files across all replicates and humidity conditions; file lengths vary with successful detections.
- Metadata clarity: descriptive file naming and three-column structure provide traceability for camera, replicate, humidity, day, and aggregation.

## Access, reuse, and governance
- Ownership: data collected by named researchers; implications for collaboration and reuse rest on standard research data practices.
- Licensing: no license specified in the provided text; users should contact the principal investigators for access and reuse terms.
- Use case alignment: suitable for constructing dynamic social networks across time windows and examining humidity-driven changes in social positions.

## Key considerations for Data Leaders
- Strengths:
  - Well-documented experimental design with clear replication and humidity treatment.
  - Systematic tagging and minute-by-minute aggregation provide rich temporal social network signals.
  - Explicit data processing steps (YOLOv5-based tag detection, confidence threshold, time-window aggregation) support reproducibility.
  - Metadata and naming conventions enhance discoverability and lineage tracking.
- Challenges and gaps:
  - Data completeness impacted by camera failures; standardized to 200 minutes per camera, which may truncate some observations.
  - Variable file sizes and missing detections create potential gaps in network reconstruction.
  - No explicit data license; licensing and access procedures are not specified in the text.
  Potential actions:
  - Add a formal data dictionary and data-use license to improve discoverability and reuse.
  - Provide a data provenance document outlining preprocessing steps, versioning, and any corrections.
  - Consider publishing a ready-to-use network dataset (per time window) alongside raw detections to lower reuse barriers.