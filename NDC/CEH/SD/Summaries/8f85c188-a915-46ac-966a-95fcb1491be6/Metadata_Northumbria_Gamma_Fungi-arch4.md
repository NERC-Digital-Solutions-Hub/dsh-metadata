# TREE_Northumbria_Gamma_Fungi

## Overview
- A metadata/schema description for gamma spectroscopy data of fungi collected at Northumbria, detailing sample identification, sampling site, mass, dating, and radioisotope measurements.
- Captures activity concentrations for K-40 and Cs-137 in both dry mass (DM) and fresh mass (FM), along with measurement uncertainties and minimum detectable activities (MDA).
- Includes concentration ratios comparing fungi to soil, and various notes fields for data interpretation and quality.

## Key data fields (selected)
- Latin_Species_Name: Scientific name of species (Latin).
- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample identifier.
- Site: Sampling site.
- Mass_of_Sample_analysed_g: Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as decay date.
- Fresh_Mass_Dry_Mass_Ratio: Ratio of fresh mass to dry mass.
- K-40_Bq_per_kg_DM: K-40 activity concentration in Bq per kg dry mass.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 in DM.
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity for K-40 in DM.
- K-40_<: Indicator that the K-40 value is a "less than" value for DM.
- Cs-137_Bq_per_kg_DM: Cs-137 activity concentration in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in DM.
- Cs-137_<: Indicator that the Cs-137 value is a "less than" value for DM.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity for Cs-137 in DM.
- K-40_Bq_per_kg_FM: K-40 activity concentration in Bq per kg fresh mass.
- Counting_Error_K-40_Bq_per_kg_FM: Two-sigma counting error for K-40 in FM.
- K40_<: Indicator that the K-40 value is a "less than" value for FM.
- MDA_K-40_Bq_per_kg_FM: Minimum detectable activity for K-40 in FM.
- Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq per kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_FM: Two-sigma counting error for Cs-137 in FM.
- Cs-137_<: Indicator that the Cs-137 value is a "less than" value for FM.
- MDA_Cs-137_Bq_per_kg_FM: Minimum detectable activity for Cs-137 in FM.
- Cs-137_Concentration_Ratio_Fungi_FM: Concentration ratio (Fungi FM Bq/kg divided by soil DM Bq/kg).
- Cs-137_Concentration_Ratio_Fungi_DM: Concentration ratio (Fungi DM Bq/kg divided by soil DM Bq/kg).
- CR_Notes: Concentration ratio notes.
- General_Notes: General notes.

## Measurements and units
- Mass: grams (g) for Mass_of_Sample_analysed_g.
- Activity concentrations: Bq per kg (kg_DM or kg_FM) for K-40 and Cs-137.
- Ratios: dimensionless concentration ratios for fungi to soil, expressed in FM or DM context as specified.

## Data quality and metadata
- Includes two-sigma counting errors for each activity concentration to quantify measurement uncertainty.
- Uses MDAs (Minimum Detectable Activity) to indicate detection limits.
- Some fields allow "<" markers to denote values below the MDA.
- Separate notes fields (CR_Notes, General_Notes) support contextual understanding and data governance.

## How this supports data leadership aims
- Provides a rich, metadata-dense dataset enabling discovery, evaluation, and reuse of radioisotope measurements in ecological contexts.
- Clear definitions and units support data standardization, interoperability, and cross-study comparability.
- Presence of identifiers, dating, mass, and measurement uncertainties supports traceability, data lineage, and reproducibility.
- Concentration ratios facilitate cross-scale analyses (fungus vs. soil) and potential networked data comparisons across sites.

## Considerations for data governance and implementation
- Ensure consistent interpretation of "DM" (dry mass) vs. "FM" (fresh mass) across datasets and partners.
- Manage and harmonize units, especially where "less than" markers and MDAs are used.
- Maintain clear metadata notes (CR_Notes, General_Notes) to capture context, methods, and any caveats.
- Address potential data gaps or missing values indicated by n/a in several fields.
- Facilitate discoverability by indexing key fields (sample ID, site, date, isotopes, mass type) in a data catalog.