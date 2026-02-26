# Details of data structure for 'Daily automated weather station data_1999to2015_Clocaenog.csv'

- Purpose and scope
  - Supplement to supporting documentation for the data series.
  - Describes the data structure of the daily automated weather station dataset.

- Dataset basics
  - One spreadsheet with 12 columns.
  - Date range: 12/06/1999 to 30/06/2015.
  - Empty cells indicate days with no data (missing data).

- Columns and units
  - Date
  - Relative humidity: percent
  - Mean air temperature: degrees Celsius
  - Maximum air temperature: degrees Celsius
  - Minimum air temperature: degrees Celsius
  - Rainfall: millimetres
  - Air pressure: millibars
  - Net radiation: millivolts
  - Solar radiation: kilowatts per square metre
  - Photosynthetically active radiation: micromoles per square metre per second
  - Wind speed: metres per second
  - Wind direction: degrees
  - The second row contains the units for each variable.

- GIS considerations
  - Useful for map-based temporal analyses when integrated with spatial context (e.g., weather station location, or combined with multiple stations).
  - Provides a rich set of daily climate variables for visualization and trend analysis.
  - Note potential data quality issues:
    - Missing data days.
    - Non-standard unit for net radiation (verify and, if needed, convert to standard units like W/m^2).
    - Ensure consistent date formatting and time zone handling for GIS applications.

- Data preparation guidance
  - Validate and standardize units across the dataset.
  - Address missing values for analyses requiring continuous data.
  - Align dates to a consistent format for integration with GIS workflows.
  - Consider combining with spatial metadata or additional stations for broader GIS analyses.

- Context and references
  - Part of the Clocaenog data series documentation; related to the file Clocaenog_supporting documentation_Data series.rtf.