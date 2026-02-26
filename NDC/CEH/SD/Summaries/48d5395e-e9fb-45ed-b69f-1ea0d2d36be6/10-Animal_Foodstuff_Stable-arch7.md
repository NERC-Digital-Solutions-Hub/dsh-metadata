# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

## Overview
- Metadata and data dictionary for the 10-Animal_Foodstuff_Stable.csv dataset.
- Describes how samples are identified, described, collected, and chemically analysed.
- Documents concentration measurements for multiple elements (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) with associated uncertainties and detection limits.

## Key dataset structure
- Sample identifiers and descriptions:
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample group (e.g., foodstuff category).
  - Location: Name of the collection location.
  - Sample_Description: Part of the organism analysed (e.g., which tissue or component).
  - Collection_Date: Date of sample collection (format: dd-mm-yyyy).
  - Sample_size: Amount analysed (units: g fresh matter or mL for milk).
- Chemical measurements (per element):
  - Element concentrations on a fresh mass basis (e.g., Cs_mg/kg_fm, Sr_mg/kg_fm, K_mg/kg_fm, Na_mg/kg_fm, Ca_mg/kg_fm, Mg_mg/kg_fm, P_mg/kg_fm, Pb_mg/kg_fm, U_mg/kg_fm, Th_mg/kg_fm).
  - Uncertainty fields (e.g., Unc_Cs_mg/kg_fm, Unc_Sr_mg/kg_fm, etc.).
  - Detection_limit fields (e.g., Detection_Limit_Cs_mg/kg_fm, Detection_Limit_Sr_mg/kg_fm, etc.).
  - Units notes indicate mg per kg fresh mass or mg per litre for milk as applicable.
- Data notes:
  - Where concentration or uncertainty fields are blank, the value is below the detection limit.
  - Detection limits are provided per element; some field names show variations (e.g., Unc_K_Mg/kg_fm vs Unc_K_mg/kg_fm), which may require harmonisation.

## Measurements and units
- Elements covered: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th.
- Concentration units: mg/kg_fm (milligrams per kilogram of fresh mass) or mg/L for milk where applicable.
- Sample size units: g fresh matter or mL for milk.
- Uncertainty and detection-limit fields accompany each element’s concentration.

## Data quality and conventions
- Dates conform to a dd-mm-yyyy format.
- Blank values for concentrations or uncertainties imply measurements below the detection limit.
- Detection limits are provided for each element to aid interpretation of non-detects.
- Some field names show inconsistent naming conventions (e.g., Unc_K_Mg/kg_fm vs Unc_K_mg/kg_fm) which may require data cleaning/standardisation before GIS use.

## GIS-ready considerations
- Spatial aspect:
  - Location provides a location name suitable for geocoding or joining to a spatial database; precise coordinates are not included in this documentation and may need to be derived.
  - Sample_Code can be used as a key to join chemical measurements to spatial attributes.
- Mapping opportunities:
  - Use element concentrations (and detection-limit-aware values) to create choropleth or point-based maps by location.
  - Combine with collection dates for time-series or trend maps if multiple samples exist per location.
- Data processing notes for GIS workflows:
  - Geocode Location names to obtain coordinates for map display.
  - Handle below-detection-limit values appropriately (e.g., substitute with half the detection limit, or use NaN, depending on analysis needs).
  - Harmonise field names (especially uncertainty and detection-limit fields) to ensure consistent attribute schemas across the dataset.
  - Validate date formats and ensure Sample_Code links align between metadata and measurements.

## Practical usage summary
- This document provides the essential metadata and field definitions needed to load 10-Animal_Foodstuff_Stable.csv into GIS workflows.
- Enables spatial analysis of trace element concentrations in animal-derived foodstuffs, with clear guidance on units, detection limits, and data interpretation.
- Important to standardise field naming and geocode location data before integrating into map-based data products for policy, client, or public-facing visualisations.