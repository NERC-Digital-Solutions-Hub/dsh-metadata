# Details of data structure

## Overview
- A single spreadsheet dataset named clm_micromet_2016-2021_summaryqa.csv.
- Contains 28 columns and 1683 rows, covering data from 2016–2021.
- Columns capture soil temperature at two depths (5 cm and 20 cm) and soil moisture across nine plots (1–9).
- Data quality flags: missing values marked as NA; faulty data replaced by -9999.
- Each column includes a header, unit, and description, enabling standardized interpretation and downstream processing.

## Columns and metadata
- Date: Year-Month-Day (ISO-like date format).
- Soil temperature at 5 cm depth (°C) for plots 1–9: TSoil5cm_Plot1_degC, TSoil5cm_Plot2_degC, …, TSoil5cm_Plot9_degC.
- Soil temperature at 20 cm depth (°C) for plots 1–9: TSoil20cm_Plot1_degC, TSoil20cm_Plot2_degC, …, TSoil20cm_Plot9_degC.
- Soil moisture (m3 per m3) for plots 1–9: Soil_moisture_Plot1_m3_per_m-3, Soil_moisture_Plot2_m3_per_m-3, …, Soil_moisture_Plot9_m3_per_m-3.
- Units:
  - Temperature: degrees Celsius (°C).
  - Soil moisture: cubic meters per cubic meter (m3/m3).
- Documentation per column includes a clear header, unit, and description (e.g., “Soil temperature at 5cm depth for plot 1,” etc.).

## Data quality and handling
- NA indicates data not recorded for that entry.
- -9999 indicates faulty data that has been replaced in the dataset.
- The structure supports quality assurance, cleaning, and transforming processes common in environmental monitoring workflows.

## Context and use for monitoring
- Fits into standardized environmental monitoring efforts by providing a structured, time-series view of below-ground temperature and moisture across multiple plots.
- Facilitates cross-plot and multi-depth analyses to assess soil conditions over time.
- The standardized metadata enhances interoperability when combining with other datasets or feeding into dashboards, reports, or policy performance assessments.

## Considerations for analysts
- Useful as a baseline for temporal trend analyses of soil conditions across multiple plots and depths.
- Can be merged with other environmental datasets to increase dataset value and enable broader habitat or land-management assessments.
- Ensure consistent handling of NA and -9999 values during QA/QC and downstream analyses; consider documenting data gaps and any imputation strategies.