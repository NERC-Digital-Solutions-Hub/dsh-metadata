# Ciste Mhearad snow patch perimeter mapping using GNSS in Cairngorms (19–28 June/July 2023)

## Purpose and scope
- Map the perimeter of the late-lying Ciste Mhearad snow patch with centimeter-precision GNSS data.
- Data collected on three dates (19 June 2023; 27 July 2023; 28 July 2023) to capture perimeter shape over time.

## Data collection methods
- Two GNSS receivers used as base and roving units.
- Roving receiver positioned on a 2 m vertical pole; data recorded for 20 s at each point.
- Perimeter surveyed with approximately 1 m point spacing on straight sections.

## Coordinates and units
- Horizontal locations provided in:
  - UTM zone 30N easting/northing (meters)
  - WGS84 latitude/longitude (degrees)
- Orthometric height (above mean sea level) in meters.

## Quality control and processing
- Post-processing performed with Leica Infinity software.
- Accuracy indicated by standard deviations; occasional spikes due to base station power failures.
- Differential accuracy improved by tying problematic points to the BIGF Braemar GNSS station (19 km away).

## Data structure and file naming
- Three separate CSV files, one per date:
  - o_ciste_mhearad_snow_patch_19062023.csv
  - o_ciste_mhearad_snow_patch_27072023.csv
  - o_ciste_mhearad_snow_patch_28072023.csv
- Shared column schema:
  - Date_Time (dd/MM/yyyy hh:mm)
  - Easting (m)
  - Northing (m)
  - WGS84_Latitude (degrees)
  - WGS84_Longitude (degrees)
  - Ortho_Height (m)
  - SD_Easting (m)
  - SD_Northing (m)
  - SD_Ortho_Height (m)

## Experimental design
- Roving GNSS data collected at perimeter points with 1 m spacing to capture straight segments of the patch.
- Pole height subtracted during processing to obtain true ground positions.

## Fieldwork and instrumentation
- Instruments: Two Leica VIVA GS10 GNSS receivers (loaned via NERC Geophysical Equipment Facility).
- Receivers calibrated by manufacturer and tested with fixed antenna setup.
- Conducted with care to avoid disturbing protected birds (RSPB advised).

## Acknowledgments
- Supported by NERC Geophysical Equipment Facility loan.
- Special thanks to RSPB for guidance on minimizing disturbance.