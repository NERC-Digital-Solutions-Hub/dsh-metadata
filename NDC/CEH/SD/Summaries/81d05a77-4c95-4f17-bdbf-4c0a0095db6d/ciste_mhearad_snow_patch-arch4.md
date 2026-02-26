# Ciste Mhearad snow patch perimeter GNSS measurements

## Objective
- Document GNSS-based perimeters of the late-lying Ciste Mhearad snow patch on three dates: 19 June 2023, 27 July 2023, and 28 July 2023.
- Use post-processed GNSS data to determine horizontal positions and orthometric heights with quantified accuracy.

## Methods and data collection
- Two GNSS receivers (base and roving) used for high-accuracy positioning of perimeter points.
- Roving receiver positioned on a 2 m vertical pole along the snow patch perimeter with 1 m spacing; each point recorded for 20 seconds.
- Processing performed with Leica Infinity software.
- Base station power failures identified points with higher uncertainty; differential correction tied to the BIGF station at Braemar (19 km away) to improve accuracy.

## Data recording and units
- Horizontal locations recorded as:
  - UTM zone 30N easting and northing (meters)
  - WGS84 latitude and longitude (decimal degrees)
- Ortho_Height recorded as meters above mean sea level.
- Quality indicators provided as standard deviations for easting, northing, and orthometric height.

## Data structure and files
- One CSV file per date:
  - ciste_mhearad_snow_patch_19062023.csv
  - ciste_mhearad_snow_patch_27072023.csv
  - ciste_mhearad_snow_patch_28072023.csv
- Columns included in each file:
  - Date_Time (dd/MM/yyyy HH:mm)
  - Easting (m)
  - Northing (m)
  - WGS84_Latitude (degrees)
  - WGS84_Longitude (degrees)
  - Ortho_Height (m)
  - SD_Easting (m)
  - SD_Northing (m)
  - SD_Ortho_Height (m)

## Experimental design and sampling
- Perimeter mapping conducted by moving the roving antenna along the snow patch boundary.
- Spacing chosen to capture approximately straight perimeter sections; horizontal point spacing effectively 1 m along the perimeter.
- Pole height subtracted during processing to yield true ground positions.

## Fieldwork and instrumentation
- Instruments: two Leica VIVA GS10 GNSS receivers (base and roving).
- Equipment provided by NERC Geophysical Equipment Facility; receivers calibrated by manufacturer and tested with fixed antenna.

## Quality control and data quality
- Point accuracy quantified using standard deviations (SD_Easting, SD_Northing, SD_Ortho_Height).
- Notable data quality issue at a few points due to base station power failure; accuracy improved by differential correction using the BIGF Braemar reference station.

## Data governance, accessibility, and reuse considerations
- Clear documentation of coordinate systems, units, and data processing steps to support reproducibility and reuse.
- Per-date CSV structure facilitates time-sequenced comparisons of snow patch perimeters.
- Acknowledgments indicate external support and guidance to minimize disturbance to protected birds, highlighting environmental and ethical considerations.

## Context and acknowledgments
- Work supported by NERC Geophysical Equipment Facility loan.
- Acknowledges RSPB guidance on avoiding disturbance to protected birds.