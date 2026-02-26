# Clocaenog_supporting documentation_Data series.rtf

## Purpose and context
- This document serves as a supplement to the supporting documentation for the data series.
- It describes the data structure of the dataset used in the monitoring framework.

## Dataset structure
- One spreadsheet with 38 columns.
- Columns include:
  - Date
  - Soil temperature at 5 cm depth for plots 1–9
  - Soil temperature at 20 cm depth for plots 1–9
  - Air temperature at 20 cm above the soil surface for plots 1–9
  - Soil moisture (m3/m3) for plots 1–9
- The second row contains the plot number.
- Empty cells indicate that data are not available for that day.

## Data quality and governance considerations
- Metadata clarity: column meanings, plot indexing, and depth references must be well-documented.
- Handling missing data: empty cells signal gaps; governance should address imputation or gap reporting.
- Consistency and transformation: dataset may require cleaning and transformation to ensure comparability across plots and variables.

## Practical notes for monitoring implementation
- Variables cover key environmental indicators: soil temperature at two depths, ambient air temperature, and soil moisture.
- Temporal dimension is represented by Date; spatial dimension by plots 1–9.
- Plot numbers are defined in the second row, which is essential for correct interpretation.

## Recommendations for authors of monitoring frameworks
- Ensure robust metadata standards accompany the dataset (units, depths, plot IDs).
- Establish data quality checks and explicit handling of missing data.
- Promote data accessibility and linkage to the supporting documentation to support reproducibility and informed decision-making.