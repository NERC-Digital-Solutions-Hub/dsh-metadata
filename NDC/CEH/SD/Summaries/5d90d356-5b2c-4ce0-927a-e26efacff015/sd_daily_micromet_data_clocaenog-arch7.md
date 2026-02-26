# Details of data structure

- File and scope
  - Dataset: clm_micromet_2016-2021_summaryqa.csv
  - Structure: 28 columns, 1683 rows
  - Time span: 2016–2021
  - Data type: Micrometeorological measurements across nine plots

- Date and measurements
  - Date column: Year-Month-Day
  - Temperature measurements
    - TSoil5cm_Plot1_degC through TSoil5cm_Plot9_degC (soil temperature at 5 cm depth)
    - TSoil20cm_Plot1_degC through TSoil20cm_Plot9_degC (soil temperature at 20 cm depth)
  - Soil moisture measurements
    - Soil_moisture_Plot1_m3_per_m-3 through Soil_moisture_Plot9_m3_per_m-3 (volumetric water content)

- Data quality and coding
  - Missing data: marked as 'NA'
  - Faulty data: replaced by '-9999'
  - Units
    - Temperature: degrees Celsius (°C)
    - Soil moisture: m3 m-3

- Column labeling pattern
  - B–J: TSoil5cm_Plot1_degC to TSoil5cm_Plot9_degC
  - K–S: TSoil20cm_Plot1_degC to TSoil20cm_Plot9_degC
  - T–AB: Soil_moisture_Plot1_m3_per_m-3 to Soil_moisture_Plot9_m3_per_m-3

- Practical notes for GIS use
  - The dataset is tabular and time-series across plots; to map, you should join with spatial plot locations (coordinates) for each plot
  - Handle -9999 and NA values during analysis or visualization
  - Ensure unit consistency when integrating with other data sources or map layers