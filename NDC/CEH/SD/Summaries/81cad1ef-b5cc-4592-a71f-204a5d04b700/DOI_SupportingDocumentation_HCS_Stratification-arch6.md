# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview of the dataset
- Spatial data in HCS_Stratification.shp detailing stratification of the study site using the spectral signature of satellite imagery per the High Carbon Stock (HCS) methodology.
- Data intended to map habitat strata and carbon stock across the SAFE project landscape.

## Experimental context
- Location: SAFE project site and surrounding Benta Wawasan managed oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo (coordinates provided).
- Purpose: assess the response of medium-large tropical forest mammals to a disturbance gradient to inform reduced-impact land-use practices in human-modified landscapes.
- Study design includes highly disturbed lowland and hill dipterocarp forest, near-pristine forest, twice-logged forest, and plantations (oil palm and acacia).

## Methods and data collection
- Data sources and imagery: Landsat 8 (15 m) and SPOT5 (2.5 m) from 2012–2014; multiple sources used to mitigate cloud cover and haze.
- Classification approach: supervised classification of satellite images, supplemented by visual interpretation to correct for topographic shadow.
- Stratification outcome: four discrete HCS classes ranked by carbon value (from highest to lowest).

## HCS classes and calibration
- Dense Forest
- Young Regenerating Forest
- Scrub
- Open Land
- Calibration: classes tied to above-ground carbon values derived from forest inventory data collected as part of the core SAFE monitoring programme (N = 139).

## Data products and schema
- Primary file: HCS_Stratification.shp (shapefile)
- Attribute table fields:
  - FID: unique identifier for each polygon
  - Shape: object type indicator for shapefile objects
  - HCS_Class: numerical code for HCS strata (1 = Dense Forest; 2 = Young Regenerating Forest; 3 = Scrub; 4 = Open Land)
  - Area_ha: area of each polygon in hectares
  - Perim_km: perimeter of each polygon in kilometres

## Data provenance and contributions
- Lead data collation and HCS protocol implementation by N.J. Deere; assistance from M. Pfeifer.
- Interpretation contributed by N.J. Deere, G. Guillera-Arroita, E.L. Baking, H. Bernard, M. Pfeifer, G. Reynolds, O.R. Wearn, M.J. Struebig, and Z.G. Davies.