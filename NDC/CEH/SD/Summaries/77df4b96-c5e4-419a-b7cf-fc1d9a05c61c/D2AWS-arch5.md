# Automatic Weather Station recordings from Moor House and Helbeck, Cumbria, 1974 - 1987

## Overview
- Historic dataset of Automatic Weather Station (AWS) observations from Helbeck and Moor House, Cumbria, UK.
- Collected by Ken Taylor; stored in a database described by Cuthbertson (1993).
- Moor House location continues to be monitored by the UK Environmental Change Network (ECN).

## Provenance and context
- Data collection: Automatic Weather Stations at Helbeck (near Brough) and Moor House.
- Site locations:
  - Helbeck AWS: grid reference 378900 516000.
  - Moor House AWS: grid reference 375100 533400.
- ECN continues monitoring at Moor House (Rennie et al., 2017) with related data portal entry.

## Dataset structure and contents
- Data are organized into multiple recording series with different temporal resolutions (hourly or daily) and date ranges, identified by DATID:
  - 40: Helbeck – Hourly readings. Earliest 01-Jan-78 to 18-Oct-83.
  - 6: Helbeck – Hourly readings. May 1974 – June 1978.
  - 7: Helbeck – Daily readings. May 1974 – June 1978.
  - 5: Moor House – Daily readings. July 1974 – August 1979.
  - 41: Moor House – Hourly readings. 01-Jan-79 to 08-Feb-87.
  - 4: Moor House – Hourly readings. July 1974 – August 1979.
- Variables included (with units as described in the dataset):
  - DATID: Data set identification record number.
  - NO_REC: Number of recordings used to establish the value.
  - REC_TIME: Date of the reading (DD-MM-YYYY).
  - REC_HOUR: Hour of the reading (0–23).
  - SOL_RAD: Solar radiation (units vary; described as Watts per square metre in some entries).
  - AIR_TEMP: Air temperature (°C).
  - DEP_TEMP: Temperature depression (°C) – difference between dry and wet bulb temperatures.
  - WIND_VEL: Wind velocity (units reported as kilometres; varies by entry).
  - WIND_DIR: Wind direction.
  - RAINFALL: Rainfall (mm).
- Data include multiple measurements per day (hourly) or per day (daily) depending on the DATID.

## Temporal coverage
- Range spans 1974–1987 across sites and series, with gaps depending on the DATID:
  - Helbeck: 1974–1978 (some hourly and some daily series), extending to 1983 in one hourly series.
  - Moor House: 1974–1979 (daily and hourly series) and 1979–1987 for a separate hourly series.

## Data quality and metadata
- Missing values are present in several records; reasons for missing data are not documented.
- Quality assurance procedures are not known, as this is a historic dataset.
- A dataset description and variable definitions are provided, but QA provenance and data cleaning status are unclear.
- Metadata notes:
  - Site coordinates and data collection context are documented.
  - The dataset references a 1993 database publication and a later ECN data continuity at Moor House, indicating potential for cross-reference or linking to additional metadata.

## Data governance and stewardship considerations
- Governance needs:
  - Establish or confirm data quality procedures for historic AWS data (imputation, QA checks, provenance tracking).
  - Harmonize differing temporal resolutions (hourly vs daily) and ensure consistent units across DATIDs.
  - Validate and document the meaning of SOL_RAD unit specifications across entries.
- Metadata and discovery:
  - Ensure dataset-level metadata includes provenance (Ken Taylor), storage history (Cuthbertson 1993), and ECN continuity reference.
  - Provide a data dictionary and a clear data dictionary mapping for all variables, units, and DATID-specific notes.
- Access and sharing:
  - Determine appropriate access policy for historic AWS data and any embargo or licensing constraints.
  - Consider linking to ECN/NERC Environmental Information Data Centre for discoverability and updates.
- Reuse and interoperability:
  - Align with standard meteorological data formats and conventions to facilitate reuse by data users.
  - Document any data transformations performed during sharing (cleaning, aggregation, unit conversions).

## Practical implications for data stewards
- Actionable steps:
  - Compile a complete data dictionary with consistent units and definitions for SOL_RAD, WIND_VEL, and DEP_TEMP across all DATIDs.
  - Audit missing values and define a strategy (e.g., flag, imputation, or exclusion) and document rationale.
  - Capture and preserve data provenance, including collection methods, instruments, and maintenance notes.
  - Facilitate interoperability by providing machine-readable metadata and, if possible, a consolidated data file that harmonizes the multiple DATIDs into a single coherent dataset.
  - Document and communicate any updates or corrections, and establish a plan for ongoing access via ECN or related data centers.

## Next steps and recommendations
- Create a consolidated metadata record summarizing all DATIDs, site locations, variables, units, and date ranges.
- Develop a data quality plan for historical AWS data, including QA checks and acceptable data gaps.
- Provide data access guidance, including preferred formats, licensing, and related EU/ECN data portal references.
- Consider adding a data stewardship note describing the collection context, collector (Ken Taylor), and referenced publications for traceability.