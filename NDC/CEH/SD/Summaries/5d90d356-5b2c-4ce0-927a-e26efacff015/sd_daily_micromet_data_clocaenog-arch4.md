# Details of data structure

- Dataset scope
  - A single CSV file containing micrometeorological data collected from 2016 to 2021.
  - 28 columns in total and 1683 rows.

- Column groups and content
  - Date: header is Date; format is Year-Month-Day.
  - Soil temperature at 5 cm depth (TSoil5cm) for plots 1 through 9: TSoil5cm_Plot1_degC, ..., TSoil5cm_Plot9_degC.
  - Soil temperature at 20 cm depth (TSoil20cm) for plots 1 through 9: TSoil20cm_Plot1_degC, ..., TSoil20cm_Plot9_degC.
  - Soil moisture (volumetric water content) for plots 1 through 9: Soil_moisture_Plot1_m3_per_m-3, ..., Soil_moisture_Plot9_m3_per_m-3.
  - Units: Temperature in degrees Celsius (o C); Soil moisture in m3/m3; Date as Year-Month-Day.

- Data quality and coding
  - Missing or not recorded data marked as 'NA'.
  - Faulty or invalid data replaced by '-9999'.

- File and documentation details
  - File name: clm_micromet_2016-2021_summaryqa.csv.
  - Each column includes a header, unit, and description:
    - Example: TSoil5cm_Plot1_degC – Soil temperature at 5 cm depth for plot 1 (unit: °C).
    - Example: Soil_moisture_Plot1_m3_per_m-3 – Soil volumetric water content for plot 1 (unit: m3/m3).

- Data structure scale
  - 28 columns to capture 3 variables (date, soil temperature at two depths, soil moisture) across 9 plots.
  - 1683 rows representing time-series observations within the 2016–2021 window.

- Usage and integration notes
  - Structured for cross-plot and cross-depth comparisons.
  - Clear metadata facilitates discoverability and interpretation, though users should account for missing data and the -9999 flag during analysis.