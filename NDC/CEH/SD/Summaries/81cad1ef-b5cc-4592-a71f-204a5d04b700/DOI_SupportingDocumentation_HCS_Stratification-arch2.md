# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Spatial data detailing the stratification of the SAFE study site based on satellite-derived spectral signatures following the High Carbon Stock (HCS) methodology.
- Study area: SAFE project site and surrounding Benta Wawasan oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo.
- Objective: support assessment of forest disturbance gradients and inform reduced impact land-use practices.

## Experimental design, sampling regime and data collection
- Data sources: Landsat 8 (15 m) and SPOT5 (2.5 m) imagery (temporal range 2012–2014) to mitigate cloud/haze issues.
- Approach: supervised classification of satellite imagery complemented by visual interpretation to correct topographic shadow effects.
- Scope: stratify habitat into four discrete HCS classes, ordered by carbon value.

## HCS classification and calibration
- Four HCS classes (descending carbon value):
  - Dense Forest (1)
  - Young Regenerating Forest (2)
  - Scrub (3)
  - Open Land (4)
- Calibration: class boundaries tied to above-ground carbon values derived from forest inventory data (N = 139) collected as part of the core SAFE monitoring programme.
- Purpose: establish a robust linkage between spectral signatures and carbon stock for monitoring habitat change and informing management actions.

## Data outputs and schema
- Output format: HCS_Stratification.shp shapefile containing polygon features with:
  - FID: unique polygon identifier
  - Shape: object type indicator
  - HCS_Class: numeric class code (1 Dense Forest; 2 Young Regenerating Forest; 3 Scrub; 4 Open Land)
  - Area_ha: polygon area in hectares
  - Perim_km: polygon perimeter in kilometres

## Purpose and applications
- Primary aim: assess responses of medium-large tropical forest mammals to disturbance gradients.
- Application: inform implementation of reduced impact land-use practices in human-modified landscapes.
- Data stewardship: dataset collated and HCS protocol implemented by the listed authors; designed to support standardised monitoring and subsequent analyses.

## Key contributors
- Data collation and HCS protocol implementation: N.J. Deere (lead), with assistance from M. Pfeifer.
- Interpretation and analysis: G. Guillera-Arroita, E.L. Baking, H. Bernard, M. Pfeifer, G. Reynolds, O.R. Wearn, Z.G. Davies, M.J. Struebig.