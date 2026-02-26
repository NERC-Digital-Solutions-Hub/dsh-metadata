# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment colloidal carbohydrate concentration in saltmarsh and mudflat habitats

## Overview
- Dataset measuring colloidal carbohydrate concentration in surface sediments, expressed as glucose equivalents in micrograms per gram (µg g-1).
- Focus on saltmarsh and mudflat habitats; winter and summer 2013 data with five replicates per quadrat.
- Part of the CBESS program; aims to enable cross-site comparison and data use across topics.

## Sampling design and locations
- Staff responsible: Jack Maunder.
- Locations ( Essex and Morecambe Bay ):
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Habitat contrasts and site characteristics:
  - Saltmarsh sites represent two soil types: clay soils (Essex) and sandy soils (Morecambe Bay).
  - Essex and Morecambe Bay saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation.
  - Mudflat sites: Essex with cohesive clays, mud, silt; Morecambe alongside coarser, mobile sediments.
- Sampling framework:
  - 22 randomly allocated 1 x 1 m quadrats per mudflat and saltmarsh site.
  - Four spatial scales (A–D): A=1 quadrat, B=3 quadrats 1–10 m apart, C=6 quadrats 10–100 m apart, D=12 quadrats 100–1000 m or site max.
  - Random allocation via R; no repeats planned.

## Methods and processing
- Observation/measurement target: Colloidal carbohydrate concentration (µg g-1) in surface sediment.
- Sample collection and handling:
  - Sediment cores collected as contact cores; liquid nitrogen used to freeze top 2 mm; excess unfrozen sediment removed; cores stored below -80°C.
  - Wet weight recorded; samples freeze-dried to remove water.
- Laboratory analysis:
  - Colloidal carbohydrate concentration determined by Dubois Phenol-Sulphuric assay.
  - Sub-sample (50–500 mg, site-dependent) from dried core; known volume of distilled water added; vortexed and centrifuged; supernatant used.
  - Color development with concentrated sulfuric acid and 5% phenol; ratio sample:phenol:acid 1:1:5 by volume; 35-minute development.
  - Absorbance read at 486.5 nm using Thermo Biomate 5 spectrophotometer.
  - Concentrations calculated from regression standards and expressed as glucose equivalents (µg g-1).
- QC and notes:
  - Zeroes indicate concentrations below detectable level.
  - Spectrophotometer and scale measurements validated via standards and laboratory protocols.
  - Spatial calibration and lab protocols followed for scale design.

## Data structure and formats
- File format: Comma-separated values (.csv).
- Key fields:
  - Row Number (sorting aid)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A=1m, B=1–10m, C=10–100m, D=100–upper limit)
  - Colloidal Carb (µg g-1) – average concentration
  - StDev – standard deviation
- Data quality notes:
  - NA indicates missing data due to inaccessibility of quadrat.

## Quality control and limitations
- Calibration steps:
  - Spectrophotometer accuracy checked with glucose standards.
  - Lab protocols followed for scale calibration and sampling.
- Data limitations:
  - No planned repeats; dataset provides a single campaign snapshot (winter and summer 2013).
  - Some quadrats may have missing data (NA).
- Outputs suitable for self-service data exploration and comparisons across sites, habitats, seasons, and spatial scales.