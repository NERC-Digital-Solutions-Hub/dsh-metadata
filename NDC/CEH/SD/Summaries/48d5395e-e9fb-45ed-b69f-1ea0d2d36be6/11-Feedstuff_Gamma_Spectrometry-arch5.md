# Supporting documentation for 11-Feedstuff_Gamma_Spectrometry.csv

## Overview
- Metadata documentation for a gamma spectrometry dataset on feedstuff samples.
- Each entry describes a sample's identity, context, and measured radioisotope activities.

## Data fields and units
- Sample_Code: Unique sample identifier.
- Sample_Type: General description of sample (e.g., feedstuff group).
- Location: Site where the sample was collected.
- Sample_Description: Part of the organism analyzed (e.g., tissue portion).
- Collection_Date: Date of collection (format: dd-mm-yyyy).
- Sample_size: Amount analyzed (units: kg fresh mass).
- Radionuclide activity concentrations (per dry mass basis, Bq/kg_dm):
  - Ra-226_Bq/kg_dm (and Unc_Ra-226_Bq/kg_dm, with notes on equilibrium; detection limit available as Detection_Limit_Ra-226_Bq/kg_dm)
  - Cs-137_Bq/kg_dm (and Unc_Cs-137_Bq/kg_dm; Detection_Limit_Cs-137_Bq/kg_dm)
  - Ra-228_Bq/kg_dm (and Unc_Ra-228_Bq/kg_dm; Detection_Limit_Ra-228_Bq/kg_dm)
  - K-40_Bq/kg_dm (and Unc_K-40_Bq/kg_dm; Detection_Limit_K-40_Bq/kg_dm)
- Notes on each radionuclide:
  - Equilibrium statements (e.g., Ra-226 in equilibrium with Pb-214 and Bi-214; Ra-228 in equilibrium with Ac-228).
  - Blank entries indicate concentration below detection limit.
  - Some fields include subfields (e.g., 1 = ..., 2 = ..., 3 = ...) to denote specific components of uncertainty or detection limit metadata.
- Detection_Limit_*: Detection limit values calculated according to ISO 11929 (per radionuclide).

## Data quality and interpretation
- Data quality indicators:
  - Clear definitions of units (Bq/kg_dm for activity on a dry-mass basis; Sample_size in kg fresh mass).
  - Explicit uncertainties (Unc_* fields) accompanying activity concentrations.
  - Detection limits documented per ISO 11929; blanks indicate below-detection values.
- Provenance and context:
  - Location and Collection_Date establish sampling context.
  - Sample_Description clarifies which part of the organism was analyzed.
- Consistency considerations for shareable datasets:
  - Standardize naming conventions and units across isotopes.
  - Ensure ISO 11929-based detection limits are consistently applied and documented.
  - Align missing values with a defined representation (e.g., blank vs. explicit below-detection indicators).

## Metadata and governance considerations for Data Stewards
- Metadata completeness:
  - Ensure Explanation, Units, and Notes are present for all fields.
  - Maintain clear interpretation guidance for equilibrium notes and below-detection values.
- Standardization and interoperability:
  - Use consistent date format (dd-mm-yyyy) and unit terminology (Bq/kg_dm, kg fresh mass).
  - Document calculation methods for detection limits (ISO 11929) and any assumptions about equilibrium.
- Data provenance and lifecycle:
  - Record dataset versioning and data source lineage.
  - Clarify any embargo periods or access restrictions.
  - Provide guidelines for updates and reprocessing (e.g., when new measurements or recalibrations occur).
- Challenge readiness:
  - Manage multiple systems/formats and large datasets by adopting a common schema and clear metadata descriptors.
  - Address incomplete user needs by capturing sufficient metadata to enable discoverability and reuse.