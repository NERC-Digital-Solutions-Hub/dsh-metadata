# TREE_Northumbria_Gamma_Vegetation

- Purpose and scope
  - A dataset capturing gamma-emitting radionuclide concentrations in vegetation, focusing on potassium-40 (K-40) and cesium-137 (Cs-137).
  - Includes activity concentrations in both dry mass (DM) and fresh mass (FM), with associated uncertainties and detection limits.
  - Records for each sample include taxonomic details, sampling site, sample identifiers from UKCEH, and the date used for decay calculations.

- Data structure and key fields
  - Taxonomy and plant context
    - Latin_Species_Name, Common_Species_Name
    - Plant_Part_Analysed
  - Sampling and site metadata
    - Site, CEH_Sample_Identifier, CEH_Sample_Description
    - Sampling_Date_Used_As_Decay_Date
  - Sample mass
    - Dry_Mass_Of_Sample_Analysed_g
  - Radionuclide concentrations (per mass)
    - K-40 in DM and FM (Bq/kg_DM and Bq/kg_FM)
    - Cs-137 in DM and FM (Bq/kg_DM and Bq/kg_FM)
  - Uncertainties and detection limits
    - Counting_Error_K-40_Bq_per_kg_DM
    - Counting_Error_K-40_Bq_per_kg_FM
    - Counting_Error_Cs-137_Bq_per_kg_DM
    - Counting_Error_Cs-137_Bq_per_kg_FM
    - MDA_K-40_Bq_per_kg_DM
    - MDA_K-40_Bq_per_kg_FM
    - MDA_Cs-137_Bq_per_kg_DM
    - MDA_Cs-137_Bq_per_kg_FM
    - Several fields may use "<" to indicate values below the minimum detectable activity (MDA)
  - Concentration ratios (derived metric)
    - Cs-137_Concentration_Ratio_DM (ratio of vegetation to soil, dry mass basis)
    - Cs-137_Concentration_Ratio_FM (ratio of vegetation to soil, fresh mass basis)
    - Related notes for interpretation and applicability
  - Notes and general guidance
    - Notes_Related_to_137Cs_Concentration_Ratio
    - General_Notes

- Data interpretation highlights
  - Cs-137 concentration ratios compare vegetation to soil on both DM and FM bases.
  - Presence of “<” values indicates measurements below the detectable limit (MDA) for the corresponding concentration.
  - Two-sigma counting errors accompany reported activity concentrations to aid uncertainty assessment.
  - Decay-date consideration is explicitly linked to Sampling_Date_Used_As_Decay_Date, enabling decay-corrected analyses.
  - Data provenance includes UKCEH laboratory sample identifiers and descriptive CEH sample descriptions for traceability.

- Practical considerations for analysts
  - Ensure consistent mass basis when comparing DM vs FM values (and when computing ratios).
  - Treat MDA and "<" indicators as censoring points in statistical analyses; consider survival/ Tobit models if appropriate.
  - Be aware of potential data gaps or missing fields, especially for some samples where certain measurements or notes are not available.
  - Use the Notes_Related_to_137Cs_Concentration_Ratio and General_Notes to understand any dataset-specific caveats or methodological details.

- Potential analyses enabled
  - Correlations between K-40 and Cs-137 activity concentrations across species, sites, or plant parts.
  - Relationships between vegetation Cs-137 uptake (DM and FM) and soil concentrations via concentration ratios.
  - Temporal trends using Sampling_Date_Used_As_Decay_Date for decay-corrected comparisons.
  - Meta-analyses integrating these measurements with other environmental datasets in government or academic contexts.