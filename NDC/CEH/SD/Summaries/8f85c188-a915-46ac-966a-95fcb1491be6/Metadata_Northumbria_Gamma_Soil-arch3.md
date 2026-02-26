# TREE_Northumbria_Gamma_Soil

## Overview
- Dataset describing soil gamma radiochemistry measurements conducted by UKCEH Radiochemistry Laboratory.
- Key isotopes measured: Potassium-40 (K-40) and Cesium-137 (Cs-137) expressed as activity per dry mass (Bq/kg DM).
- Includes metadata for each sample (identifiers, description, site), sample mass, and date handling for decay calculations.
- Aims to support environmental health monitoring and inform policy decisions by providing transparent measurement data and metadata.

## Data schema and key fields
- CEH_Sample_Identifier: UKCEH unique sample identifier.
- CEH_Sample_Description: Description of the sample.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of the soil sample analyzed (grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- Fresh_Mass_Dry_Mass_Ratio: Fresh mass to freeze-dried mass ratio of soil.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 in Bq/kg dry mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two-sigma counting error for K-40 in Bq/kg DM.
- K-40_<: Marker indicating the K-40 concentration is below the MDA (less-than value).
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration for K-40 (Bq/kg DM).
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 in Bq/kg DM.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two-sigma counting error for Cs-137 in Bq/kg DM.
- Cs-137_<: Marker indicating Cs-137 concentration is below the MDA.
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration for Cs-137 (Bq/kg DM).

## Metadata quality and interpretation
- Each measurement field is accompanied by an explanation, clarifying units and meaning.
- Uses "DM" (dry mass) for activity concentrations.
- "<" markers denote values below the respective Minimum Detectable Activity (MDA).
- "Not measured" corresponds to concentrations below the MDA.
- Decay-date linkage for accurate activity interpretation over time.

## Use in monitoring and policy
- Enables assessment of soil radioactivity as part of environmental health monitoring frameworks.
- Provides traceable, well-documented data to support decision-making, risk assessment, and policy evaluation.
- Facilitates transparency and reproducibility through explicit sample identifiers, descriptions, and measurement metadata.

## Data governance and challenges (context for monitoring framework authors)
- Emphasizes the need for robust metadata and clear data provenance (unique sample IDs, site details, description).
- Highlights potential data governance considerations when sharing underlying data, given MDA handling and not-measured flags.
- Data format requires transformation between units or mass definitions if integrating with other datasets (e.g., different mass bases or time since sampling).
- Clear QA implications: reporting of counting errors and MDAs supports assessment of data quality and reliability.