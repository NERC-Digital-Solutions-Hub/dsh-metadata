# UAV RGB images were collected from sites within core protected areas of the UNESCO Rhӧn Biosphere Reserve dominated by European beech ( Fagus sylvatica ) forest.

## Overview
- Dataset of UAV-derived imagery and terrain data from core protected areas of the UNESCO Rhön Biosphere Reserve, dominated by European beech.
- Data collected in September 2020 using a DJI Phantom 4 RTK UAV system.
- Eight GeoTiff files in total, comprising orthorectified RGB mosaics and corresponding Digital Elevation Models (DEMs) for multiple sites.

## Data collection details
- Sites and times:
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with slight intensity changes (wind not recorded).
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind.
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds.
  - Site 2: 10 Sept 2020, 11:05–12:35, changeable sky (cloudy/sunny), wind not recorded.
- Equipment: DJI Phantom 4 RTK UAV.
- Environment: Core protected areas of the Rhön Biosphere Reserve with beech-dominated forest.

## Data structure, nature, and units
- File set: Eight GeoTiff files named per site and data type:
  - 20200909_Site1a_RGB_DEM.tif
  - 20200909_Site1a_RGB_Ortho.tif
  - 20200909_Site1b_RGB_DEM.tif
  - 20200909_Site1b_RGB_Ortho.tif
  - 20200909_Site1c_RGB_DEM.tif
  - 20200909_Site1c_RGB_Ortho.tif
  - 20200910_Site2_RGB_DEM.tif
  - 20200910_Site2_RGB_Ortho.tif
- Data types:
  - Ortho mosaics: RGB, 8-bit unsigned integers, 0–255 range, ~3 cm pixel size.
  - DEMs: Digital Elevation Models, in meters above sea level, ~10 cm pixel size.
- Coordinate Reference System: WGS 84 / UTM zone 32N (meters).

## Data access and provenance
- Orthorectified mosaics and DEMs prepared by the NERC Field Spectroscopy Facility (FSF).
- Underlying data requests should be directed to fsf@nerc.ac.uk.

## Quality control
- QA performed by NERC FSF prior to creation of mosaicked images.

## Potential uses for analysts
- Enables high-resolution habitat and vegetation structure analysis in beech-dominated forests.
- Supports correlations between UAV-derived terrain/reflectance data and ecological variables.
- Facilitates development and validation of predictive models at fine spatial scales (3 cm–10 cm) within protected forest sites.
- Can be integrated with other datasets (e.g., ground truth, habitat surveys) for multidisciplinary environmental assessments.

## Considerations and limitations
- Temporal coverage limited to September 2020; single-season snapshot.
- Missing wind data for some sites and limited weather context beyond basic sky conditions.
- Data volume and processing demands due to very high-resolution imagery (3 cm) and multiple large DEM/orthomosaic files.
- Access to underlying data requires contact with FSF; may require formal data requests.