# UAV RGB Images from Core Protected Areas of the UNESCO Rhön Biosphere Reserve Dominated by European Beech (Fagus sylvatica)

## Overview
- Purpose: Provide orthorectified RGB mosaics and corresponding DEMs for environmental monitoring and analysis within protected areas of the UNESCO Rhön Biosphere Reserve.
- Coverage: Sites within core protected areas dominated by European beech (Fagus sylvatica): Site 1a, Site 1b, Site 1c, and Site 2.
- Collection period: September 2020.
- Platform: DJI Phantom 4 RTK UAV system.
- Data provenance: Mosaics and DEMs produced from UAV imagery; QA performed by NERC Field Spectroscopy Facility (FSF).

## Methods (Section 1)
- Data collection dates and times:
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with slight intensity changes; wind not recorded.
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind.
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds.
  - Site 2: 10 Sept 2020, 11:05–12:35, changeable sky (cloudy/sunny); wind not recorded.
- Sensor/Platform: UAV-based RGB data collected with DJI Phantom 4 RTK.
- Output types: Orthorectified RGB mosaic images and corresponding Digital Elevation Models (DEMs).

## Data Structure, Nature and Units (Section 2)
- Files and naming:
  - 20200909_Site1a_RGB_DEM.tif
  - 20200909_Site1a_RGB_Ortho.tif
  - 20200909_Site1b_RGB_DEM.tif
  - 20200909_Site1b_RGB_Ortho.tif
  - 20200909_Site1c_RGB_DEM.tif
  - 20200909_Site1c_RGB_Ortho.tif
  - 20200910_Site2_RGB_DEM.tif
  - 20200910_Site2_RGB_Ortho.tif
- Data characteristics:
  - Ortho mosaics: RGB images, 8-bit unsigned integers, value range 0–255, pixel size ~3 cm.
  - DEMs: Digital Elevation Models, units in meters above sea level, pixel size ~10 cm.
- Coordinate Reference System (CRS): WGS 84 / UTM zone 32N (in meters).
- Site-by-site content: Each site has one Ortho TIFF and one DEM TIFF.
- Data access for underlying data: Provided by NERC Field Spectroscopy Facility; contact fsf@nerc.ac.uk for details.

## Quality Control
- QA performed by NERC FSF prior to creation of the mosaicked images.

## Relevance for Environmental Monitoring
- Provides standardized, high-resolution geospatial imagery and elevation data suitable for consistent environmental health assessments over time.
- Enables integration with other datasets while maintaining data provenance and quality assurance.
- Supports transparency and accessibility of the underlying data for broader use by researchers and policymakers.