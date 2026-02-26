# Records of social aggregations female cockroaches (Blaptica dubia)

## Overview
- Study focus: recording social aggregations among female Blaptica dubia to study plasticity of social network positions in response to humidity.
- Experimental design: four groups of 24 cockroaches each, placed in four boxes with four shelters and fixed cameras; replicates across humidity treatments (50%, 40%, 30%) over three weeks and four days per week.
- Data aim: generate standardized observations of which individuals use which shelters at given times, enabling comparison over environmental conditions.

## What was recorded and in what form
- Observations: detections of individuals co-occurring in shelters, captured via photographs and translated into aggregations.
- Data product: 192 CSV files containing detections; each line records a single detected cockroach in a photograph.
- Data content per line:
  - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG)
  - V2: cockroach tag (one of 24 identifiers) or blank if none detected
  - V3: detection confidence (0.95–1; NA if no detection)
- Aggregations: each aggregation corresponds to a shelter usage event; a photograph with multiple individuals yields multiple lines for that aggregation.
- Sample scale: 4 replicates × 3 humidity weeks × 4 days × 4 groups per day; each group box contains 4 cameras; each camera takes one photograph per minute.

## Data collection details
- Location and period: University of Aberdeen Zoology building insectary; 12 June 2023 to 22 September 2023.
- Experimental setup: 96 adult female cockroaches per run, divided into four groups of 24; fixed tags on dorsum; four shelters per box; four Akaso V50 cameras above shelters; incubator conditions at 28°C with 50%, 40%, or 30% RH.
- Procedure:
  - Four-hour observation per run.
  - Four replicates, repeated across three humidity levels (50%, 40%, 30%).
  - After each run, individuals were re-assigned to new groups; deaths replaced to maintain 24 per group.
  - Data extraction with image_to_assoc (YOLO v5) to identify tag digits in each photo; detections below 0.95 confidence removed.
  - To equalize camera data, only the first 200 photos from each camera (200 minutes) were used; four cameras per box combined into a single aggregation per 3 hours 20 minutes.

## Data structure and metadata
- Completeness: 192 CSV files; each file length varies (approximately 1,378 to 3,719 lines) depending on successful detections.
- File naming: S1_R1_WK1_1_001.csv format; components indicate shelf, replicate, week (humidity level), day.
- Column definitions:
  - V1: aggregation/photograph name (e.g., A1_R1_WK1_1_001.JPG)
  - V2: tag of cockroach in photograph (one of 24 identifiers; blank if no detection)
  - V3: confidence level (0.95–1); NA if no detection
- Data storage organization: one folder per shelf per day per week per replicate; individual aggregations from four cameras per group per time period are combined.

## Quality assurance and processing
- Quality controls:
  - Only detections with confidence ≥ 0.95 retained.
  - Uniform sampling window by using the first 200 photographs per camera.
- Data provenance:
  - Responsible collectors/analysts: Callum McLean (Research Associate) and David Fisher (Principal Investigator).

## How this dataset supports monitoring objectives
- Provides standardized, auditable environmental data across defined humidity treatments.
- Enables analysis of how environmental conditions influence social network positions and aggregation patterns.
- Data are organized for clear provenance, reproducibility, and potential integration with other environmental datasets.

## Completeness, limitations, and reuse considerations
- Strengths: standardized data collection, explicit metadata, reproducible processing pipeline, explicit handling of missing detections and replacements.
- Limitations: detections depend on camera performance and tag visibility; only the first 200 minutes per camera are used, potentially excluding later activity.
- Reuse considerations: data are structured for integration with environmental health analyses; however, access locations or repositories are not specified beyond local storage conventions in the description.