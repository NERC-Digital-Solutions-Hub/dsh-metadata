# What has been recorded and what form does the data take?

## Overview and purpose
- Records of social aggregations in female cockroaches (Blaptica dubia) to study the plasticity of social network positions in response to humidity.
- Part of a project on the evolution and plasticity of social networks traits.

## Study setup and data collection environment
- Location: University of Aberdeen Zoology building ground floor insectary.
- Timeframe: 12/6/23 to 22/09/23.
- Experimental design: four groups of 24 cockroaches (total 96) forming four replicates; three humidity levels (50%, 40%, 30%) applied across weeks.
- Housing: each group in a box with four shelters; four cameras mounted above shelters.
- Conditions: incubator at 28°C with specified humidity; lights on.

## Data collection protocol
- Photographs: one fixed camera per shelter; one photo per minute.
- Identification: each cockroach tagged on the dorsum; IDs extracted from photos using a machine-vision program (image_to_assoc, YOLOv5-based).
- Duration per run: four hours per session; repeated across four days per humidity level, with group re-assignment between runs.
- Replacement: deceased individuals replaced from stock to maintain group size.

## Data content and structure
- Outputs: detections of aggregations (which cockroaches used which shelter at each minute).
- Detection filtering: only detections with confidence ≥ 0.95 retained; photos with no detectable individuals marked as NA.
- Time normalization: only the first 200 photographs per camera used to equalize across cameras.
- Aggregations: results from four cameras per box combined for each three-hour twenty-minute period.

## Data files and naming
- Total: 192 CSV files (4 replicates × 3 weeks × 4 days × 4 groups).
- File size/lines: 1378 to 3719 lines per file, depending on detections.
- File naming: S1_R1_WK1_1_001.csv (S shelf, R replicate, WK week (1=50% humidity, 2=40%, 3=30%), day, 001).
- CSV columns (V1, V2, V3):
  - V1: aggregation/photograph name (A1_R1_WK1_1_001.JPG) indicating camera, replicate, week, day, aggregation number.
  - V2: cockroach tag detected (one per line; 24 possible tags).
  - V3: detection confidence (0.95–1); NA if no detection.
- Each line represents a single detection; photos with multiple individuals yield multiple lines.

## Data completeness and scope
- Four replicates, three weeks, four days per week, four groups per day; 24 individuals per group.
- Some photos/cameras failed, leading to varying totals; first 200 photos per camera used to standardize.

## Processing, QA, and limitations
- Data cleaned via confidence threshold; some camera failures and incomplete captures acknowledged.
- Detections do not include undetected individuals; cross-week linking relies on the recorded tags (V2).
- Metadata and provenance provided for reproducibility.

## Metadata and provenance
- Collected and interpreted by: Callum McLean (Research Associate) and David Fisher (Principal Investigator).
- Data intended to support analyses of social network traits under environmental humidity changes.