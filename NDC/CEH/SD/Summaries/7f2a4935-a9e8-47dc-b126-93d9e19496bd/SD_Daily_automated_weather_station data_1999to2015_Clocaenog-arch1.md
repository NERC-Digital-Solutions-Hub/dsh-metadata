# Details of data structure for 'Daily automated weather station data_1999to2015_Clocaenog.csv'

- Overview
  - This document serves as a supplement to the supporting documentation for the data series and describes the data structure of the daily automated weather station data for Clocaenog, covering 1999 to 2015.
  - The dataset is provided as a single spreadsheet and includes a defined set of meteorological variables with their units.

- Data columns and units
  - 12 columns: Date, Relative humidity (%), Mean air temperature (°C), Maximum air temperature (°C), Minimum air temperature (°C), Rainfall (mm), Air pressure (mb), Net radiation (millivolts), Solar radiation (kilowatts per square metre), Photosynthetic active radiation (µmol/m²/s), Wind speed (m/s), Wind direction (degrees).
  - The second row of the spreadsheet contains the units for each variable.

- Time span and data completeness
  - Date range: from 12/06/1999 to 30/06/2015.
  - The presence of empty cells indicates missing data for those days.

- Data format and accessibility
  - Data are organized in a single spreadsheet with the 12 specified columns.
  - This description is part of the supplementary documentation for the data series; access and use may be governed by the accompanying supporting documents (e.g., Clocaenog_supporting documentation_Data series.rtf).

- Considerations for analysts
  - Expect daily time series with potential gaps due to missing values on certain days.
  - Units are listed in a separate row; ensure correct interpretation during data import.
  - Some variables (e.g., Net radiation in millivolts) may require attention to sensor calibration or contextual interpretation when conducting analyses.