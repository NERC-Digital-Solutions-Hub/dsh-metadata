# Data Structure

- The Non-agricultural pollution to rivers in Scotland data are stored in two CSV files: NonAgLoadsInland_Scotland.csv and NonAgLoadsCoastal_Scotland.csv.
- The data can be mapped in GIS by joining these CSVs to Water Framework Directive (WFD) catchment polygons for Scotland.
- Key identifiers:
  - CATCH_ID: Unique identifier of the WFD river catchment (units: -).
  - INLAND_ID: SEPA ID for inland catchments (units: -).
  - COASTAL_ID: SEPA ID for coastal catchments (units: -).
- WFD catchments dataset is not published by SEPA yet; SEPA intends to add it to its Environmental data page.

## Data Files and Structure

- Columns include: name, description, and unit (as described in the accompanying table).
- The catchment IDs link each record to specific WFD catchments or SEPA-defined inland/coastal areas.

## Variables and Units

- Sediment loads:
  - STW_Z: Suspended solids load from sewage treatment works (kg sediment per yr).
  - Urban_Z: Suspended solids load from urban areas (kg sediment per yr).
  - Wood_Z: Suspended solids load from woodland areas (kg sediment per yr).
  - Bank_Z: Total sediment from local bank erosion (kg sediment per yr).
  - Montane_Z: Suspended solids load from montane areas (kg sediment per yr).
  - Other_Z: Sediment load from other areas (kg sediment per yr).

- Phosphorus loads:
  - STW_P: Orthophosphate load from sewage treatment works after UWWTD secondary treatment (kg phosphorus per yr).
  - SEP_P: Total phosphate load from septic tanks (kg phosphorus per yr).
  - Urban_P: Phosphorus load from urban areas (kg phosphorus per yr).
  - Wood_P: Phosphorus load from woodland areas (kg phosphorus per yr).
  - Bank_P: Total phosphorus from local bank erosion (kg phosphorus per yr).
  - Montane_P: Phosphorus load from montane areas (kg phosphorus per yr).
  - Other_P: Phosphorus load from other areas (kg phosphorus per yr).

- Nitrogen loads:
  - STW_N: Inorganic nitrogen load from sewage treatment works after UWWTD secondary treatment (kg nitrate per yr).
  - SEP_N: Total nitrogen load from septic tanks (kg nitrate per yr).
  - Urban_N: Nitrogen load from urban areas (kg nitrate per yr).
  - Wood_N: Nitrogen load from woodland areas (kg nitrate per yr).
  - Bank_N: Total nitrogen from local bank erosion (kg nitrate per yr).
  - Montane_N: Nitrogen load from montane areas (kg nitrate per yr).
  - Other_N: Nitrogen load from other areas (kg nitrate per yr).

- Faecal coliform loads:
  - STW_F: Faecal coliform load from sewage treatment works (10^6 cfu per yr).
  - SEP_F: Faecal coliform load from septic tanks (10^6 cfu per yr).
  - Urban_F: Faecal coliform load from urban areas (10^6 cfu per yr).

## Publication Status and GIS Integration

- The WFD catchment dataset is not yet published by SEPA.
- The data are prepared to support GIS mapping via join to WFD catchment polygons; publication on SEPA’s Environmental data page is anticipated.

## References

- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.