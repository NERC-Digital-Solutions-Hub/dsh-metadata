# UAV RGB images from sites within core protected areas of the UNESCO Rhӧn Biosphere Reserve dominated by European beech (Fagus sylvatica) forest; September 2020

## Quick overview
- UAV RGB imagery collected September 2020 using a DJI Phantom 4 RTK in core protected areas of the Rhön Biosphere Reserve (beech forest).
- Data captured to produce orthomosaic RGB images and corresponding Digital Elevation Models (DEMs).
- Association with NERC Field Spectroscopy Facility (FSF) for data provisioning and QA.

## Data collection details
- Sites and dates:
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with changing intensity
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds
  - Site 2: 10 Sept 2020, 11:05–12:35, changeable sky (cloudy/sunny)
- Equipment: DJI Phantom 4 RTK
- Weather notes: sky conditions and limited wind information available for some sites

## Data structure and contents
- Eight GeoTiff files (two per site: one Ortho RGB mosaic and one DEM):
  - 20200909_Site1a_RGB_DEM.tif
  - 20200909_Site1a_RGB_Ortho.tif
  - 20200909_Site1b_RGB_DEM.tif
  - 20200909_Site1b_RGB_Ortho.tif
  - 20200909_Site1c_RGB_DEM.tif
  - 20200909_Site1c_RGB_Ortho.tif
  - 20200910_Site2_RGB_DEM.tif
  - 20200910_Site2_RGB_Ortho.tif
- Data characteristics:
  - Ortho mosaics: 8-bit unsigned integers (0–255), approx. 3 cm pixel size
  - DEMs: in meters above sea level, approx. 10 cm pixel size
- Coordinate Reference System: WGS 84 / UTM zone 32N (meters)

## Data provenance and access
- Underlying data and further details available via the NERC Field Spectroscopy Facility: fsf@nerc.ac.uk
- Quality control: QA conducted by NERC FSF prior to mosaic generation

## Practical notes for data use and support
- Data suitable for high-resolution land-cover and elevation analyses in beech-dominated forest areas.
- Weather and wind conditions at collection may influence image quality and should be considered during analysis.
- If additional data or raw observations are needed, contact fsf@nerc.ac.uk for access requests.