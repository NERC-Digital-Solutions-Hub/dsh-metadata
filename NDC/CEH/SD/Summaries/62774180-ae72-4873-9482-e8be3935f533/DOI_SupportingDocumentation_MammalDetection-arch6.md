# Mammal detection data for the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Contains detection matrices for 28 medium-large mammal species recorded May–September 2015.
- Two CSV files: MammalDetectionData_2015.csv (detection matrices) and MammalDetectionSurveyEffort_2015.csv (sampling metadata).
- Study area: SAFE project site and surrounding oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo; landscape-scale forest modification experiment.

## Experimental design and sampling regime
- Camera-trap deployment at 130 locations; data retrieved from 120 sampling locations due to theft, vandalism, and malfunction.
- Sampling stratified into four habitat classes: continuous logged forest, highly disturbed forest, isolated forest remnants, and oil palm plantations.
- Two rotations: 65 locations per rotation; single unit deployed for 42 consecutive nights per location (total of 4,669 camera nights).
- Camera setup: Reconyx HC500 Hyperfire, height 30 cm, high sensitivity, 10 images per trigger.
- Spatial context: elevation 64–735 m a.s.l. (mean 376 m); mean inter-site distance ~1.4 km.

## Data collection and processing
- GPS coordinates recorded for each site; exact deployment, collection, and malfunction times documented.
- Images not identifiable to species (blurred or non-target) excluded from analysis.
- Detection matrices: 42-day sampling period divided into six 7-day temporal replicates.
- Analytic units: 115 sites with 2–6 replicates; sites active fewer than seven days excluded.
- Data collection and interpretation led by N.J. Deere et al.; collaborators listed for interpretation.

## Data structure and fields

- MammalDetectionData_2015.csv
  - Site: unique site identifier; habitat prefixes indicating class (OM for occupancy modelling; CLF, EA, OPF, OP) with numeric suffix differentiating sites within a class.
  - Rep1–Rep6: 7-day sampling intervals (temporal replicates). Values: 1 = presence, 0 = absence, NA = malfunction.
  - Total Detection: sum of detections across replicates for each species.
  - Species: taxonomic information for the 28 recorded mammal species.

- MammalDetectionSurveyEffort_2015.csv
  - Site_ID: unique site identifier.
  - Latitude; Longitude: coordinates (GCS WGS84).
  - Date_On; Time_On: deployment date and time.
  - Date_Off; Time_Off: collection date and time (or failure).
  - Number_of_Photos: images captured during the sampling period.
  - CTNs: number of operational camera trap nights (sampling effort).
  - CTHs: number of operational camera trap hours (sampling effort).