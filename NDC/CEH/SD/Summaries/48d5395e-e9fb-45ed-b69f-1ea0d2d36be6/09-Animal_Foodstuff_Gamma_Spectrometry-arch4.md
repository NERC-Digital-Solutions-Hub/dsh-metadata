# Supporting documentation for 09-Animal_Foodstuff_Gamma_Spectrometry.csv

## Overview
- Provides a data dictionary for a gamma spectrometry dataset on animal-derived foodstuff.
- Documents activity concentrations of specific radionuclides in fresh mass basis, including uncertainties and detection limits.
- Notes measurement context, such as equilibrium with decay products and ISO 11929-based detection limits.

## Data schema and key fields
- Sample_Code: unique sample identifier.
- Sample_Type: general description of the sample (foodstuff group).
- Location: location where the sample was collected.
- Collection_Date: date of collection (format dd-mm-yyyy).
- Sample_Description: part of the organism analysed (e.g., tissue or whole organism portion).
- Sample_size: amount analyzed (kg fresh matter or L for milk).
- For radionuclides measured:
  - Ra-226_Bq/kg_fm: activity concentration of Ra-226 (Bq per kg fresh mass).
  - Unc_Ra-226_Bq/kg_fm: uncertainty of Ra-226 concentration.
  - Detection_Limit_Ra-226_Bq/kg_fm: detection limit (ISO 11929 method); may be blank if below detection limit.
  - Cs-137_Bq/kg_fm: activity concentration of Cs-137.
  - Unc_Cs-137_Bq/kg_fm: uncertainty of Cs-137 concentration.
  - Detection_Limit_Cs-137_Bq/kg_fm: detection limit (ISO 11929); may be blank if below detection limit.
  - Ra-228_Bq/kg_fm: activity concentration of Ra-228.
  - Unc_Ra-228_Bq/kg_fm: uncertainty of Ra-228 concentration.
  - Detection_Limit_Ra-228_Bq/kg_fm: detection limit (ISO 11929); may be blank if below detection limit.
  - K-40_Bq/kg_fm: activity concentration of K-40.
  - Unc_K-40_Bq/kg_fm: uncertainty of K-40 concentration.
  - Detection_Limit_K-40_Bq/kg_fm: detection limit (ISO 11929); may be blank if below detection limit.
- Notes and conventions:
  - Concentrations may be below detection limit (fields left blank in that case).
  - Equilibrium relationships noted for certain isotopes (e.g., Pb-214/Bi-214 with Ra-226; Ac-228 with Ra-228).
  - Units specified as Bq per kg fresh mass (or Bq per kg_fm); for milk, sometimes Bq per L.
  - Some field names show minor typographical variations (e.g., spacing in “Bq/kg_fm” and “B q/kg_fm”).

## Measurement quality and interpretation
- Uncertainties accompany measured concentrations (Unc_ fields).
- Detection limits calculated according to ISO 11929; fields may be blank when the concentration is below detection limit.
- Data may reflect equilibrium assumptions and decay-product relationships, affecting interpretation of activity values.

## Data governance and practical takeaways for Data Leaders
- Demonstrates the necessity of clear, machine-readable metadata to enable discoverability and reuse across partners.
- Highlights handling of non-detects (blank values) and the need to document detection limits and measurement methods explicitly.
- Emphasizes standardized units and date formats to maintain consistency across datasets.
- Underlines importance of provenance, methodological notes (ISO procedures), and equilibrium considerations for accurate downstream analysis.
- Suggests a governance approach: standardize similar fields across datasets, document data quality flags (uncertainties, DL), and maintain transparent metadata to support cross-network collaboration and analysis.