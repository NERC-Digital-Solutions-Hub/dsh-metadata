# TREE_Northumbria_Gamma_Soil

## Overview
- Dataset documenting soil gamma spectrometry measurements (K-40 and Cs-137) in Bq per kg of dry mass (kg DM).
- Managed by UKCEH Radiochemistry Laboratory; includes sample metadata, site information, and measurement details.
- Data used to assess radioisotope concentrations in soil and support data discovery and reuse.

## Key Metadata Fields
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken (also used as decay date).
- Fresh_Mass_Dry_Mass_Ratio: Fresh mass to freeze-dry mass ratio of soil.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 (Bq/kg DM) at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 (Bq/kg DM).
- K-40_<: Less-than marker indicating the value in MDA_K-40_Bq_per_kg_DM is a "<" value.
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration for K-40 (Bq/kg DM).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 (Bq/kg DM).
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 (Bq/kg DM).
- Cs-137_<: Less-than marker indicating the value in MDA_Cs-137_Bq_per_kg_DM is a "<" value.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration for Cs-137 (Bq/kg DM).

## Measurements, Units, and Detection Limits
- Units: Bq per kg of dry mass (Bq/kg DM) for both K-40 and Cs-137.
- Includes: measured activity, two-sigma counting error, and minimum detectable activity (MDA) for each isotope.
- Flags: Not measured entries (below MDA) and "<" indicators for <MDA values.

## Sample and Site Details
- Site information included to locate samples.
- Mass of sample analysed provided to assess data representativeness.
- Sampling date used as decay date to align with radiometric timing.
- Fresh-to-dry mass ratio provided for sample characterization and recalculations if needed.

## Data Quality and Flags
- Not measured flags indicate concentrations below detection limits.
- "<" markers denote values reported as upper bounds (below MDA).
- Counting errors (two-sigma) accompany activity concentrations to convey uncertainty.

## Governance and Stewardship Considerations
- Ensure consistent units (Bq/kg DM) and standardized field names across datasets.
- Maintain complete metadata to enable discovery, understanding, and reuse.
- Capture and document the source (UKCEH Radiochemistry Laboratory) and any data processing steps.
- Clearly record detection limits (MDA) and related flags to support proper interpretation.
- Manage data sharing constraints and embargoes if applicable; document any access restrictions.

## Action Items for Data Stewards
- Validate and harmonize sample identifiers and descriptions with the dataset catalog.
- Confirm site names, sample masses, and decay-date applicability.
- Ensure MDA fields and counting errors are present and correctly linked to their respective isotopes.
- Verify proper handling of Not Measured and "<" indicators in downstream portals and analyses.
- Prepare and upload the dataset to relevant data portals with clear metadata and provenance.