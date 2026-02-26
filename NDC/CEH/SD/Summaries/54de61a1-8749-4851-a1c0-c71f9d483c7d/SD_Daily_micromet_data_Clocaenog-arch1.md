# This document is a supplement to the supporting documentation for data series detailed in: 'Clocaenog_supporting documentation_Data series.rtf'

- Overview
  - Provides details of the data structure for the dataset referenced in the supporting documentation.
  - The dataset is intended for analysis of environmental variables across plots.

- Data structure details
  - The dataset is a single spreadsheet with 38 columns.
  - Columns include: Date, soil temperature at 5 cm soil depth for plots 1-9, soil temperature at 20 cm soil depth for plots 1-9, air temperature 20 cm above the soil surface for plots 1-9, and soil moisture (m3/m3) for plots 1-9.
  - The second row contains the plot number.
  - Empty cells indicate that data are not available for that day.

- Data quality and considerations
  - Data are organized as a time series across 9 plots.
  - Units implied: temperatures in degrees Celsius; soil moisture in cubic meters per cubic meter.
  - Missing data (empty cells) may require imputation or special handling in analyses.

- Analytical opportunities for Analysts
  - Investigate correlations between soil temperatures at different depths, air temperature, and soil moisture across plots.
  - Develop predictive models of soil moisture or temperature using date and other variables.
  - Explore spatial (between plots) and temporal (across dates) patterns.

- Practical notes
  - This document is supplementary to the main dataset documentation; cross-reference with "Clocaenog_supporting documentation_Data series.rtf" for full context.
  - Be aware of the column count discrepancy (38 columns noted) versus described structure. Verify consistency when accessing the raw file.