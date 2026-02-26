# TREE_Northumbria_Gamma_Deer

- Overview
  - A dataset capturing radiochemical measurements of Cs-137 in Roe deer tissue, including sample identifiers, sampling site, mass, date, and activity concentrations (both fresh mass and dry mass).

- Core data fields and purposes
  - Latin_Species_Name: Latin name of the species.
  - CEH_Sample_description: UKCEH sample description.
  - Tissue: Tissue type analysed.
  - CEH_Sample_code: UKCEH unique sample identifier.
  - Site: Sampling site.
  - Fresh_Mass_Of_Sample_Analysed_g: Fresh mass of the sample analysed (grams).
  - Sampling_date_Used_As_Decay date: Date of sampling, used as decay date for activity calculations.
  - Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass at sampling.
  - Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in Bq per kg dry mass.
  - Cs-137 <: Indicator that a value is below a detection threshold.
  - MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity concentration in Bq per kg fresh mass.
  - Cs-137_Concentration_Ratio_FM: Cs-137 concentration ratio using fresh mass (e.g., muscle) relative to another reference (e.g., soil dry mass).
  - CR_Notes: Notes related to the concentration ratio.

- Units and explanations
  - Each field includes explicit units (e.g., g for mass, Bq/kg FM or DM for activity concentrations) and brief explanations to aid interpretation.
  - For the decay/date field, the sampling date is used as the decay date for Cs-137 activity calculations.
  - The "<" marker denotes values reported as below the minimum detectable activity (MDA).

- Data quality and metadata considerations
  - Fields have dedicated explanations, improving data discoverability and correct usage.
  - Presence of MDA and counting error supports assessment of data reliability and detection limits.
  - The use of a unique sample code and explicit site information supports traceability and reproducibility.

- Implications for data strategy and governance (Data Leaders perspective)
  - Demonstrates robust metadata practice with clear field definitions, units, and purpose, aiding discoverability and reuse.
  - Facilitates cross-site data comparisons through standardized measurements (Bq/kg FM/DM) and explicit decay/date handling.
  - Highlights the importance of documenting detection limits (MDA) and measurement uncertainty (counting error) for informed analysis and reporting.
  - Emphasizes the value of clear sample provenance (Latin name, sample description, tissue, site, sample code) to support data provenance and user trust.
  - Illustrates potential data challenges in multi-source radiochemical datasets, such as consistent interpretation of concentration ratios and handling of censored data (< values).