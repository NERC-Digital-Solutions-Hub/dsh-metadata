# Ciste Mhearad Snow Patch Perimeter GNSS Dataset

- The dataset documents perimeter measurements of the late-lying Ciste Mhearad snow patch taken on three dates in 2023: 19 June, 27 July, and 28 July.
- Data were collected with two GNSS receivers and post-processed to provide precise spatial positions.

## Scope and Content
- Three per-date CSV files storing perimeter measurements:
  - ociste_mhearad_snow_patch_19062023.csv (perimeter measured on 19/06/2023)
  - ociste_mhearad_snow_patch_27072023.csv (perimeter measured on 27/07/2023)
  - ociste_mhearad_snow_patch_28072023.csv (perimeter measured on 28/07/2023)
- Coordinates and elevations are provided in multiple reference systems.

## Data Records and Structure
- Columns (examples):
  - Date_Time: date and time in dd/MM/yyyy hh:mm
  - Easting: Easting in metres (UTM zone 30N)
  - Northing: Northing in metres (UTM zone 30N)
  - WGS84_Latitude: Latitude in degrees (WGS84)
  - WGS84_Longitude: Longitude in degrees (WGS84)
  - Ortho_Height: Height above mean sea level (metres)
  - SD_Easting: Standard deviation of easting (m)
  - SD_Northing: Standard deviation of northing (m)
  - SD_Ortho_Height: Standard deviation of height (m)
- Notes: A separate CSV file exists for each measurement date.

## Data Collection and Processing
- Method: GNSS roving survey along the snow patch perimeter with a 2 m vertical pole, spaced approximately 1 m apart along the perimeter; each point recorded for ~20 seconds.
- Instrumentation: Two Leica VIVA GS10 GNSS receivers (loaned by NERC Geophysical Equipment Facility); receivers calibrated by the manufacturer and tested with a fixed antenna.
- Processing: Post-processed using Leica Infinity software.
- Reference framework: Horizontal positions provided in UTM zone 30N and in WGS84 lat/long; orthometric heights referenced to mean sea level.
- Pole height: Subtracted during processing to obtain true horizontal/vertical positions.

## Quality Control and Uncertainty
- Reported accuracy indicators:
  - Standard deviations included for easting, northing, and orthometric height.
  - In 19/06/2023 and related points, a temporary rise in horizontal SD to 0.01 m and vertical SD to 0.04 m occurred due to base station power failures.
  - Differential accuracy was achieved by tying problematic points to the BIGF station at Braemar (19 km away).

## Provenance, Documentation, and Acknowledgments
- Documentation of data collection context and methods included within the dataset description.
- Acknowledgments: Supported by NERC Geophysical Equipment Facility loan 1164; RSPB advised on minimizing disturbance to protected birds.

## Data Management and Stewardship Implications
- Metadata richness: clear data provenance, coordinate reference systems, and measurement methodology are captured in the dataset files and descriptions.
- Formats and standards: CSV files with explicit coordinate systems and units; consistent field naming across dates.
- Reuse considerations for Data Stewards:
  - Ensure complete metadata (methods, coordinate reference systems, date range, data creator, and licensing) accompanies the dataset for discoverability.
  - Maintain links to instrumentation details and processing workflow (Leica Infinity) to support reproducibility.
  - Plan for updates or additions if new dated measurements are collected or if reprocessing is performed.
  - Note data limitations (temporary GPS reliability issues) and document any known constraints affecting future sharing or interpretation.