# Supporting documentation for 17-Transfer_Parameter_Vegetal_Stable.csv

## Overview
- Documentation for the CSV 17-Transfer_Parameter_Vegetal_Stable.csv.
- Contains sample metadata and transfer factor (Fv) values for stable elements across plant samples.
- Fields cover sample identification, description, collection date, location, and per-element Fv data with uncertainties and detection limits.
- Elements included include Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th, with various unit specifications.

## Data fields and structure
- Core sample metadata
  - Sample_Code: unique sample identifier.
  - Sample_Type: general description of the sample (e.g., foodstuff group).
  - Location: name of the collection location.
  - Sample_Description: part of the plant analysed (e.g., specific tissue).
  - Collection_Date: date of sample collection (dd-mm-yyyy).
- Per-sample transfer factor (Fv) data
  - For each element (e.g., Cs_Fv, Sr_Fv, K_Fv, Na_Fv, Ca_Fv, Mg_Fv, P_Fv, Pb_Fv, U_Fv, Th_Fv):
    - Fv value fields (e.g., Cs_Fv, Sr_Fv) with units guidance.
    - Unc_Fv fields (e.g., Unc_Cs_Fv) indicating uncertainty.
    - Detection_Limit_Fv fields (e.g., Detection_Limit_Cs_Fv) indicating detection limits.
    - Some elements show multiple subfields or indexed variants (e.g., P_Fv with 1/2/3 suffixes) describing different aspects or data representations (values, units, below-detection-limit handling).
- Units and notes
  - Units vary by field; some Fv fields are Unitless, others are Unitless or kg dry matter per L (e.g., olive oil and wine contexts).
  - Where blanks appear in Fv or Unc fields, they often indicate a value below the detection limit.
  - The documentation explicitly pairs each Fv value with its uncertainty and its detection limit.

## Spatial relevance for GIS use
- Location provides a string identifier for mapping; no explicit geographic coordinates included in this document.
- To create geospatial maps, locations should be joined to a geocoded locations table or shapefile containing coordinates.
- Sample metadata (Sample_Code, Collection_Date, Sample_Description) can be used as attributes to enrich GIS layers (e.g., filter by plant part, date, or collection site).

## Data quality, limitations, and caveats
- The dataset relies on consistent field naming and unit interpretation; some fields show inconsistent or truncated wording (e.g., end-of-document lines with incomplete definitions for Th_Fv and related fields).
- Missing values commonly represent measurements below detection limits; treat as censored data in analyses.
- Potential data integrity issues due to typos or misformatted fields (e.g., Detection_Limit_K_Fv lines with mixed labeling) may require cleaning before GIS integration.
- The presence of multiple subfields for certain elements (e.g., P_Fv with numbered suffixes) suggests multiple representations or measurements per sample; ensure correct mapping when linking to spatial attributes.

## Practical guidance for GIS specialists
- Prepare a geospatial workflow by:
  - Linking Location identifiers to a georeferenced dataset to obtain coordinates.
  - Parsing Collection_Date into a proper date field for temporal mapping.
  - Normalizing Fv fields to consistent units across all samples (e.g., convert all unitless values to a common scale or convert all to kg DM per L where appropriate).
  - Handling below-detection-limit values by using appropriate GIS data handling (e.g., censoring, special nulls, or flag fields).
- Visualisation ideas:
  - Thematic maps of Fv values by location for each element (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th).
  - Maps highlighting uncertainties (Unc_Fv fields) as a secondary theme or via symbology.
  - Spatial-temporal analyses by combining Collection_Date with Fv values.
- Data cleaning priorities:
  - Resolve inconsistent field names and complete any truncated explanations.
  - Validate that all Location entries can be accurately geocoded.
  - Ensure consistent unit interpretation across all Fv-related fields.

## Endnotes
- The documentation provides a comprehensive schema for transfer factor values but ends with incomplete lines, indicating potential missing definitions for some fields (notably Th_Fv-related entries). This should be reviewed during data preparation to avoid misinterpretation.