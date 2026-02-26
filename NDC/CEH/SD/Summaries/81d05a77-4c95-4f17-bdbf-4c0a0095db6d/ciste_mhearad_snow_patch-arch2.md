# Ciste Mhearad snow patch perimeter GNSS data collection (June–July 2023)

## Objective
- Collect centimetre-accurate perimeter coordinates of the late-lying Ciste Mhearad snow patch to map its extent and support environmental monitoring and policy performance over time.

## Methods and collection
- Two Leica VIVA GS10 GNSS receivers used as base and roving stations; data post-processed with Leica Infinity.
- Roving receiver positioned on a 2 m vertical pole; 1 m spacing along the snow patch perimeter; each point recorded for 20 seconds.
- Perimeter measurements taken on three dates: 19 June 2023, 27 July 2023, and 28 July 2023.
- Pole height subtracted during processing.

## Data recorded and units
- Horizontal positions recorded as:
  - UTM zone 30N easting/northing (meters)
  - WGS84 latitude/longitude (degrees)
- Height recorded as orthometric height above mean sea level (meters)

## Quality control and accuracy
- Point accuracy indicated by standard deviations:
  - SD_Easting, SD_Northing, SD_Ortho_Height (meters)
- Occasional sudden increases in horizontal SD (to 0.01 m) and vertical SD (to 0.04 m) due to base station power failures.
- Differential accuracy achieved by tying measurements to the BIGF station at Braemar (19 km away).

## Experimental design and field protocol
- Perimeter points recorded with 1 m spacing to approximate straight perimeter segments.
- Processing subtracts the 2 m pole height to obtain true ground positions.

## Data structure and files
- Three per-date CSV files:
  - o_ciste_mhearad_snow_patch_19062023.csv
  - o_ciste_mhearad_snow_patch_27072023.csv
  - o_ciste_mhearad_snow_patch_28072023.csv
- Columns:
  - Date_Time (dd/MM/yyyy hh:mm)
  - Easting (UTM 30N easting, m)
  - Northing (UTM 30N northing, m)
  - WGS84_Latitude (degrees)
  - WGS84_Longitude (degrees)
  - Ortho_Height (m)
  - SD_Easting (m)
  - SD_Northing (m)
  - SD_Ortho_Height (m)

## Instrumentation and processing details
- Field instruments: Two Leica VIVA GS10 GNSS receivers (loaned by NERC Geophysical Equipment Facility); receivers calibrated and tested.
- Data processing: Post-processed to ensure differential accuracy; reference to BIGF Braemar station for longer-baseline corrections when needed.
- Documentation support: Figures illustrating GNSS setup and snow patch extent accompany the dataset.

## Data handling and accessibility
- Datasets prepared for storage and uploading to appropriate data portals; organized by collection date for consistency and traceability.

## Acknowledgments
- Supported by NERC Geophysical Equipment Facility loan 1164.
- RSPB acknowledged for guidance on avoiding disturbance to protected birds.