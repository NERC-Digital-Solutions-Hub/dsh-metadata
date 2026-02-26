# Supporting documentation for 12-Feedstuff_Stable.csv

- Purpose: Defines the structure and meaning of fields for reporting stable element concentrations in feedstuff samples, including metadata, measurement data, and detection limits to support environmental health monitoring and transparency.

- Core metadata fields
  - Sample_Code: unique sample identifier
  - Sample_Type: general description of sample (foodstuff group)
  - Location: name of the collection location
  - Sample_Description: part of the organism analysed (e.g., specific tissue or segment)
  - Collection_Date: date of sample collection (format: dd-mm-yyyy)
  - Sample_size: amount analyzed (g fresh matter)
  - Notes: fields may be blank or contain explanations; where blank often indicates below detection limit for measurements

- Measurement data fields (per element)
  - Cs_mg/kg_dm: concentration of stable Cs on a dry mass basis (mg per kg dry mass)
  - Unc_Cs_mg/kg_dm: combined uncertainty of Cs concentration (mg per kg dry mass)
  - Detection_Limit_Cs_mg/kg_dm: detection limit for Cs on a dry mass basis (mg per kg dry mass)
  - Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm: analogous for stable Sr
  - K_mg/kg_dm, Unc_K_mg/kg_dm, Detection_Limit_K_mg/kg_dm: analogous for stable K
  - Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm: analogous for stable Na
  - Ca_mg/kg_dm, Unc_Ca_Mg/kg_dm, Detection_Limit_Ca_mg/kg_dm: analogous for stable Ca
  - Mg_mg/kg_dm, Unc_Mg_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm: analogous for stable Mg
  - P_mg/kg_dm, Unc_P_mg/kg_dm, Detection_Limit_P_mg/kg_dm: analogous for stable P
  - Pb_mg/kg_dm, Unc_Pb_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm: analogous for stable Pb
  - U_mg/kg_dm, Unc_U_mg/kg_dm, Detection_Limit_U_mg/kg_dm: analogous for stable U
  - Th_mg/kg_dm, Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm: analogous for stable Th

- Interpretation rules
  - A blank value in a concentration field generally indicates that the concentration is below the stated detection limit.
  - Each concentration is accompanied by its combined uncertainty and a detection limit to support data quality assessment and risk interpretation.

- Data quality and governance considerations (as reflected by the documentation)
  - Emphasizes the need for clear metadata (sample origin, collection date, sample description) to enable traceability and comparability across datasets.
  - Highlights the importance of reporting uncertainties and detection limits alongside concentrations.
  - Notes potential inconsistencies in field naming (e.g., some variation like Unc_K_Mg/kg_dm) that should be harmonized for robust data governance and interoperability.