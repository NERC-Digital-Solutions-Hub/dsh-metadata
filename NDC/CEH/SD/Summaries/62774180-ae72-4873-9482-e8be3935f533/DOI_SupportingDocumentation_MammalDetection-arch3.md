# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Data describe detection matrices for 28 medium–large mammal species recorded at the SAFE project site in Sabah, Malaysian Borneo, during May–September 2015.
- Two camera-trap rotations across 120 sampling locations (temporarily reduced from 130 due to theft/vandalism/malfunction), yielding 4,669 camera nights.
- Habitat-wide sampling to capture landscape heterogeneity: continuous logged forest, heavily degraded forest, isolated forest remnants, and oil palm plantations.
- The dataset supports occupancy modelling and presence/absence analyses across habitat classes and sampling periods.

## Experimental design, sampling regime, and data collection
- Study area: SAFE landscape-scale forest modification experiment within Kalabakan Forest Reserve and surrounding oil palm estates.
- Sampling framework: Stratified within four broad habitat classes to reflect landscape heterogeneity; locations separated by a mean of 1.4 km; elevation 64–735 m asl (mean 376 m).
- Camera-traps: Reconyx HC500 Hyperfire deployed at 130 locations; data retrieved from 120 locations over two rotations (65 locations per rotation).
- Deployment: Each site sampled for 42 consecutive nights; standard setup included camera height at 30 cm, high sensitivity, 10 images per trigger.
- Data collection period: May–September 2015.
- Processing notes: Exact deployment/collection dates and times recorded; sites with malfunctions tracked.

## Data processing and structure
- Image processing: Non-target or blurred images excluded; remaining images used to create species detection matrices.
- Temporal structuring: 42-day sampling periods divided into six 7-day temporal replicates.
- Analytical units: Excluding sites active fewer than seven days left 115 analytical units with 2–6 replicates.
- Responsibility: N.J. Deere and E.L. Baking collected data; multiple authors contributed to interpretation.

## Data files and structure
- MammalDetectionData_2015.csv
  - Site: unique site identifier; prefixes indicate habitat class for occupancy modelling (OM; CLF; EA; OPF; OP with numerical suffix to differentiate sites within a class).
  - Rep1–Rep6: 7-day sampling intervals (temporal replicates); 1 = present, 0 = absent; NA for malfunctioning/unsampled periods.
  - Total Detection: sum of detections across temporal replicates for each species.
  - Species: taxonomic information for the 28 recorded mammal species.
- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique site identifier.
  - Latitude/Longitude: geographic coordinates (GCS WGS 1984).
  - Date_On/Time_On: deployment date and time.
  - Date_Off/Time_Off: collection date and time (or failure).
  - Number_of_Photos: total photos captured during the sampling period.
  - CTNs: number of operational camera trap nights (sampling effort).
  - CTHs: number of operational camera trap hours (sampling effort).

## Metadata and coding details
- Habitat-class prefixes:
  - OM: occupancy modelling context
  - CLF: continuous logged forest
  - EA: experimental area – heavily degraded forest
  - OPF: established oil palm forest fragments
  - OP: oil palm
- Temporal replicates: Rep1–Rep6 correspond to six 7-day blocks within each 42-day sampling period.
- Data quality and governance considerations: dataset includes precise timestamps and GPS coordinates; processing steps ensure consistency for occupancy analyses; explicit documentation of sampling effort facilitates reproducibility and methodological transparency.

## Relevance for monitoring frameworks
- Provides a robust, habitat-stratified, repeat-sampling dataset suitable for occupancy modelling and detection probability estimation.
- Rich metadata supports data governance practices: explicit site identifiers, geospatial data, sampling dates/times, and effort metrics (CTNs, CTHs).
- Demonstrates practical challenges and mitigations relevant to monitoring frameworks (e.g., equipment loss, malfunctions, temporal replication, and data cleaning).
- Data structure facilitates integration with monitoring dashboards and comparative analyses across habitat classes and time periods.