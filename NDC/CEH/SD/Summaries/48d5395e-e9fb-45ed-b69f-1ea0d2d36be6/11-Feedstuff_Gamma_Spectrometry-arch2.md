# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

- Purpose: Define the data dictionary for the 11-Feedstuff_Gamma_Spectrometry.csv dataset to enable consistent monitoring of environmental radioactivity in feedstuffs and support scrutiny of health and policy performance over time.
- Context for analysts: Supports standardized data capture, quality assurance, and interoperability with portals and dashboards used in environmental monitoring.

## Dataset structure and key fields

- Sample metadata
  - Sample_Code: Unique sample identifier.
  - Sample_Type: General description of the sample (feedstuff group).
  - Location: Location where the sample was collected.
  - Sample_Description: Part of the organism analysed (e.g., whole organism, specific tissue).
  - Collection_Date: Date of sample collection (format dd-mm-yyyy).
  - Sample_size: Amount analyzed (kg fresh mass).
- Radionuclide activity concentrations (all on a dry mass basis, Bq/kg_dm)
  - Ra-226_Bq/kg_dm
  - Unc_Ra-226_Bq/kg_dm (uncertainty)
  - Detection_Limit_Ra-226_Bq/kg_dm (detection limit per ISO 11929)
  - Cs-137_Bq/kg_dm
  - Unc_Cs-137_Bq/kg_dm
  - Detection_Limit_Cs-137_Bq/kg_dm
  - Ra-228_Bq/kg_dm
  - Unc_Ra-228_Bq/kg_dm
  - Detection_Limit_Ra-228_Bq/kg_dm
  - K-40_Bq/kg_dm
  - Unc_K-40_Bq/kg_dm
  - Detection_Limit_K-40_Bq/kg_dm

## Measurement details and interpretations

- Units
  - Activity concentrations: Bq/kg dry mass (Bq/kg_dm)
  - Sample size: kg fresh mass
- Equilibrium notes
  - Ra-226 is in equilibrium with Pb-214 and Bi-214.
  - Ra-228 is in equilibrium with Ac-228.
- Handling non-detects
  - When a concentration is blank, it indicates the activity concentration is below the detection limit.
- Detection limits
  - Calculated according to ISO 11929 for Ra-226, Cs-137, Ra-228, and K-40.

## Data quality, standards, and accessibility

- The document emphasizes standardized data formats and clear metadata to support trustworthy, comparable outputs over time.
- Results and associated uncertainties are documented per radionuclide to enable traceability and quality assurance.
- Encourages storage and upload of created datasets to appropriate data portals for broader access by monitoring actors.

## Practical considerations for analysts

- Ensure consistent treatment of non-detects (blank vs. detection-limit values) in analyses and reporting.
- Use the defined metadata fields to enable cross-site comparisons and longitudinal environmental health assessments.
- Leverage the ISO-based detection limits and equilibrium notes to interpret results within the context of radiological monitoring.