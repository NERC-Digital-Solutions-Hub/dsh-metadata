# Supporting documentation for 10-Animal_Foodstuff_Stable.csv

- Purpose and scope
  - Provides metadata and field definitions for the 10-Animal_Foodstuff_Stable.csv dataset.
  - Documents how stable element concentrations (and related quality metrics) are captured for animal-derived foodstuffs.
  - Supports consistent data recording to aid environmental health monitoring and policy performance analysis over time.

- Core data structure
  - Sample identifiers and context
    - Sample_Code: unique sample identifier (no units).
    - Sample_Type: general description of the sample (foodstuff group).
    - Location: name of the collection site.
    - Sample_Description: part of the organism analyzed (e.g., tissue or product portion).
    - Collection_Date: date of sample collection (dd-mm-yyyy).
    - Sample_size: amount analyzed (g fresh matter or mL for milk).
  - Analytical outputs (concentration data)
    - Cs_mg/kg_fm, Sr_mg/kg_fm, K_mg/kg_fm, Na_mg/kg_fm, Ca_mg/kg_fm, Mg_mg/kg_fm, P_mg/kg_fm, Pb_mg/kg_fm, U_mg/kg_fm, Th_mg/kg_fm
    - Units are mg per kg fresh mass (fm) or mg per litre for milk (as specified).
    - For Na, the data can be reported as mg/kg_fm or mg/L for milk.
  - Uncertainty and detection limits
    - Unc_<element>_mg/kg_fm: combined uncertainty of the element concentration on a fresh mass basis.
    - Detection_Limit_<element>_mg/kg_fm: detection limit of the element on a fresh mass basis (or milk basis when applicable).
    - Notes indicate: if a field is blank, the concentration is below the detection limit.
  - Data quality notes
    - The documentation explicitly notes how to interpret undetected values (below detection limit) and how uncertainties and limits are reported.
    - For several fields, multiple descriptors (e.g., Na_mg/kg_fm, 1/2/3) indicate the structure of the accompanying metadata (concentration, units, and detection-limit handling).

- What is captured for each analyte
  - Stable Cs, Sr, K, Na, Ca, Mg, P, Pb, U, and Th concentrations.
  - For each, the accompanying uncertainty (Unc_*) and detection limit (Detection_Limit_*) fields are provided to support data quality assessment and comparability over time.
  - Some entries use alternative reporting (e.g., Na in mg/L for milk) to accommodate sample type.

- Data use implications for Analysts Monitoring the Environment
  - Enables standardized reporting and cross-sample comparisons across time and sites.
  - Supports data cleaning, verification, and transformation by documenting exact meanings, units, and handling of non-detects.
  - Facilitates integration with other datasets by clearly defining metadata and measurement context.
  - Aligns with the aim of demonstrating environmental health and policy performance through repeatable, quality-assured data outputs (e.g., reports, maps, charts).

- Practical considerations and guidance
  - When concentration fields are blank, treat as below detection limit according to the notes.
  - Uncertainty fields provide a quantitative measure of measurement confidence alongside the reported concentrations.
  - Awareness of unit variations for Na (fm vs. milk) is essential for correct aggregations and comparisons.
  - The documentation supports storing and sharing the dataset via appropriate data portals, in line with standard monitoring practice.