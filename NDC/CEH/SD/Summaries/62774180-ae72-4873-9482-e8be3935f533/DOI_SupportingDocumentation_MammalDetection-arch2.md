# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Contains presence/absence data for 28 medium-large mammal species recorded at the SAFE project site between May and September 2015.
- Two CSV datasets are included: MammalDetectionData_2015.csv (detection matrices) and MammalDetectionSurveyEffort_2015.csv (sampling metadata).
- Data cover 120 sampling locations across four habitat classes within a landscape-scale forest modification experiment in Sabah, Malaysian Borneo.

## Experimental design and sampling regime
- Study context: Stability of Altered Forest Ecosystems (SAFE) site and surrounding managed oil palm estates.
- Habitat classes: continuous logged forest, highly disturbed forest, isolated forest remnants, oil palm plantations.
- Sampling framework: 130 locations originally planned; data retrieved from 120 sites due to theft, vandalism, and malfunction.
- Camera-trap deployment: Remotely operated Reconyx HC500 cameras, positioned at ~30 cm height on low resistance routes and off-trail areas.
- Temporal design: two rotations of 65 locations each; each location surveyed for 42 consecutive nights (total survey effort 4,669 camera nights).
- Sampling details: high sensitivity, 10 images per trigger to aid species identification; 1.4 km mean spacing between sites; elevation range 64–735 m above sea level.

## Data collection and metadata
- Site and effort data recorded:
  - GPS coordinates for each site; deployment and retrieval dates/times; number of photos; operational camera trap nights and hours.
- Data handling: exact timing of deployment, collection, or failure documented to indicate sampling effort.

## Data processing
- Image screening: only images identifiable to species level were retained; blurred or non-target images excluded.
- Detection matrices: constructed from 42-day sampling into six 7-day temporal replicates per site.
- Site inclusion criteria: camera-trap sites active for fewer than seven days excluded; resulting in 115 analytical units with 2–6 replicates.

## Data structure and fields
- MammalDetectionData_2015.csv
  - Site: unique site identifier; prefixes denote habitat class (e.g., OM, CLF, EA, OPF, OP).
  - Rep1–Rep6: 7-day sampling interval indicators (1 = present, 0 = absent); NA for malfunctioning periods.
  - Total Detection: sum of detections across Replicates for each species.
  - Species: taxonomic information; total of 28 recorded mammal species.
- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique site identifier.
  - Latitude, Longitude: GPS coordinates (WGS 84).
  - Date_On, Time_On; Date_Off, Time_Off: deployment and retrieval timestamps.
  - Number_of_Photos: total images captured in the period.
  - CTNs: number of operational camera-trap nights.
  - CTHs: number of operational camera-trap hours.

## Data quality, limitations, and provenance
- Data quality ensured by screening images and standardising temporal replication.
- Limitations include incomplete deployment (130 planned vs. 120 collected) and potential data gaps from equipment issues.
- Authorship and responsibilities:
  - Data collection by N.J. Deere and E.L. Baking.
  - Data interpretation by Deere, Guillera-Arroita, Baking, Bernard, Pfeifer, Reynolds, Wearn, Struebig, Davies.