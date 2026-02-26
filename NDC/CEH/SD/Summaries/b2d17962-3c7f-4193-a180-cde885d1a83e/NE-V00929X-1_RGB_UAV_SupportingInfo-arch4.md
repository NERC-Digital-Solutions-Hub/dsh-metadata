# UAV RGB images were collected from sites within core protected areas of the UNESCO Rhӧn Biosphere Reserve dominated by European beech ( Fagus sylvatica ) forest

## Section 1 - Methods
- UAV data were collected in September 2020 using a DJI Phantom 4 RTK.
- Study sites: 1a, 1b, 1c, and 2 within core protected areas of the UNESCO Rhön Biosphere Reserve, dominated by European beech.
- Collection details:
  - Site 1a: 09 Sept 2020, 17:35–18:12, cloudy with changing intensity (wind not reported).
  - Site 1b: 09 Sept 2020, 10:15–11:05, clear sky, light wind.
  - Site 1c: 09 Sept 2020, 12:46–13:30, clear sky, strong winds.
  - Site 2: 10 Sept 2020, 11:05–12:35, variable sky (cloudy/sunny) (wind not reported).

## Section 2 - Data Structure, Nature and Units of recorded values
- Eight GeoTiff files:
  - 20200909_Site1a_RGB_DEM.tif
  - 20200909_Site1a_RGB_Ortho.tif
  - 20200909_Site1b_RGB_DEM.tif
  - 20200909_Site1b_RGB_Ortho.tif
  - 20200909_Site1c_RGB_DEM.tif
  - 20200909_Site1c_RGB_Ortho.tif
  - 20200910_Site2_RGB_DEM.tif
  - 20200910_Site2_RGB_Ortho.tif
- Each site includes:
  - An orthorectified RGB mosaic (Ortho) and a corresponding Digital Elevation Model (DEM).
  - Ortho mosaics: 8-bit unsigned integers, range 0–255, ~3 cm pixel size.
  - DEMs: in meters above sea level, ~10 cm pixel size.
- Coordinate Reference System: WGS 84 / UTM zone 32N (meters).
- Data origin: mosaic images provided by the NERC Field Spectroscopy Facility (FSF); requests for underlying data via fsf@nerc.ac.uk.
- Quality control: QA performed by NERC FSF prior to mosaic creation.

## Data Access and Governance
- Underlying data requests should be directed to fsf@nerc.ac.uk.
- Data formats are GeoTiff; accompanying metadata implied by capture details (date/time, sky conditions) and CRS.

## Quality Control
- QA conducted by NERC Field Spectroscopy Facility before mosaic creation.

## Relevance for Data Leaders
- Clear data provenance and standardized formats support data governance and reuse.
- Well-defined data structure (separate DEM and Ortho for each site) aids discoverability and integration into analyses.
- Explicit coordinate system and pixel resolutions facilitate interoperability and metadata clarity.
- Contact point for access (fsf@nerc.ac.uk) enables controlled data sharing and governance.
- Documentation of collection conditions (dates, times, sky conditions) enhances context and potential reproducibility.