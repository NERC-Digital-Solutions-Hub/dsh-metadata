# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017)

## Overview
- Data product: HCS_Stratification.shp containing spatial stratification of the study site by spectral signatures following the High Carbon Stock (HCS) methodology.
- Purpose: assess responses of medium-large tropical forest mammals to disturbance gradients to inform reduced-impact land-use practices in human-modified landscapes.
- Study context: SAFE project site and surrounding Benta Wawasan managed oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo (location 4°46'N, 116°57'E).

## Experimental design, data collection, and processing
- Data sources and scope:
  - Satellite imagery: Landsat 8 (15 m) and SPOT5 (2.5 m) covering 2012–2014; multiple sources used to mitigate cloud cover and haze.
- Methodology:
  - Supervised classification of imagery complemented by visual interpretation to correct for topographic shadow effects.
  - Stratification produced four discrete HCS classes in descending carbon value: Dense Forest, Young Regenerating Forest, Scrub, Open Land.
- Calibration:
  - HCS classes calibrated using above-ground carbon values derived from forest inventory data collected as part of the core SAFE monitoring programme (N = 139).
- Team and responsibilities:
  - Data collation and HCS protocol implementation led by N.J. Deere, with assistance from M. Pfeifer; interpretation supported by a team including G. Guillera-Arroita, E.L. Baking, H. Bernard, G. Reynolds, O.R. Wearn, Z.G. Davies, and M.J. Struebig.

## Data product details
- File: HCS_Stratification.shp (polygon shapefile).
- Attribute table fields:
  - FID: unique identifier for each polygon.
  - Shape: object type indicator for each polygon.
  - HCS_Class: numeric code for strata: 1 = Dense Forest; 2 = Young Regenerating Forest; 3 = Scrub; 4 = Open Land.
  - Area_ha: area of each polygon in hectares.
  - Perim_km: perimeter of each polygon in kilometres.

## Purpose and implications for monitoring frameworks
- The stratified HCS mapping provides a structured basis to monitor habitat condition and carbon stock across disturbance gradients.
- Data supports evaluation of environmental health in landscape-scale management and informs policy or practice changes for reduced-impact land-use in mixed forest–agriculture landscapes.

## Data provenance and governance notes (implications for practice)
- Data produced through integration of remote sensing and field calibration, with explicit attention to mitigating cloud cover and topographic shadow.
- Underlines the importance of robust metadata, transparent data provenance, and calibration with ground-truth measurements to ensure data usefulness for ongoing monitoring and decision-making.