# Section 1 - Methods

- Study context: UAV RGB imagery collected in core protected areas of the UNESCO Rhön Biosphere Reserve dominated by European beech (Fagus sylvatica); data collection occurred in September 2020 using a DJI Phantom 4 RTK.
- Collection dates and conditions: 
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with varying intensity; no wind data.
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind.
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds.
  - Site 2: 10 Sept 2020, 11:05–12:35, changeable sky (cloudy/sunny); no wind data.
- Data products and structure: Eight GeoTiff files named per site and data type, with each site having an orthorectified RGB mosaic (Ortho) and an associated Digital Elevation Model (DEM).
  - Filenames include 20200909_Site1a_RGB_DEM.tif, 20200909_Site1a_RGB_Ortho.tif, 20200909_Site1b_RGB_DEM.tif, 20200909_Site1b_RGB_Ortho.tif, 20200909_Site1c_RGB_DEM.tif, 20200909_Site1c_RGB_Ortho.tif, 20200910_Site2_RGB_DEM.tif, 20200910_Site2_RGB_Ortho.tif.
- Data origin and access: Orthorectified mosaics and DEMs provided by the NERC Field Spectroscopy Facility; requests for underlying data should be directed to fsf@nerc.ac.uk.
- Geospatial specifications: 
  - DEMs in meters above sea level with ~10 cm pixel size.
  - Ortho mosaics in 8-bit unsigned integers (0–255) with ~3 cm pixel size.
  - All datasets use WGS 84 / UTM zone 32N (meters) as the Coordinate Reference System.
- Quality control: QA performed by NERC FSF prior to mosaic creation.