# Details of data structure for 'Water table depth_Clocaenog.csv'

- This document is a supplement to the supporting documentation for data series related to Clocaenog.
- Focuses on the structure of the Water table depth_Clocaenog.csv dataset.

## Data structure

- One spreadsheet containing 10 columns.
- Column 1: Date, spanning from 13/05/1999 to 30/06/2015.
- Columns 2–10: water table depth measurements (cm) from the soil surface for experimental plots 1–9.
- Entries may include the value 'below detectable limit' to indicate depths under the detection threshold.

## Data content specifics

- Time series across approximately 16 years.
- Nine plots measured; each plot has a dedicated column (2–10).
- Dates are in a day/month/year format consistent with the dataset; consider standardizing to ISO 8601 for interoperability.
- Measurement unit is centimetres (cm).

## Data quality and interpretation

- Presence of censored values ('below detectable limit') requires special handling during analysis (e.g., substitution rules, censored data methods).
- The document does not include methodological details (measurement technique, equipment, calibration); refer to the accompanying supporting documentation for context.
- No explicit mention of missing data beyond censored values; verification may be needed.

## Metadata and discoverability

- Dataset name: Water table depth_Clocaenog.csv.
- Part of a larger data series with supporting documentation (Clocaenog_supporting documentation_Data series.rtf).
- Clear mapping: Date column plus nine plot-specific measurement columns; strong potential for cross-plot comparisons if metadata (units, methods) are consistent.

## Access, governance, and usage considerations

- Ensure comprehensive metadata is captured (units, data collection methods, data steward, update schedule, licensing).
- Improve discoverability by including a data dictionary, data quality flags, and provenance in the metadata.
- For integration with other datasets, standardize date formats and clearly document handling of 'below detectable limit' values.

## Next steps for Data Leaders

- Normalize date formats to a consistent standard (e.g., ISO 8601).
- Establish and document a policy for treating 'below detectable limit' values in analyses.
- Link to and incorporate the full methodology from the supporting documentation.
- Create or update metadata to include units, measurement methods, frequency, and data provenance.
- Assess data completeness and identify any gaps across the date range or plots for planning updates.