# Details of data structure to ' Digestate_NF_SoilTemperature_WFPS.csv '

## Overview
- Supplement to the supporting documentation for data series (referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Dataset comprises 4 columns and 31,778 rows.
- Data originate from a digestate wheat trial conducted in 2017 at North Wyke Research station and Rothamsted Research.
- Measures soil temperature and water-filled pore space (WFPS) at a 2.5 cm soil depth across ten plots.

## Dataset Composition
- Columns (4 total):
  - Time: Date and time of day
  - Block: Blocks 1 to 5
  - Soil_Temperature_degrees_celcius: soil temperature at 2.5 cm depth (Degrees Celsius)
  - WFPS_percent: water-filled pore space at 2.5 cm soil depth (Percent)

## Context and Provenance
- Data derived from the digestate wheat trial of 2017, with experiments conducted at North Wyke Research station and Rothamsted Research.
- Part of a broader data series described in linked supporting documentation.

## Metadata and Data Quality Considerations
- Units are specified for each measurement (°C for soil temperature; % for WFPS) and depth is consistently 2.5 cm.
- Depth and location context provided; time resolution and exact data collection methods are not detailed in this excerpt.
- Metadata completeness beyond the listed columns is not described; alignment with broader data dictionary advisable.

## Structure, Access, and Discoverability
- Flat table structure with 4 fields and a single time-based measurement per row.
- File name: Digestate_NF_SoilTemperature_WFPS.csv, indicating a focused subset of the digestate dataset.
- Data likely intended for analysis of soil temperature and moisture relationships within the experimental blocks.

## Use Cases and Implications for Data Leaders
- Useful for analyses linking soil temperature to WFPS at shallow depth across plots and blocks.
- Supports cross-block and cross-site comparisons within the CINAg experimental framework.
- Emphasizes the need for robust metadata to enable discoverability, reproducibility, and reuse.

## Next Steps and Recommendations
- Validate time zone, date format, and any time-related missing values.
- Confirm interpretation of Block and how it maps to the experimental design.
- Document data collection methods, instruments used, and any data cleaning steps.
- Ensure comprehensive metadata coverage (data dictionary, sampling frequency, integrity checks) to improve discoverability and reuse, especially if shared beyond the originating project.