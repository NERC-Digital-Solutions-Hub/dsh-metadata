# TREE_Northumbria_Gamma_Soil

## Overview
- A radiochemistry dataset describing soil samples analyzed for radioactive isotopes K-40 and Cs-137, including identifiers, site, sample description, mass analysed, date used as decay date, and mass ratio data.
- Measurements are reported as activity concentrations in Bq per kg dry mass (kg_DM), with associated counting errors and minimum detectable activities (MDA). Non-detections are indicated with “<” markers.

## Data Model and Key Fields
- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken (also used as decay date).
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to freeze-dried mass.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 (Bq per kg dry mass) at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40.
- K-40_<: < marker indicating value is below MDA for K-40.
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration for K-40 (Bq per kg DM).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 (Bq per kg dry mass).
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137.
- Cs-137_<: < marker indicating value is below MDA for Cs-137.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration for Cs-137 (Bq per kg DM).

## Measurements and Quality Indicators
- Reports both measured activity concentrations and MDAs for K-40 and Cs-137.
- Non-detections are clearly flagged with “<” values tied to the corresponding MDA fields.
- Includes two-sigma counting errors to indicate measurement uncertainty.
- Units are consistently Bq per kg dry mass (kg_DM) for all activity concentrations.

## Metadata and Data Governance
- Sample identifiers and descriptions linked to UKCEH Radiochemistry Laboratory records.
- Site and sampling date data support traceability and temporal analyses.
- Mass information (sample mass, fresh-to-dry ratio) supports data normalization and quality assessments.
- Metadata clarity around what is measured, what is a non-detection (below MDA), and associated uncertainties supports data discoverability and reuse.

## Implications for Data Leaders
- Ensure consistent interpretation of measured values versus non-detections (MDA) across datasets.
- Maintain clear metadata standards for units (kg_DM), detection limits, and uncertainty (counting error).
- Support data discoverability by preserving sample identifiers, site, dates, and descriptive fields.
- Address data gaps or inconsistencies arising from non-detections when aggregating across samples or sites.
- Facilitate co-ownership and cross-dataset integration by aligning on metadata semantics (e.g., what constitutes a “Not measured” value and how MDAs are reported).