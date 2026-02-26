# Details of data structure for 'Daily micromet data_1998to2015_Clocaenog.csv'

- Scope
  - Supplement to the supporting documentation for data series documenting daily micrometeorological measurements at Clocaenog.
  - Covers daily observations from 05/11/1998 to 30/06/2015.

- Dataset content and structure
  - One spreadsheet with 38 columns.
  - Variables per plot (plots 1–9):
    - Soil temperature at 5 cm depth
    - Soil temperature at 20 cm depth
    - Air temperature at 20 cm above the soil surface
    - Soil moisture (m3/m3)
  - The second row contains the plot numbers.
  - Date column present to align daily observations across plots.
  - Missing data are represented by empty cells.

- Data specifics and units
  - Temperature measurements in degrees Celsius.
  - Soil moisture in cubic meters per cubic meter (m3/m3).
  - Data are organized by date and by plot-variable combinations, enabling cross-plot comparisons.

- Data quality and gaps
  - Data may have gaps (empty cells indicate missing days/measurements).
  - Structure implies potential need for metadata on measurement methods, sensor types, and data quality flags to support governance and usability.

- Governance and usage considerations for Data Leaders
  - Ensure discoverability and metadata completeness (column definitions, units, plot mapping).
  - Track data provenance and versioning within the Clocaenog dataset lineage.
  - Plan for data quality assessment and gap filling strategies if analytics require complete time series.
  - Align with broader data strategy by documenting data availability, granularity, and any access restrictions or data protection considerations.
  - Use the dataset to support cross-plot analyses of micrometeorological conditions, with attention to temporal alignment and missing data handling.