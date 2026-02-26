# Supporting documentation for 05-Soil_Stable.csv

- Overview
  - A data dictionary accompanying the soil stable element concentration dataset (05-Soil_Stable.csv), detailing sample metadata, measured element concentrations, and associated quality metadata (uncertainties and detection limits).

- Data Model: Key Fields
  - Sample metadata
    - Sample_Code: unique sample identifier.
    - Sample_Type: "Soil".
    - Location: name of the collection site.
    - Sample_Description: extra detail; for this dataset, soil collected at depth 0-10 cm.
    - Collection_Date: date of sample collection (dd-mm-yyyy).
    - Sample_size_g_dm: amount of sample analyzed (g dry matter).
  - Element concentration measurements (for each element, values are on a dry matter basis and reported in mg/kg_dm)
    - Cs_mg/kg_dm, Sr_mg/kg_dm, K_mg/kg_dm, Na_mg/kg_dm, Ca_mg/kg_dm, Mg_mg/kg_dm, P_mg/kg_dm, Pb_mg/kg_dm, U_mg/kg_dm, Th_mg/kg_dm
    - Unc_*: combined uncertainty for the corresponding element concentration (e.g., Unc_Cs_mg/kg_dm)
    - Detection_Limit_*: detection limit for the corresponding element (e.g., Detection_Limit_Cs_mg/kg_dm)
  - Notes and variations
    - Some fields indicate concentration is below the detection limit when blank (e.g., "Where blank, then concentration was below the detection limit").
    - Some elements have slightly different field naming or formatting, e.g., Ca_mg/kg_dm, on a dry matter basis, with explanatory notes; similarly for Mg_mg/kg_dm and others.

- Data Content and Scope
  - Description: topsoil samples (0–10 cm depth) with measured concentrations of select stable elements.
  - Elements included: Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th.
  - Data types and units: concentrations and uncertainties in mg/kg_dry_mass; detection limits provided per element.
  - Data completeness: presence of non-detects indicated via blanks or explicit notes; some fields may be incomplete or require inference from detection limits.

- Data Quality and Metadata Considerations
  - Detection limits accompany each concentration measurement, allowing proper handling of non-detects.
  - Uncertainty fields accompany concentration values, enabling uncertainty propagation in analyses.
  - Metadata ensures traceability of samples (Code, Location, Collection Date, Description) and the analytical context (dry matter basis, sample size).

- Relevance to Monitoring Frameworks
  - Provides a structured, standards-oriented data dictionary to support environmental health monitoring and policy evaluation.
  - Facilitates data governance by explicitly documenting measurement metadata, uncertainties, and detection limits.
  - Highlights data quality considerations and potential gaps (non-detects, missing fields, formatting inconsistencies) relevant for planning and decision making.

- Practical Implementation Considerations
  - Maintain consistency in units (mg/kg_dm) and field naming across all elements.
  - Record non-detects clearly (either as blanks with corresponding Detection_Limit fields or explicit non-detect indicators).
  - Ensure Collection_Date formatting is uniform (dd-mm-yyyy) and that Sample_Description consistently notes depth.
  - Align data handling with governance practices to support transparency and reuse of underlying data.