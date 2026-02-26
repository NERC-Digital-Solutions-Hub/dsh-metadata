# Ciste Mhearad snow patch perimeter GNSS measurements

- Purpose and timing
  - Geospatially locate the perimeter of the late-lying Ciste Mhearad snow patch with centimetre-resolution GNSS measurements.
  - Fieldwork conducted on 19 June 2023, 27 July 2023, and 28 July 2023; data post-processed with Leica Infinity.

- Data collected and units
  - Horizontal locations provided in:
    - UTM zone 30N easting/northing (metres)
    - WGS84 latitude/longitude (decimal degrees)
  - Elevation provided as orthometric height above mean sea level (metres)
  - Quality indicators: standard deviations (SD_Easting, SD_Northing, SD_Ortho_Height)
  - Some points show higher SD due to base station power failures; differential accuracy achieved by tying to BIGF station at Braemar (19 km away)

- Data structure and files
  - Three CSV files, one per survey date:
    - o_ciste_mhearad_snow_patch_19062023.csv
    - o_ciste_mhearad_snow_patch_27072023.csv
    - o_ciste_mhearad_snow_patch_28072023.csv
  - Common columns per file:
    - Date_Time (dd/MM/yyyy hh:mm)
    - Easting (UTM zone 30N) in metres
    - Northing (UTM zone 30N) in metres
    - WGS84_Latitude (degrees)
    - WGS84_Longitude (degrees)
    - Ortho_Height (metres)
    - SD_Easting (metres)
    - SD_Northing (metres)
    - SD_Ortho_Height (metres)

- Experimental design and field sampling
  - Roving GNSS receiver mounted on a 2 m vertical pole at perimeter points with 1 m spacing along straight perimeter sections.
  - Each point recorded for 20 seconds; pole height subtracted during processing.

- Field equipment and processing
  - Instrumentation: two Leica VIVA GS10 GNSS receivers (NERC GEF loan).
  - Receivers factory-calibrated and tested with a fixed antenna.
  - Data processing: post-processing with Leica Infinity; data tied to BIGF station when base power failed to improve accuracy.

- Location context and visualization
  - Perimeter mapped on 19 June 2023 (light blue) and 27 July 2023 (dark blue); contours informed by OS Terrain 5 DTM (Figure references).

- Acknowledgments and considerations
  - Supported by NERC Geophysical Equipment Facility loan 1164.
  - RSPB advised on avoiding disturbance to protected birds.
  - Practical notes for GIS use: consider potential data gaps due to base station power issues and the subjective spacing along perimeter when integrating across dates.