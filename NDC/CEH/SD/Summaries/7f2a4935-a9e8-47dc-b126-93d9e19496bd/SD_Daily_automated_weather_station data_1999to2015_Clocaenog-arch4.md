# Details of data structure for 'Daily automated weather station data_1999to2015_Clocaenog.csv'

## Overview
- Supplement to supporting documentation for data series
- Dataset comprises one spreadsheet with 12 columns
- File name: Daily automated weather station data_1999to2015_Clocaenog.csv
- Time coverage: 12/06/1999 to 30/06/2015
- Empty cells indicate days with no data

## Data fields
- Date
- Relative humidity as a percent
- Mean air temperature in degrees Celsius
- Maximum air temperature in degrees Celsius
- Minimum air temperature in degrees Celsius
- Rainfall in millimetres
- Air pressure in Millibars
- Net radiation in Millivolts
- Solar radiation as kilowatts per metre square
- Photosynthetic active radiation as micromoles per metre square per second
- Wind speed as metres per second
- Wind direction as degrees

## Units
- The second row contains the units for each variable (as listed above)

## Data structure and interpretation
- Date is continuous; first entry 12/06/1999; last entry 30/06/2015
- The dataset is a single spreadsheet
- Empty cells denote days with no data

## Implications for Data Leaders
- Plan for addressing missing data indicated by empty cells to maintain completeness
- Leverage the explicit units row to support metadata quality and interoperability
- Recognize the dataset as a continuous daily time series from a weather station, useful for integration with broader data assets
- Ensure data provenance and documentation beyond the second row to support long-term discoverability and use