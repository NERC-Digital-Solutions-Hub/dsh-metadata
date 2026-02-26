# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Contains mammal detection matrices for 28 medium-large mammal species recorded at the SAFE project site during May–September 2015.
- Metadata for 120 camera-trap sampling sites; final analytical units number 115 with 2–6 temporal replicates.
- Data collected using remotely operated cameras to assess occupancy and presence/absence across habitat types.

## Study area and sampling design
- Location: SAFE project site and surrounding managed oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo.
- Habitat classes (stratification): continuous logged forest, highly disturbed forest, isolated forest remnants, oil palm plantations.
- Spatial design: sampling points separated by approximately 1.4 km, elevational range 64–735 m above sea level (mean 376 m).
- Camera-trap deployment: 130 locations configured to two rotations (65 locations per rotation), 30 cm camera height, high sensitivity, 10 images per trigger.
- Sampling period: May–September 2015; total survey effort of 4,669 camera nights across 120 sites (reduced from 130 due to theft, vandalism, and malfunctions).

## Data collection and processing
- Equipment: Reconyx HC500 Hyperfire camera-traps; deployments aimed at capturing inter- and intra-specific habitat use differences.
- Data handling: images not identifiable to species or non-target removed prior analysis.
- Temporal structuring: 42-day sampling periods divided into six 7-day temporal replicates.
- Analytical units: sites with fewer than seven days of data excluded, resulting in 115 analytical units with 2–6 replicates each.
- Personnel: N.J. Deere and E.L. Baking led data collection; multiple authors contributed to interpretation.

## Data structure and contents
- MammalDetectionData_2015.csv
  - Site: unique sampling site identifier; prefixes indicate habitat class and occupancy modelling (e.g., OM, CLF, EA, OPF, OP).
  - Rep1–Rep6: 7-day sampling intervals (temporal replicates); values 1 = presence, 0 = absence, NA = camera malfunction.
  - Total Detection: sum of detections across replicates for each species.
  - Species: taxonomic information; total of 28 species recorded.
- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique sampling site identifier.
  - Latitude / Longitude: geographic coordinates (GCS WGS 1984).
  - Date_On / Time_On: deployment date and time (first image).
  - Date_Off / Time_Off: collection or failure date and time.
  - Number_of_Photos: images captured during the sampling period.
  - CTNs: number of operational camera trap nights (sampling effort).
  - CTHs: number of operational camera trap hours (sampling effort).

## GIS-ready notes
- Coordinates provided in WGS 1984; suitable for mapping site distribution across habitat classes.
- Data support occupancy modelling and presence/absence analyses across multiple habitats and land-use types.
- Data quality considerations: strict filtering to ensure species-level identifications; NA values indicate occasional camera malfunctions or incomplete replicates.