# TREE_Northumbria_Gamma_Water

## Overview
- A radiochemical dataset from UKCEH Northumbria, detailing gamma-emitting analytes (K-40 and Cs-137) in water samples.
- Captures sample identity, description, site, sample mass, and decay-date usage, along with activity concentrations, uncertainties, and detection limits.

## Key metadata fields
- CEH_Sample_Identifier: UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of sample (grams).
- Sampling_Date_Used_As_Decay_Date: Date sample was taken and used as decay date.
- K-40_Bq_per_kg_FM: Activity concentration of K-40 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_FM: Two sigma counting error for K-40 in Bq per kg fresh mass.
- K-40_<: Indicator that the corresponding K-40 value is a "<" (less-than) value, tied to MDA_K-40_Bq_per_kg_FM.
- MDA_K-40_Bq_per_kg_FM: Minimum Detectable Activity for K-40 in Bq per kg fresh mass.
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two sigma counting error for Cs-137 in Bq per kg fresh mass.
- Cs-137_<: Indicator that the corresponding Cs-137 value is a "<" (less-than) value, tied to MDA_Cs-137_Bq_per_kg_FM.
- MDA_Cs-137_Bq_per_kg_FM: Minimum Detectable Activity for Cs-137 in Bq per kg fresh mass.
- General_Notes: General notes.

## Data quality and provenance
- Provisions for both measured activities and associated uncertainties (counting errors) alongside detection limits.
- Uses clear units (Bq per kg fresh mass for activity, grams for mass).
- Sample provenance and description are recorded, enabling traceability from sampling to results.
- Presence of < indicators and MDAs ensures proper interpretation of non-detect results.

## Data sharing and governance considerations
- Metadata includes essential identifiers and descriptions to support discovery and reuse.
- Standardized field naming and units facilitate interoperability across portals and datasets.
- Ensure consistent handling of < values and MDAs during data ingestion and downstream analyses.
- Maintain linkage between sample identifiers, site information, and date of sampling/decay reference for longitudinal or comparative studies.

## Recommendations for data stewards
- Validate completeness of core fields (identifier, description, site, mass, date, K-40 and Cs-137 data, MDAs, and counts).
- Enforce unit consistency (Bq/kg_FM, g, date formats) and document any unit conversions if needed.
- Capture and preserve provenance: origin as UKCEH radiochemistry data, date used as decay date, and any metadata in General_Notes.
- Apply controlled vocabularies for Site where possible to improve searchability.
- Clearly flag and document < values and corresponding MDA fields to avoid misinterpretation.
- Consider publishing this dataset with a clear data dictionary and data quality notes to aid discoverability by researchers and other data stewards.