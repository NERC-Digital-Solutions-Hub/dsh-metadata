# TREE_Northumbria_Gamma_Vegetation

## Purpose and scope
- Data dictionary / schema for a vegetation gamma-activity dataset from Northumbria.
- Captures species, site, sample identifiers, and descriptive metadata.
- Records activity concentrations for K-40 and Cs-137 in dry mass (DM) and fresh mass (FM), with associated uncertainties and detection limits.
- Includes concentration ratios comparing vegetation to soil, and notes on interpretation.

## Key data fields and units
- Latin_Species_Name, Common_Species_Name: taxonomic names; human-readable common names.
- Plant_Part_Analysed: plant part analysed.
- Site: sampling location.
- CEH_Sample_Identifier: UKCEH radiochemistry lab unique sample identifier.
- CEH_Sample_Description: description of the UKCEH sample.
- Sampling_Date_Used_As_Decay_Date: date used as decay date (for activity decay considerations).
- Dry_Mass_Of_Sample_Analysed_g: dry mass of sample (grams).

- K-40_Bq_per_kg_DM: potassium-40 activity concentration in Bq per kg dry mass.
- Counting_Error_K-40_Bq_per_kg_DM: two-sigma counting error for K-40 in Bq per kg dry mass.
- K-40_<: indicator used when value is below a threshold.
- MDA_K-40_Bq_per_kg_DM: minimum detectable activity for K-40 in Bq per kg dry mass.

- K-40_Bq_per_kg_FM: potassium-40 activity concentration in Bq per kg fresh mass.
- Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting error for K-40 in Bq per kg fresh mass.
- K-40_FM_<: below-detection indicator for fresh mass measurement.
- MDA_K-40_Bq_per_kg_FM: MDA for K-40 in Bq per kg fresh mass.

- Cs-137_Bq_per_kg_DM: Cs-137 activity concentration in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: two-sigma counting error for Cs-137 in Bq per kg dry mass.
- Cs-137_DM_<: below-detection indicator for dry mass.
- MDA_Cs-137_Bq_per_kg_DM: MDA for Cs-137 in Bq per kg dry mass.

- Cs-137_Bq_per_kg_FM: Cs-137 activity concentration in Bq per kg fresh mass.
- Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting error for Cs-137 in Bq per kg fresh mass.
- Cs-137_FM_<: below-detection indicator for fresh mass.
- MDA_Cs-137_Bq_per_kg_FM: MDA for Cs-137 in Bq per kg fresh mass.

- Cs-137_Concentration_Ratio_DM_<: Cs-137 concentration ratio (vegetation vs soil) on a dry-mass basis; below-detection indicator.
- Cs-137_Concentration_Ratio_DM: Cs-137 concentration ratio (dry mass) vegetation/soil.
- Cs-137_Concentration_Ratio_FM_<: concentration ratio on a fresh-mass basis; below-detection indicator.
- Cs-137_Concentration_Ratio_FM: concentration ratio (fresh mass) vegetation/soil.
- Notes_Related_to_137Cs_Concentration_Ratio: numeric notes clarifying Cs-137 concentration ratio details.

- General_Notes: general metadata notes.

## Data quality and interpretation notes
- Below-detection values are indicated with a "<" marker in corresponding MDA fields.
- Some fields use "n/a" or have placeholder explanations; notes provide context for Cs-137 concentration ratios.
- Data capture spans both dry-mass and fresh-mass contexts, enabling multiple normalization schemes.
- Concentration ratios compare vegetation to soil, enabling assessment of transfer factors for Cs-137.

## Practical usage and workflow considerations
- Use CEH_Sample_Identifier and CEH_Sample_Description to trace laboratory processing and decays.
- Align Sampling_Date_Used_As_Decay_Date with decay calculations for accurate activity comparisons.
- Validate mass measurements (Dry_Mass_Of_Sample_Analysed_g) before calculating or interpreting DM and FM activity values.
- Handle MDA and "<" indicators properly when aggregating summaries or performing statistical analyses.
- Leverage Concentration_Ratio fields to assess uptake of Cs-137 by vegetation relative to soil, with clear documentation from Notes_Related_to_137Cs_Concentration_Ratio.