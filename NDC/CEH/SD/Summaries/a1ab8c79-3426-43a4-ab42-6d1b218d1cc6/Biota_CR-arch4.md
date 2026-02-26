# Supporting documentation for Biota_CR.csv.

- Purpose: Defines how concentration ratios (CR) are calculated from soil and biota stable-element data. CR = biota stable element concentration / soil stable element concentration.

- Key identifiers and context:
  - Sample_Code: unique sample identifier.
  - RAP: sample type based on ICRP Reference Animals and Plants (RAPs).
  - Sample_Description: provides additional context for the sample.
  - Collection_Date: date of soil sample collection (format: dd month yyyy).
  - Soil_used_for_CR_Calculations: links to soil sample(s) used to estimate CRs.
  - Notes: notes on analyses or how samples were used to estimate whole-organism CRs.

- Data model and scope:
  - Each row corresponds to a unique sample with associated RAP, description, date, and soil context used for CR calculation.
  - CR values are provided for multiple elements (e.g., I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U, etc.).
  - All CR fields are unitless; for animals, values represent the whole-organism concentration ratio.

- Detection limits and non-detect handling:
  - For many elements, accompanying Detection_Limit_<element> fields indicate the likely maximum CR value corresponding to the quoted detection limit.
  - If the primary CR value is blank, it indicates the concentration ratio was below the detection limit and the reported value may be taken from the corresponding detection-limit field.
  - Notes explain when a concentration ratio is reported in a previous column or when the value is below the detection limit.

- Data quality and quality assurance cues:
  - Detailed metadata for each element supports transparency about measurement limits and data interpretation.
  - The presence of detection-limit fields helps quantify uncertainty and censoring in the dataset.
  - The Notes field provides context on analyses and how samples contribute to whole-organism CR estimation.

- Metadata standards and format considerations:
  - Units: most CR fields are unitless.
  - Collection_Date format specified as day-month-year with month name.
  - RAPs tied to ICRP conventions, enabling cross-dataset alignment and comparability.
  - Rich element-level metadata (including detection limits) supports data discoverability and reuse across networks.

- Provenance and traceability:
  - Sample_Code and Soil_used_for_CR_Calculations enable traceability from biota/soil measurements back to the soil samples used for CR estimation.
  - RAP classification provides a standardized sample-type context, aiding cross-study comparisons.

- Practical implications for use:
  - Enables environmental monitoring and risk assessment through standardized CR measurements across a broad suite of elements.
  - Supports downstream analyses with explicit handling of non-detects and measurement limits.
  - Facilitates collaboration and data sharing by adhering to documented data fields, units, and interpretation rules.