# Ciste Mhearad snow patch perimeter mapping using GNSS (19-06-2023 to 28-07-2023)

- Objective
  - Locate and map the perimeter of the late-lying Ciste Mhearad snow patch on Cairngorm with centimeter-resolution GNSS methods.
  - Data collected on three dates: 19 June 2023, 27 July 2023, and 28 July 2023; post-processed with Leica Infinity software.

- Data collected and units
  - Horizontal positions provided in:
    - UTM zone 30N easting/northing (meters)
    - WGS84 latitude/longitude (degrees)
  - Elevation provided as orthometric height (meters above mean sea level).
  - Each date has a separate CSV file:
    - o_ciste_mhearad_snow_patch_19062023.csv
    - o_ciste_mhearad_snow_patch_27072023.csv
    - o_ciste_mhearad_snow_patch_28072023.csv
  - Columns include:
    - Date_Time (dd/MM/yyyy hh:mm)
    - Easting (m), Northing (m)
    - WGS84_Latitude (degrees), WGS84_Longitude (degrees)
    - Ortho_Height (m)
    - SD_Easting (m), SD_Northing (m), SD_Ortho_Height (m) for measurement uncertainty

- Quality control and accuracy
  - Post-processed point accuracy indicated by standard deviations.
  - Occasional sudden increases in SD (0.01 m horizontal, 0.04 m vertical) due to base-station power failures.
  - Differential accuracy achieved by tying affected points to the BIGF station at Braemar (19 km away).

- Experimental design and measurement protocol
  - Roving receiver mounted on a 2 m vertical pole positioned at 1 m spacing around the snow-patch perimeter.
  - Each point recorded for 20 seconds; horizontal spacings chosen to capture approximately straight perimeter sections.
  - Pole height subtracted during data processing.

- Fieldwork and instrumentation
  - Data collected with two Leica VIVA GS10 GNSS receivers.
  - Equipment loaned by the NERC Geophysical Equipment Facility; receivers calibrated and tested with a fixed antenna.

- Data structure and accessibility
  - Perimeter data organized into three date-specific CSV files.
  - Each file contains detailed coordinate information and associated measurement uncertainties.

- Acknowledgments
  - Supported by NERC Geophysical Equipment Facility loan (ref. 1164).
  - Advisory input from RSPB to avoid disturbance to protected birds.

- Visual context
  - Figures depict the RNSS mapping setup (roving and reference receivers) and snow-patch extents on 19 June and 27 July 2023, with contours from OS Terrain 5 DTM.