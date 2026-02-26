# Supporting documentation for 05-Soil_Stable.csv

## Overview
- Provides a data dictionary for a CSV of soil stable element concentrations (0–10 cm depth).
- Designed to support GIS mapping and analysis by clarifying field names, units, and data quality indicators.
- Emphasizes linking sample metadata (location, collection date, sample size) with concentration measurements to enable map-based visualisations.

## Data structure and key fields
- Sample identifiers and metadata
  - Sample_Code: unique sample identifier.
  - Location: name of where the sample was collected (used for geocoding in GIS).
  - Sample_Type: “Soil”.
  - Sample_Description: further details (e.g., depth 0–10 cm).
  - Collection_Date: date of collection (format: dd-mm-yyyy).
  - Sample_size_g_dm: amount of sample analysed, in grams of dry matter.
- Element concentration fields (all on a dry mass basis, mg/kg_dm)
  - Cs_mg/kg_dm; Sr_mg/kg_dm; K_mg/kg_dm; Na_mg/kg_dm; Ca_mg/kg_dm; Mg_mg/kg_dm; P_mg/kg_dm; Pb_mg/kg_dm; U_mg/kg_dm; Th_mg/kg_dm (note: Th has multi-entry indexing in the dictionary).
- Uncertainty and detection limit fields
  - Unc_<element>_mg/kg_dm: combined measurement uncertainty for the element.
  - Detection_Limit_<element>_mg/kg_dm: detection limit for the element.
  - For any <element> where the field is blank, the concentration is below the detection limit.
- Special formatting for Th
  - Th_mg/kg_dm, 1/2/3 and corresponding Unc_Th_mg/kg_dm, 1/2/3 and Detection_Limit_Th_mg/kg_dm indicate multiple measurement contexts or replicates.

## Units and basis
- Concentrations: milligrams per kilogram of dry mass (mg/kg_dm).
- Sample size: grams dry matter (g_dm).
- Collection dates: day-month-year (dd-mm-yyyy).

## Data quality indicators and handling
- Blank concentration fields indicate concentrations below the detection limit for that element.
- Unc_<element> fields provide the combined uncertainty; blanks imply no quantified uncertainty reported.
- For Th, multiple entries suggest distinct measurement contexts or replicates that should be interpreted accordingly during analysis.

## How this supports GIS workflows
- Sample_Code serves as a unique key to join with spatial data; Location enables geocoding for mapping.
- Depth context from Sample_Description helps differentiate surface vs. other layers if expanded in GIS analyses.
- Element concentration maps (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) can be visualised as choropleth or point data over space, with uncertainty and detection-limit flags informing reliability and data cleaning.
- Consistent dry-mass basis units facilitate comparability across samples and integration with other geo-referenced datasets.

## Considerations for data preparation and analysis
- When exporting to GIS, ensure consistent geocoding of Location to spatial coordinates.
- Treat blank concentration fields as "< Detection limit" in analyses that require numeric values.
- Incorporate Unc_<element> as error bars or uncertainty surfaces where relevant.
- Be mindful of Th’s multi-entry format (1/2/3) to avoid misinterpretation of replicates or contexts.

## Summary of covered elements
- Elements measured: Cesium (Cs), Strontium (Sr), Potassium (K), Sodium (Na), Calcium (Ca), Magnesium (Mg), Phosphorus (P), Lead (Pb), Uranium (U), Thorium (Th).