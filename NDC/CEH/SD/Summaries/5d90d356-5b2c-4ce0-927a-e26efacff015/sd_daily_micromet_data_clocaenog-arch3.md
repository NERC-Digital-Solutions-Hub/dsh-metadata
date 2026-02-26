# Details of data structure

## Dataset at a glance
- Single spreadsheet with 28 columns and 1683 rows.
- Variables include:
  - Date (Year-Month-Day)
  - Soil temperature at 5 cm depth for plots 1–9 (TSoil5cm_Plot1_degC to TSoil5cm_Plot9_degC)
  - Soil temperature at 20 cm depth for plots 1–9 (TSoil20cm_Plot1_degC to TSoil20cm_Plot9_degC)
  - Soil volumetric water content for plots 1–9 (Soil_moisture_Plot1_m3_per_m-3 to Soil_moisture_Plot9_m3_per_m-3)
- Data markings:
  - Missing values noted as 'NA'
  - Faulty data replaced by '-9999'
- Units:
  - Temperature: degrees Celsius (°C)
  - Soil moisture: m3 per m3 (dimensionless volumetric water content)

## Columns and definitions
- 28 columns total:
  - Date
  - TSoil5cm_Plot1_degC through TSoil5cm_Plot9_degC
  - TSoil20cm_Plot1_degC through TSoil20cm_Plot9_degC
  - Soil_moisture_Plot1_m3_per_m-3 through Soil_moisture_Plot9_m3_per_m-3
- Each column includes a header, unit, and description:
  - Example descriptions: “Soil temperature at 5cm depth for plot X”; “Soil temperature at 20cm depth for plot X”; “Soil volumetric water content for plot X”

## Data quality and handling
- Missing data indicated as 'NA'
- Faulty data replaced by '-9999' (flagged as invalid)
- Metadata provided for each column (header, unit, description)
- Potential labeling inconsistency in the listed 5 cm temperature columns (e.g., repeated Plot4 label); verify mappings to plots during use

## Data size and structure implications for monitoring
- 1683 observations over time across 9 plots and 3 variable types (5cm temp, 20cm temp, moisture)
- Suitable for time-series analysis of soil conditions across multiple plots and depths
- Requires careful handling of -9999 and 'NA' values during analysis and reporting

## Practical implications for monitoring frameworks
- Enables multi-plot, multi-depth comparison of soil conditions to inform environmental health assessments
- Emphasizes the need for robust metadata and data provenance to support data governance
- Highlights common data-management considerations relevant to monitoring programs:
  - Clear metadata (units, descriptions) and consistent column mappings
  - Accessibility and sharing of underlying data for transparency
  - Maintaining data quality through consistent handling of missing and erroneous values