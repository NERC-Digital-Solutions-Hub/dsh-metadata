# Light penetration for determination of the euphotic zone in Durleigh Reservoir, 2018

## Overview
- Purpose: Light penetration measurements to determine the euphotic zone in Durleigh Reservoir, 2018.
- Instrumentation: HOBO Pendant Temperature/Light 8K Loggers.
- Depths: 0.5 m, 1.5 m, and 2.5 m.
- Location: lat 51.1210, lon -3.0403.
- Timeframe: Deployments between 30/05/2018 and 05/10/2018.
- Data frequency: Measurements taken every 10 minutes.
- File naming: Filenames include depth, e.g., '0.5mPENDANT.csv'.
- Measurement units: Light intensity in lum/ft²; Temperature in °F.
- Date/time format: mm/dd/yyyy HH:MM:SS.
- Authors and citation: Authors Slavin, E.I., and Wain, D.J.; dataset cited as Slavin and Wain (2018); also noted as Salvin, E.I., Wain, D.J. 2018 in the metadata.

## Data collection and structure
- Data collection method: Light intensity readings at specified depths using HOBO loggers.
- Depth-specific data: Each depth has an accompanying CSV file (e.g., 0.5mPENDANT.csv).
- Metadata context: Includes deployment dates, location, depth information, and measurement interval.
- Output format: CSV files per depth; accompanying metadata/dateline referenced as a metadate file.

## Dataset structure and metadata
- Key fields: Depth, location coordinates, date/time stamps, light units (lum/ft²), temperature units (°F), and sampling interval (every 10 minutes).
- Time representation: Date and time stamped in mm/dd/yyyy HH:MM:SS format.
- Metadata completeness: Includes depth, site coordinates, depth-specific filenames, units, and sampling cadence.

## Data quality, standards, and stewardship considerations
- Clear attribution of authors and dataset citation.
- Defined units and measurement interval support reuse, but additional quality flags or calibration details are not specified here.
- For long-term reuse, consider adding:
  - Sensor calibration and serial numbers.
  - Data quality flags (e.g., море or questionable readings).
  - Calibration/maintenance logs and metadata completeness notes.
  - Licensing and usage rights.

## Access, sharing, and provenance
- Indication of a metadate file and the intention to upload datasets to relevant portals and catalogues.
- Governance needs:
  - Confirm data licensing and access permissions.
  - Define update and versioning procedures if data are refreshed.
  - Ensure consistent file naming and metadata schemas across depths.

## Practical considerations for Data Stewards
- Ensure consistency across all depth files (naming, units, date formats).
- Validate time stamps and sampling interval remaining uniform throughout the dataset.
- Maintain clear provenance by preserving authorship and correct citation guidance.
- Plan for potential data sharing constraints (embargoes, proprietary concerns) and document any limitations.