# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017)

## Overview
- Dataset description of mammal detections at the SAFE project site in Sabah, Malaysian Borneo, collected in 2015.
- Two CSV files:
  - MammalDetectionData_2015.csv: detection matrices for 28 medium-large mammal species.
  - MammalDetectionSurveyEffort_2015.csv: metadata for the 120 sampling sites.
- Authors include N.J. Deere, G. Guillera-Arroita, E.L. Baking, H. Bernard, M. Pfeifer, G. Reynolds, O.R. Wearn, Z.G. Davies, and M.J. Struebig.

## Experimental design, sampling regime, and data collection
- Location and context:
  - SAFE landscape-scale forest modification experiment in Kalabakan Forest Reserve, Sabah, with varied habitat classes (continuous logged forest, highly disturbed forest, isolated forest remnants, oil palm plantations).
- Sampling framework:
  - Camera-trap survey deployed across 130 locations; data retrieved from 120 sites due to theft, vandalism, and malfunction.
  - Sampling conducted over two rotations, each with 65 locations.
  - Standardized camera settings: Reconyx HC500, 30 cm height, high sensitivity, 10 images per trigger.
  - Each site surveyed for 42 consecutive nights.
  - Spatial arrangement: mean 1.4 km between sites; elevation 64–735 m (mean 376 m).
- Data capture period:
  - May–September 2015.
- Data collection responsibilities:
  - N.J. Deere and E.L. Baking collected the data; interpretation by a larger team including Deere, Guillera-Arroita, Baking, Bernard, Pfeifer, Reynolds, Wearn, Struebig, and Davies.

## Data structure and metadata

### MammalDetectionData_2015.csv
- Site: unique site identifier; habitat class prefixes (e.g., OM for occupancy modelling; CLF, EA, OPF, OP for habitat classes) with numerical suffixes for site differentiation within a class.
- Rep1–Rep6: values for 7-day sampling intervals (temporal replicates). 1 indicates presence, 0 indicates absence; NA for camera malfunctions.
- Total Detection: sum of detections across temporal replicates for each species.
- Species: taxonomic information; total of 28 mammal species recorded.

### MammalDetectionSurveyEffort_2015.csv
- Site_ID: unique sampling site identifier.
- Latitude / Longitude: coordinates (GCS WGS84).
- Date_On / Time_On: deployment date and time.
- Date_Off / Time_Off: collection date and time (or failure date/time).
- Number_of_Photos: total images captured during the sampling period.
- CTNs: number of operational camera-trap nights (sampling effort measure).
- CTHs: number of operational camera-trap hours (sampling effort measure).

## Data processing and quality assurance
- Image screening:
  - Excluded images that could not be identified to species (e.g., blurred images or non-target species).
- Data reduction:
  - 42-day sampling periods converted into six 7-day temporal replicates.
  - Sites with fewer than seven active days excluded, resulting in 115 analytical units with 2–6 replicates.
- Team responsibilities:
  - Data collection by N.J. Deere and E.L. Baking; interpretation by the listed authors.

## Data management and stewardship considerations

- Data governance and standards:
  - Consistent use of CSV format for both data and effort metadata.
  - Clear, standardized column definitions and coding (presence/absence, 7-day replicates, site prefixes, and habitat classes).
- Metadata completeness:
  - Location data (latitude/longitude), timestamps for deployment and retrieval, and explicit effort metrics (CTNs, CTHs) are provided.
- Data quality notes:
  - Potential gaps due to field losses (theft/vandalism/malfunction) resulting in fewer than the intended 130 locations being available (120 with usable data; 115 analytical units after filtering).
  - Reliance on species-level identifications; non-target or non-identifiable images excluded.
- Reuse and discovery:
  - Documentation includes detailed data structure guidance, enabling reuse for occupancy modelling and related analyses.
  - Preserves site-level identifiers and habitat class coding to support comparative analyses across habitat types and management regimes.

## Practical implications for use
- Suitable for occupancy modelling, diversity analyses, and assessments of mammal presence across disturbance gradients and oil palm plantations.
- Metadata supports reproducibility: exact dates/times, GPS coordinates, and explicit sampling effort metrics facilitate replication and upscaling to similar study contexts.
- Data steward actions recommended:
  - Maintain site identifiers and habitat prefixes to ensure consistency across datasets.
  - Preserve the temporal replicate structure and NA handling rules.
  - Monitor and document any future updates or corrections to species identifications or site-level metadata.