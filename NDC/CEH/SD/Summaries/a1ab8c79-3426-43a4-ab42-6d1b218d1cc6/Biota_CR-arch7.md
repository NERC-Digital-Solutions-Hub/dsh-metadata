# Supporting documentation for Biota_CR.csv

- Purpose
  - Documents the Biota_CR.csv dataset, which contains concentration ratios (CR) calculated as biota stable element concentration divided by soil stable element concentration.
  - Based on soil and biota data, with CR values provided on a fresh mass basis (unitless).

- Key metadata and structure
  - Sample_Code: Unique sample identifier (units: not applicable).
  - RAP: Sample type following ICRP Reference Animals and Plants (RAPs) conventions (units: not applicable).
  - Sample_Description: Additional description of the sample.
  - Collection_Date: Date of soil sample collection (format: dd month yyyy).
  - Soil_used_for_CR_Calculations: Identifies soil sample code(s) used to estimate the CR.
  - Notes: Notes on analyses or how samples were used to estimate whole-organism CR (where applicable).

- Element-wise CR fields (all unitless)
  - I-127, Li, Be, B, Na, Mg, Al, P, S, K, Ca, Ti, V, Cr, Mn, Fe, Co, Ni, Cu, Zn, As, Se, Rb, Sr, Mo, Ag, Cd, Cs, Ba, Tl, Pb, U
  - Each corresponds to the concentration ratio for the respective element on a fresh mass basis.
  - For animals, some elements represent the whole-organism CR; where blank, the value is reported as below the detection limit (see corresponding Detection_Limit_<Element>).

- Detection limits and non-detect handling
  - Detection_Limit_<Element>: Indicates the likely maximum CR value estimated using biota concentration corresponding to the quoted detection limit.
  - If the CR value column is blank, it means the concentration ratio was below the detection limit (as indicated in the adjacent detection limit column).
  - Some elements have multiple detection-limit fields (e.g., Cs, Ba, Tl) with entries such as Cs_1, Cs_2, Cs_3, etc., each representing different aspects of the detection limit or estimation context.
  - In most cases, when a detection limit column is present, it guides interpretation of non-detect CR values.

- Data interpretation and usage notes
  - CR values are presented on a fresh mass basis and are unitless.
  - The Documentation emphasizes how to interpret blanks (non-detects) and the role of detection-limit fields in estimating maximum plausible CRs.
  - The Notes field provides context on analyses or how samples contributed to estimating whole-organism CRs.

- Practical considerations for GIS specialists
  - The dataset links each CR value to a Sample_Code and RAP, enabling spatial joins with site metadata, RAP mappings, and soil data layers.
  - Ensure date formatting consistency (Collection_Date) for temporal analyses.
  - When visualizing, treat blank CR entries as non-detects and consider incorporating the corresponding Detection_Limit_<Element> values to indicate uncertainty bounds.
  - Use Soil_used_for_CR_Calculations to trace the soil reference samples used for each CR, supporting spatial data provenance and reproducibility.