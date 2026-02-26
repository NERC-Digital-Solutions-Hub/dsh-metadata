# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Detection matrices detailing presence/absence for 28 medium-large mammal species recorded at the SAFE project ( Sabah, Malaysia) between May and September 2015.
- Includes MammalDetectionData_2015.csv (species detections) and MammalDetectionSurveyEffort_2015.csv (sampling site metadata).
- Data support occupancy modelling and biodiversity assessments across a landscape with varied habitat types.

## Experimental design, sampling regime and data collection
- Study area: SAFE site and surrounding estates in Kalabakan Forest Reserve, Sabah; habitat types include continuous logged forest, heavily degraded forest, isolated remnants, and oil palm plantations.
- Camera trapping: 130 locations deployed; 120 active after losses; two rotations of 65 locations; 42 consecutive nights per location.
- Equipment and settings: Reconyx HC500 Hyperfire cameras; height ~30 cm; high sensitivity; 10 images per trigger.
- Sampling layout: locations arranged to capture inter- and intra-habitat differences; mean distance between sites ~1.4 km; elevation range 64–735 m a.s.l. (mean 376 m).
- Data captured: GPS coordinates, deployment/collection dates and times, number of photos, and measures of sampling effort (operational nights/hours).

## Data processing and quality control
- Pre-analysis cleaning: exclude images that cannot be confidently identified to species (blurred/non-target images).
- Data structuring: create 42-day sampling periods divided into six 7-day temporal replicates.
- Inclusion criteria: exclude camera-trap sites active fewer than seven days; final analytical units = 115 sites with 2–6 replicates.
- Roles: N.J. Deere and E.L. Baking led data collection; multiple authors contributed to interpretation.

## Data structure and fields
- MammalDetectionData_2015.csv
  - Site: unique site identifier; prefix OM indicates occupancy modelling; habitat classes encoded (CLF, EA, OPF, OP) with numeric suffixes for site differentiation.
  - Rep1–Rep6: 7-day sampling interval replicates; values 1 = presence, 0 = absence, NA = malfunction.
  - Total Detection: sum of detections across replicates per species.
  - Species: taxonomic information; total of 28 recorded species.
- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique site identifier.
  - Latitude / Longitude: geographic coordinates (GCS WGS84).
  - Date_On / Time_On; Date_Off / Time_Off: deployment and collection timestamps.
  - Number_of_Photos: total images captured in the period.
  - CTNs: number of operational camera-trap nights.
  - CTHs: number of operational camera-trap hours.

## Data governance, accessibility and reuse
- Data provenance: collected by a collaborative team (list of authors) with explicit roles for data collection and interpretation.
- Metadata and discoverability: two CSV files containing structured data and rich metadata on site location, timing, effort, and species detections.
- Reproducibility: clear data processing steps (replicates, exclusion criteria, and analytical unit definitions) to support occupancy analyses and cross-site comparisons.
- Scope and limitations: data represent 2015 sampling within a mosaic of forest and plantation habitats; identifiable limitations include potential detection biases and the exclusion of non-identifiable images, as well as the absence of data beyond 2015.