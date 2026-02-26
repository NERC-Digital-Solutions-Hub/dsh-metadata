# Supporting documentation for 07-Vegetal_Foodstuff_Spectrometry.csv

- Purpose and scope
  - Provides metadata and field explanations for a CSV dataset analyzing radiological content in vegetal foodstuffs.
  - Aims to support environmental health monitoring, policy scrutiny, and informing future decisions by ensuring clear data structure and traceability.

- Key data fields and structure
  - Sample identifiers and descriptions:
    - Sample_Code: unique sample identifier.
    - Sample_Type: general description of the sample (e.g., foodstuff group).
    - Location: site from which the sample was collected.
    - Sample_Description: portion of the plant analysed (e.g., part of plant).
    - Collection_Date: date of sample collection (format dd-mm-yyyy).
    - Sample_size: amount analyzed (kg fresh matter or L for olive oil and wine).
  - Radiological measurements (all on a dry mass basis unless noted):
    - Ra-226_Bq/kg_dm with Unc_Ra-226_Bq/kg_dm and Detection_Limit_Ra-226_Bq/kg_dm (where olive oil and wine use Bq/L).
    - Cs-137_Bq/kg_dm with Unc_Cs-137_Bq/kg_dm and Detection_Limit_Cs-137_Bq/kg_dm.
    - Ra-228_Bq/kg_dm with Unc_Ra-228_Bq/kg_dm and Detection_Limit_Ra-228_Bq/kg_dm (references ISO 11929 for detection limits; olive oil and wine use Bq/L).
    - K-40_Bq/kg_dm with Unc_K-40_Bq/kg_dm and Detection_Limit_K-40_Bq/kg_dm (ISO 11929 referenced where applicable; olive oil and wine use Bq/L).
  - Equilibrium notes (context for interpretation):
    - Ra-226_Bq/kg_dm assumed in equilibrium with Pb-214 and Bi-214.
    - Ra-228_Bq/kg_dm assumed in equilibrium with Ac-228.
  - Data quality indicators:
    - Where a value is blank, the concentration is below the detection limit for that measurement.

- Units and measurement standards
  - Primary unit: Bq per kg dry mass (Bq/kg_dm) for Ra-226, Cs-137, Ra-228, and K-40.
  - For olive oil and wine: measurements expressed as Bq per liter (Bq/L) where noted.
  - Detection limits calculated according to ISO 11929 (where specified).

- Data handling and interpretation
  - Uncertainties (Unc_ fields) accompany each activity concentration measurement.
  - Blank entries indicate below-detection-limit values, not necessarily zero.
  - Clear annotation of sample description and collection date facilitates traceability and reproducibility.

- Relevance to environmental monitoring frameworks
  - Provides a structured metadata template enabling consistent tracking of radiological indicators in vegetal foods.
  - Supports data quality assurance, transparent reporting, and interoperability for monitoring policy effectiveness and informing future decisions.