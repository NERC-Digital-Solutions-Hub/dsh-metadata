# clm_micromet_2016-2021_summaryqa.csv

- Overview
  - One spreadsheet dataset with 28 columns and 1683 rows.
  - Timeframe implied by filename: 2016–2021.
  - Measures soil temperature at two depths (5 cm and 20 cm) and soil moisture for 9 plots (Plot1–Plot9).

- Data structure and variables
  - Date: Year-Month-Day.
  - Soil temperature at 5 cm depth: TSoil5cm_Plot1_degC … TSoil5cm_Plot9_degC.
  - Soil temperature at 20 cm depth: TSoil20cm_Plot1_degC … TSoil20cm_Plot9_degC.
  - Soil moisture (volumetric water content): Soil_moisture_Plot1_m3_per_m-3 … Soil_moisture_Plot9_m3_per_m-3.
  - Each measurement includes units:
    - Temperature: degrees Celsius (degC).
    - Moisture: m3 m-3.
  - Note: The description lists a potential duplicate header entry for TSoil5cm_Plot4_degC, indicating a possible indexing error in the text.

- Data quality and encoding
  - Missing data indicated by 'NA'.
  - Faulty data replaced by '-9999'.
  - Data stored in a single spreadsheet with 28 columns (including Date).

- Notes on usage
  - Suitable for analyses of correlations, patterns, and potential predictive insights across multiple plots and depths.
  - Be mindful of scale and data completeness when conducting local-level analyses.