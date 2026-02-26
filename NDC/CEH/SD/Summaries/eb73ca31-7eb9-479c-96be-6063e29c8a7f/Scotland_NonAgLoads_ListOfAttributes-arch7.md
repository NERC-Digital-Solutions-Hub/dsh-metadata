# Data Structure

## Overview
- Non-agricultural pollution to rivers in Scotland data are stored in CSV files: NonAgLoadsInland_Scotland.csv and NonAgLoadsCoastal_Scotland.csv.
- Designed for GIS mapping by joining these CSVs to Water Framework Directive (WFD) catchment polygons for Scotland.

## Data Files and Identifiers
- Key columns:
  - INLAND_ID (NonAgLoadsInland_Scotland.csv)
  - COASTAL_ID (NonAgLoadsCoastal_Scotland.csv)
  - CATCH_ID: Unique identifier of the WFD river catchment
- The WFD catchments dataset is not published by SEPA yet; SEPA intends to add it to the Environmental data page.

## GIS Mapping and Integration
- CSVs can be joined to WFD catchment polygons to map pollution loads spatially.
- The CATCH_ID, INLAND_ID, and COASTAL_ID serve as linkage points to corresponding WFD catchment features.

## Variables and Units
- Sediment loads (Z)
  - STW_Z: Suspended solids load from sewage treatment works — kg sediment per yr
  - Urban_Z: Suspended solids load from urban areas — kg sediment per yr
  - Wood_Z: Suspended solids load from woodland areas — kg sediment per yr
  - Bank_Z: Total sediment from local bank erosion — kg sediment per yr
  - Montane_Z: Suspended solids load from montane areas — kg sediment per yr
  - Other_Z: Suspended solids load from other areas — kg sediment per yr
- Phosphorus loads (P)
  - STW_P: Orthophosphate load from sewage treatment works after Urban Wastewater Directive secondary treatment — kg phosphorus per yr
  - SEP_P: Total phosphate load from septic tanks — kg phosphorus per yr
  - Urban_P: Phosphorus load from urban areas — kg phosphorus per yr
  - Wood_P: Phosphorus load from woodland areas — kg phosphorus per yr
  - Bank_P: Total phosphorus from local bank erosion — kg phosphorus per yr
  - Montane_P: Phosphorus load from montane areas — kg phosphorus per yr
  - Other_P: Phosphorus load from other areas — kg phosphorus per yr
- Nitrogen loads (N)
  - STW_N: Inorganic nitrogen load from sewage treatment works after Urban Wastewater Directive secondary treatment — kg nitrate per yr
  - SEP_N: Total nitrogen load from septic tanks — kg nitrate per yr
  - Urban_N: Nitrogen load from urban areas — kg nitrate per yr
  - Wood_N: Nitrogen load from woodland areas — kg nitrate per yr
  - Bank_N: Total nitrogen from local bank erosion — kg nitrate per yr
  - Montane_N: Nitrogen load from montane areas — kg nitrate per yr
  - Other_N: Nitrogen load from other areas — kg nitrate per yr
- Faecal coliform loads (F)
  - STW_F: Faecal coliform load from sewage treatment works — 10^6 cfu per yr
  - SEP_F: Faecal coliform load from septic tanks — 10^6 cfu per yr
  - Urban_F: Faecal coliform load from urban areas — 10^6 cfu per yr

## Data Availability and Gaps
- WFD catchments dataset is not yet published by SEPA; planned addition to SEPA’s Environmental data page.
- Data are stored across separate inland and coastal files, requiring joins to corresponding WFD catchment identifiers for complete spatial mapping.

## Practical Notes for GIS Work
- Ensure consistent use of IDs (CATCH_ID, INLAND_ID, COASTAL_ID) when joining to catchment polygons.
- Be aware of the current absence of the official WFD catchment dataset on SEPA’s site; plan for updating joins once published.

## Reference
- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.