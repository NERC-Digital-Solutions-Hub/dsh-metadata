# Data Structure

## Overview
- Non-agricultural pollution to rivers in Scotland data are stored in two CSV files: NonAgLoadsInland_Scotland.csv (inland catchments) and NonAgLoadsCoastal_Scotland.csv (coastal catchments).

## Data schema
- Core identifiers:
  - CATCH_ID: Unique Water Framework Directive (WFD) river catchment identifier
  - INLAND_ID: SEPA ID for inland catchments
  - COASTAL_ID: SEPA ID for coastal catchments
- For each pollutant group, there are descriptive fields and units:
  - Sediment (Z): STW_Z, Urban_Z, Wood_Z, Bank_Z, Montane_Z, Other_Z
  - Phosphorus (P): STW_P, SEP_P, Urban_P, Wood_P, Bank_P, Montane_P, Other_P
  - Nitrogen (N): STW_N, SEP_N, Urban_N, Wood_N, Bank_N, Montane_N, Other_N
  - Faecal coliform (F): STW_F, SEP_F, Urban_F
- Each column pair includes:
  - Description: what the load represents (source or process)
  - Units: e.g., kg sediment per yr; kg phosphorus per yr; kg nitrate per yr; 10^6 cfu per yr

## GIS mapping and data integration
- The pollution loads can be mapped in GIS by joining the CSVs to Water Framework Directive (WFD) catchment polygons for Scotland.
- INLAND_ID and COASTAL_ID map to the corresponding catchment IDs in the WFD catchment feature class or shapefile.
- The WFD catchments dataset is not published by SEPA yet; SEPA intends to add it to its Environmental data page in the future.

## Data usage and interpretation
- Provides loads by source (STW, Urban, Wood, Bank, Montane, Other) across pollutant types (Z, P, N, F) for each catchment.
- Facilitates assessment of diffuse pollution contributions and supports creating self-serve data products (dashboards, pivot tables) when joined with catchment geography.
- Useful for informing policy/support decisions and potential data sharing or public communication.

## References
- Gooday, R., Anthony, S., Calrow, L., Harris, D. & Skirvin, D. (2016) Predicting and Understanding the Effectiveness of Measures to Mitigate Rural Diffuse Pollution. Final report for SNIFFER Project DP1, 298pp.