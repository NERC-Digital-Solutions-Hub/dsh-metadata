# High Carbon Stock (HCS) Stratification of the SAFE project site, Sabah, Malaysian Borneo, 2015 [HMTF] (2017) Deere, N.J., Guillera-Arroita, G., Baking, E.L., Bernard, H., Pfeifer, M., Reynolds, G., Wearn, O.R., Davies, Z.G. and Struebig, M.J.

## Overview
- Spatial data in HCS_Stratification.shp detailing site stratification according to the High Carbon Stock (HCS) methodology based on satellite spectral signatures.

## Experimental design, sampling regime and data collection
- Location: SAFE project site and surrounding Benta Wawasan managed oil palm estates in Kalabakan Forest Reserve, Sabah, Malaysian Borneo.
- Context: Landscape-scale forest modification experiment including highly disturbed lowland and hill dipterocarp forest, near-pristine forest, twice-logged forest, and plantations (primarily oil palm; some acacia).
- Data sources and methods:
  - Satellite imagery: Landsat 8 (15 m) and SPOT5 (2.5 m) from 2012–2014.
  - Strategy: Use multi-source data to minimize cloud/haze effects; perform supervised classification supplemented by visual interpretation to correct topographic shadow.
  - Classification outcome: Four discrete HCS classes ranked by carbon value (highest to lowest): Dense Forest, Young Regenerating Forest, Scrub, Open Land.
  - Calibration: HCS classes calibrated to above-ground carbon values derived from forest inventory data (core SAFE monitoring programme; N = 139).
- Purpose: Assess responses of medium–large tropical forest mammals to disturbance gradients to inform reduced-impact land-use practices.
- Key roles: N.J. Deere led remote-sensing data collation and HCS protocol implementation; interpretation by Deere, Guillera-Arroita, Baking, Bernard, Pfeifer, Reynolds, Wearn, Struebig, and Davies.

## HCS_Stratification.shp attribute table
- FID: Unique identifier for each polygon.
- Shape: Geometry object identifier.
- HCS_Class: Numerical code for strata:
  - 1 = Dense Forest
  - 2 = Young Regenerating Forest
  - 3 = Scrub
  - 4 = Open Land
- Area_ha: Area of each polygon in hectares.
- Perim_km: Perimeter of each polygon in kilometres.