# Radionuclide meta-data

## Overview
- Defines the structured radionuclide meta-data collected by the CEH Radiochemistry laboratory for samples (plant species or soil).
- Each field includes a description and, where applicable, the required units to support data interpretation, comparability, and traceability.

## Key Fields and Definitions
- Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
- Sampling_Site: Location where the sample was collected.
- Sampling_date: Date when the plant species or soil was sampled.
- Species: Latin name of the plant species (n/a for soil samples).
- Common_name: Common name of the plant species (or soil description) when available.
- Order, Family, Genus: Taxonomic classification (n/a for soil samples).
- Mass_of_sample_g: Mass of the dry-weight soil or plant sample (grams).
- Analysed_date: Date the sample was analyzed (dd/mm/yyyy).
- Analysis_time_days: Number of days the sample was analyzed for gamma-emitting radionuclides.
- Activity_concentration_40K_Bq_kg_dry: Measured K-40 activity concentration (Bq per kg dry weight).
- Counting_error_40K_Bq_kg_dry: Counting error for the K-40 activity concentration.
- 40K_<: Indicator that the K-40 concentration was below the limit of detection (LOD) (present when applicable).
- MDA_40K_Bq_kg_dry: Minimum detectable activity (MDA) for K-40 (Bq per kg dry weight).
- Activity_concentration_1 37Cs_Bq_kg_dry: Measured Cs-137 activity concentration (Bq per kg dry weight).
- Counting_error_137Cs_Bq_kg_dry: Counting error for Cs-137 activity concentration.
- 137Cs_<: Indicator that Cs-137 concentration was below the LOD (presence denotes below-LOD value).
- MDA_137Cs_Bq_kg_dry: Minimum detectable activity (MDA) for Cs-137 (Bq per kg dry weight).
- 7Be_<: Indicator that Be-7 concentration was below the LOD (presence denotes below-LOD value).
- MDA_7Be_Bq_kg_dry: Minimum detectable activity (MDA) for Be-7 (Bq per kg dry weight).
- Notes: Information related to the sample that may impact results (or not applicable if irrelevant).

## Units and Data Types
- Mass_of_sample_g: gram (g)
- Analysed_date: date format (dd/mm/yyyy)
- Activity concentrations (e.g., 40K_Bq_kg_dry, 137Cs_Bq_kg_dry, etc.): Bq per kg dry weight
- MDA fields: Bq per kg dry weight
- Many fields are designated as not applicable (n/a) where not relevant (e.g., taxonomic fields for soil)

## Detection Limits and Quality Indicators
- 40K_<, 137Cs_<, 7Be_< provide flags indicating concentrations below the limit of detection (LOD).
- MDA fields specify the minimum detectable activity for each radionuclide, aiding interpretation of non-detects.
- Notes field may flag sample-specific considerations that affect results.

## Data Use and Governance Implications
- This metadata schema supports traceability from sample collection to analytical results.
- Clear definitions and units facilitate data sharing, comparison, and quality assurance across monitoring and reporting activities.
- The presence of LOD/MDA indicators and notes helps stakeholders assess data reliability and any caveats in interpretation.