# Ciste Mhearad snow patch perimeter GNSS measurements

- Collection and generation method
  - GNSS basestation (rover) measurements conducted around the perimeter of the late-lying Ciste Mhearad snow patch on Cairngorm on three dates: 19 June 2023, 27 July 2023, and 28 July 2023.
  - Post-processed using Leica Infinity software.

- Nature and units of recorded values
  - Horizontal locations recorded as:
    - UTM zone 30N easting/northing (meters)
    - WGS84 latitude/longitude (decimal degrees)
  - Orthometric height recorded as height above mean sea level (meters)

- Quality control
  - Standard deviations provided for each point indicate positional accuracy.
  - Occasional sudden increases in SD to 0.01 m (horizontal) and 0.04 m (vertical) signaling base station power failures.
  - Differential accuracy achieved by tying positions to the BIGF (British Isles continuous GNSS Facility) Braemar station, 19 km away.

- Details of data structure
  - Separate CSV file for each date:
    - o_ciste_mhearad_snow_patch_19062023.csv
    - o_ciste_mhearad_snow_patch_27072023.csv
    - o_ciste_mhearad_snow_patch_28072023.csv
  - Columns:
    - Date_Time (dd/MM/yyyy HH:mm)
    - Easting (m) and Northing (m) in UTM zone 30N
    - WGS84_Latitude (degrees)
    - WGS84_Longitude (degrees)
    - Ortho_Height (m)
    - SD_Easting (m)
    - SD_Northing (m)
    - SD_Ortho_Height (m)

- Experimental design / Sampling regime
  - Roving receiver mounted on a 2 m vertical pole positioned at perimeter points with 1 m spacing along straight perimeter sections.
  - Data collection at each point for 20 seconds.
  - Pole height subtracted during processing to obtain true ground positions.

- Fieldwork and laboratory instrumentation
  - Two Leica VIVA GS10 GNSS receivers (loaned from NERC Geophysical Equipment Facility, calibrated by manufacturer and tested at GEF).

- Acknowledgments and provenance
  - Supported by NERC Geophysical Equipment Facility loan (award 1164).
  - RSPB advised on avoiding disturbance to protected birds.

- Additional notes
  - Figure references indicate gnss roving and reference receivers set-up, and snow patch mapping as of 19 June 2023 and 27 July 2023, with contours derived from OS Terrain® 5 DTM.