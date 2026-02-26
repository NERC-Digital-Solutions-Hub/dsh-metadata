# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Contains detection matrices for 28 medium-large mammal species recorded at the SAFE project site during May–September 2015.
- Two CSV data files: MammalDetectionData_2015.csv (presence/absence detections) and MammalDetectionSurveyEffort_2015.csv (sampling site metadata and effort).
- Study location: SAFE landscape-scale forest modification experiment in Kalabakan Forest Reserve, Sabah, Malaysian Borneo.

## Experimental design and sampling regime
- Landscape includes highly disturbed lowland/hill dipterocarp forest, near-pristine Brantian-Tantulit Virgin Jungle Reserve, twice-logged Ulu Segama, and plantations (primarily oil palm).
- Four broad habitat classes: continuous logged forest, heavily degraded forest, isolated forest remnants, and oil palm.
- 130 camera locations deployed; data retrieved from 120 locations due to theft, vandalism, or malfunction.
- Two rotations of sampling, each with 65 locations.
- 42 consecutive camera-nights per location, total effort 4,669 camera-nights.
- Cameras placed at ~30 cm height on travel routes and off-trail areas to capture habitat-use differences; sensitivity set high with 10 images per trigger.

## Data collection and processing
- GPS coordinates recorded for each site; exact deployment/collection times and dates logged.
- Images screened to exclude blurred or non-target species; 28 target mammal species remained.
- 42-day sampling periods divided into six 7-day temporal replicates.
- Sites active for fewer than seven days excluded; resulting in 115 analytical units with 2–6 replicates.
- Data collection and interpretation led by a team including N.J. Deere and colleagues.

## Data structure and fields

- MammalDetectionData_2015.csv
  - Site: unique site identifier; prefixes indicate type or habitat class (e.g., OM for occupancy modelling; CLF, EA, OPF, OP for habitat classes).
  - Rep1–Rep6: 7-day sampling intervals; 1 = species present, 0 = absent, NA = not functioning.
  - Total Detection: sum of detections across all temporal replicates for each species.
  - Species: taxonomic information for the 28 recorded mammal species.

- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique sampling site identifier.
  - Latitude, Longitude: geographic coordinates (WGS 1984).
  - Date_On, Time_On: deployment date and time.
  - Date_Off, Time_Off: collection or failure date and time.
  - Number_of_Photos: images captured during the sampling period.
  - CTNs: number of operational camera trap nights (sampling effort).
  - CTHs: number of operational camera trap hours (sampling effort).