# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Spatial data in HCS_Stratification.shp detailing stratification of the study site based on spectral signatures using the High Carbon Stock (HCS) methodology.

## Experimental design, sampling regime and data collection
- Study area: Stability of Altered Forest Ecosystems (SAFE) site and surrounding Benta Wawasan oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo.
- Landscape context: Highly disturbed lowland and hill dipterocarp forest, near-pristine and twice-logged forest, and plantations (oil palm and some acacia).
- Data sources and timeframe: Landsat 8 (15 m) and SPOT5 (2.5 m) imagery from 2012–2014; multiple sources used to mitigate cloud cover and haze.
- Methodology: Supervised classification of satellite images with visual interpretation to correct topographic shadow effects.
- HCS classes (in descending carbon value): Dense Forest, Young Regenerating Forest, Scrub, Open Land.
- Calibration: Above-ground carbon values from core SAFE monitoring data (N = 139) used to calibrate classes.
- Purpose of data collection: Assess mammal responses to disturbance gradient to inform reduced impact land-use practices.

## Data processing and authorship
- Data collators and protocol implementers: N.J. Deere led remote-sensing data collation and HCS protocol implementation; assistance from M. Pfeifer; interpretation contributed by Deere, Guillera-Arroita, Baking, Bernard, Pfeifer, Reynolds, Wearn, Struebig, and Davies.

## Data contents and structure
- Dataset: HCS_Stratification.shp (polygon shapefile) with attribute table including:
  - FID: unique polygon identifier
  - Shape: object type
  - HCS_Class: class code (1 = Dense Forest; 2 = Young Regenerating Forest; 3 = Scrub; 4 = Open Land)
  - Area_ha: area in hectares
  - Perim_km: perimeter in kilometres

## Purpose, context and potential uses
- Primary aim: Support understanding of habitat strata for conservation planning and land-use decisions within a disturbed tropical forest landscape.
- Stakeholders: Researchers studying forest mammals; land-use planners seeking reduced-impact practices.
- Data stewardship relevance: Clear provenance, documented methods, and structured attribute schema facilitate reuse and integration with other datasets.

## Governance, provenance and metadata considerations for Data Stewards
- Provenance: Explicitly documents data sources (Landsat 8, SPOT5), time window (2012–2014), and processing steps (supervised classification plus visual corrections).
- Metadata parity: Includes class definitions, class codes, and shapefile attributes essential for reproducibility.
- Data quality notes: Cloud cover and haze mitigated by using multiple sources; visual corrections address topographic shadow.
- Documentation and attribution: Authorship and contributions listed; dataset aligned with core SAFE monitoring program for calibration.