# TREE_Northumbria_Gamma_Vegetation

## Overview
- A radiochemical dataset for vegetation samples, focusing on potassium-40 (K-40) and cesium-137 (Cs-137) activity concentrations.
- Includes taxonomic information, sampling context, sample identifiers, and detailed measurement metadata to support analysis and data reuse.

## Data Model and Key Fields
- Taxonomy
  - Latin_Species_Name, Common_Species_Name with explanations of each field.
- Sampling context
  - Site, CEH_Sample_Identifier, CEH_Sample_Description, Sampling_Date_Used_As_Decay_Date (date taken used as decay date).
  - Plant_Part_Analysed (part of plant analysed).
- Sample metadata
  - Dry_Mass_Of_Sample_Analysed_g (dry mass in grams).
  - Sampling and description fields clarify what was measured and how.
- Radiochemical measurements
  - K-40_Bq_per_kg_DM and K-40_Bq_per_kg_FM (activity concentration in Bq per kg dry mass and fresh mass) with corresponding Counting_Error_K-40_Bq_per_kg_DM and Counting_Error_K-40_Bq_per_kg_FM.
  - K-40_< markers indicating concentrations below the detection threshold, plus MDA_K-40_Bq_per_kg_DM and MDA_K-40_Bq_per_kg_FM (minimum detectable activity).
  - Cs-137_Bq_per_kg_DM and Cs-137_Bq_per_kg_FM with their Counting_Error_Cs-137_Bq_per_kg_DM and Counting_Error_Cs-137_Bq_per_kg_FM.
  - Cs-137_< markers and MDA_Cs-137_Bq_per_kg_DM / MDA_Cs-137_Bq_per_kg_FM for concentrations below detection limits.
- Concentration ratios
  - Cs-137_Concentration_Ratio_DM_< and Cs-137_Concentration_Ratio_DM (dry mass basis), Cs-137_Concentration_Ratio_FM_< and Cs-137_Concentration_Ratio_FM (fresh mass basis).
  - Explanations clarify ratios compare vegetation to soil, and the meaning of "<" values.
- Notes and guidance
  - Notes_Related_to_137Cs_Concentration_Ratio and General_Notes fields for additional context.

## Data Quality, Metadata, and Access
- Each field includes an Explanation describing its meaning and units, supporting transparency and reuse.
- Measurements include uncertainty indicators (Two sigma counting errors) and detection limits (MDA) with explicit < markers.
- Data are associated with UKCEH radiochemistry lab identifiers and vegetation sampling context, aiding provenance and traceability.

## Implications for Data Strategy and Leadership
- Demonstrates a structured, metadata-rich approach enabling discoverability, provenance, and cross-study comparability.
- Supports multi-mass basis (Dry Mass vs Fresh Mass) measurements and derived concentration ratios for robust cross-context analyses.
- Highlights the importance of capturing measurement uncertainty and detection limits to inform interpretation and decision-making.
- The presence of detailed explanations and standardized fields aligns with best practices for data stewardship, particularly in multi-partner or networked data environments.