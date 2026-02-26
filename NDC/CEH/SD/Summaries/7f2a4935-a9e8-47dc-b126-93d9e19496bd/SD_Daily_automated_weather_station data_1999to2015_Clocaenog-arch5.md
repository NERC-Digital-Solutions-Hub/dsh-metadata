# Details of data structure for 'Daily automated weather station data_1999to2015_Clocaenog.csv'

## Overview
- Supplement to the supporting documentation for data series related to Clocaenog.
- Dataset comprises a single spreadsheet with 12 columns.
- The second row provides the units for each variable.
- Date range runs from 12/06/1999 to 30/06/2015.
- Empty cells indicate missing data for a given day.

## Dataset structure and fields
- 12 columns:
  - Date
  - Relative humidity as a percent
  - Mean air temperature in degrees Celsius
  - Maximum air temperature in degrees Celsius
  - Minimum air temperature in degrees Celsius
  - Rainfall in millimetres
  - Air pressure in Millibars
  - Net radiation in Millivolts
  - Solar radiation as kilowatts per metre square
  - Photosynthetic active radiation as micomoles per metre square per second
  - Wind speed as metres per second
  - Wind direction as degrees
- The first row contains headers; the second row contains units for each variable.

## Temporal coverage and data completeness
- Daily observations spanning 1999-06-12 to 2015-06-30.
- Presence of missing data indicated by empty cells.

## Data quality and interpretation notes
- Units are provided in the second row; ensure interpretation uses the stated units.
- Net radiation is listed as Millivolts, which may require verification against standard meteorological units.
- Missing data should be accounted for in analyses (imputation or exclusion as appropriate).
- Verify consistency of units across the full time span and with the supporting documentation.

## Metadata, provenance, and documentation
- This file is a data-structure detail supplement to the Clocaenog supporting documentation.
- Clear linkage to the dataset’s broader metadata and data series documentation is recommended for context, lineage, and versioning.

## Governance, storage, and sharing considerations
- Ensure the dataset is stored with version control and proper cataloging.
- Document data availability, potential disclosure risks, embargoes, or proprietary constraints as applicable (not explicitly stated in the document but part of standard data stewardship practice).
- Maintain alignment between the data file and its metadata (headers and units) to support discoverability and reuse.

## Practical guidance for use and reuse
- Read the header row to identify variables; consult the second row for units.
- Treat empty cells as missing data and plan analysis accordingly.
- Use the date range to assess time series continuity and identify gaps.
- Cross-reference with the Clocaenog supporting documentation for full context and any preprocessing steps.