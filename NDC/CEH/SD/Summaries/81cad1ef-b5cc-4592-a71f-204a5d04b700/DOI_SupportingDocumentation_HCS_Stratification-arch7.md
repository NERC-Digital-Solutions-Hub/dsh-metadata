# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview of data
- The HCS_Stratification.shp contains spatial data detailing stratification of the study site based on the spectral signature of satellite images in accordance with the High Carbon Stock (HCS) methodology.

## Experimental design, sampling regime and data collection
- Study area: Stability of Altered Forest Ecosystems (SAFE) project site and surrounding Benta Wawasan managed oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo (4 ⁰ 46'N, 116 ⁰ 57' E).
- Landscape context: Highly disturbed lowland and hill dipterocarp forest within the project area; near-pristine Brantian-Tantulit Virgin Jungle Reserve; twice-logged forest in Ulu Segama Forest Reserve; plantations (primarily oil palm, also acacia).
- Methods and data sources:
  - Satellite imagery: Landsat 8 (15 m) and SPOT5 (2.5 m) with temporal range 2012–2014.
  - Approach: Supervised classification of images, supplemented by visual interpretation to correct topographic shadow; multiple data sources used to mitigate cloud/haze.
  - HCS classes (descending carbon value): Dense Forest, Young Regenerating Forest, Scrub, Open Land.
  - Calibration: Above-ground carbon values derived from forest inventory data (core SAFE monitoring program; N = 139).
- Purpose: Assess the response of medium-large tropical forest mammals to the disturbance gradient to inform reduced impact land-use practices in human-modified landscapes.
- Roles: N.J. Deere (data collation and HCS protocol implementation); G. Guillera-Arroita, E.L. Baking, H. Bernard, M. Pfeifer, G. Reynolds, O.R. Wearn, M.J. Struebig, Z.G. Davies (interpretation).

## Attribute table (HCS_Stratification.shp)
- FID: unique identifier for each polygon
- Shape: discriminates between shapefile objects
- HCS_Class: numerical code for HCS strata (1 = Dense Forest; 2 = Young Regenerating Forest; 3 = Scrub; 4 = Open Land)
- Area_ha: area of each polygon in hectares
- Perim_km: perimeter of each polygon in kilometres