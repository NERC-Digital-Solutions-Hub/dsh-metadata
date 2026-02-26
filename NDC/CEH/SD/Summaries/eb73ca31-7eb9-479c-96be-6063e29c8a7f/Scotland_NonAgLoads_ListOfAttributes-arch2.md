# Data Structure

- The Non-agricultural pollution to rivers in Scotland data is stored in two CSV files: NonAgLoadsInland_Scotland.csv (inland catchments) and NonAgLoadsCoastal_Scotland.csv (coastal catchments).
- Purpose: to quantify non-agricultural pollution loads to Scotland’s rivers and enable spatial analysis by linking to Water Framework Directive (WFD) catchment polygons.

- Key identifiers:
  - CATCH_ID: Unique WFD catchment identifier
  - INLAND_ID: SEPA ID for inland catchments
  - COASTAL_ID: SEPA ID for coastal catchments

- Load variables (sediment):
  - STW_Z: Suspended solids load from sewage treatment works (kg sediment per year)
  - Urban_Z: Sediment load from urban areas (kg sediment per year)
  - Wood_Z: Sediment load from woodland areas (kg sediment per year)
  - Bank_Z: Sediment from local bank erosion (kg sediment per year)
  - Montane_Z: Sediment from montane areas (kg sediment per year)
  - Other_Z: Sediment from other areas (kg sediment per year)

- Load variables (phosphorus):
  - STW_P: Orthophosphate load from sewage treatment works (kg phosphorus per year)
  - SEP_P: Total phosphate load from septic tanks (kg phosphorus per year)
  - Urban_P: Phosphorus load from urban areas (kg phosphorus per year)
  - Wood_P: Phosphorus load from woodland areas (kg phosphorus per year)
  - Bank_P: Total phosphorus from local bank erosion (kg phosphorus per year)
  - Montane_P: Phosphorus load from montane areas (kg phosphorus per year)
  - Other_P: Phosphorus load from other areas (kg phosphorus per year)

- Load variables (nitrogen):
  - STW_N: Inorganic nitrogen load from sewage treatment works (kg nitrate per year)
  - SEP_N: Total nitrogen load from septic tanks (kg nitrate per year)
  - Urban_N: Nitrogen load from urban areas (kg nitrate per year)
  - Wood_N: Nitrogen load from woodland areas (kg nitrate per year)
  - Bank_N: Total nitrogen from local bank erosion (kg nitrate per year)
  - Montane_N: Nitrogen load from montane areas (kg nitrate per year)
  - Other_N: Nitrogen load from other areas (kg nitrate per year)

- Load variables (faecal coliform):
  - STW_F: Faecal coliform load from sewage treatment works (10^6 cfu per year)
  - SEP_F: Faecal coliform load from septic tanks (10^6 cfu per year)
  - Urban_F: Faecal coliform load from urban areas (10^6 cfu per year)

- Data usage and GIS mapping:
  - The columns INLAND_ID and COASTAL_ID enable joining the CSVs to the WFD catchment feature class or shapefile for GIS analysis.
  - The WFD catchments dataset is not published by SEPA yet, but there is an intention to add it to SEPA’s Environmental data page.

- Reference:
  - Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.