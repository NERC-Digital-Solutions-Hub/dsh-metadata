# TREE_Northumbria_Gamma_Water

## Overview
- A structured radiochemical dataset for gamma-emitting contaminants in water, detailing sample identifiers, site, mass analysed, sampling/decay timing, and radioisotope activity (K-40 and Cs-137) with associated uncertainties and detection limits.

## Data fields and meanings
- CEH_Sample_Identifier: UKCEH radiochemistry lab unique sample identifier
- CEH_Sample_Description: UKCEH sample description
- Site: Sampling site
- Mass_of_Sample_Analysed_g: Mass of sample analysed (grams)
- Sampling_Date_Used_As_Decay_Date: Date sample was taken (also used as decay date)
- K-40_Bq_per_kg_FM: Activity concentration of K-40 (Bq/kg fresh mass) at sampling
- Counting_Error_K-40_Bq_per_kg_FM: Two sigma counting error for K-40
- K-40_<: Less-than marker indicating values given as below detection/threshold
- MDA_K-40_Bq_per_kg_FM: Minimum Detectable Activity for K-40 (Bq/kg FM)
- Cs-137_Bq_per_kg_FM: Activity concentration of Cs-137 (Bq/kg fresh mass) at sampling
- Counting_Error_Cs-137_Bq_per_kg_FM: Two sigma counting error for Cs-137
- Cs-137_<: Less-than marker for Cs-137 values
- MDA_Cs-137_Bq_per_kg_FM: Minimum Detectable Activity for Cs-137 (Bq/kg FM)
- General_Notes: General notes about the dataset

## Measurement specifics
- Primary analytes: K-40 and Cs-137 activity concentrations on the day of sampling
- Uncertainty: Two sigma counting errors provided for both isotopes
- Detection limits: Minimum Detectable Activity (MDA) reported for both isotopes
- Data flags: "<" markers indicate values below the MDA

## Temporal and data context
- Sampling date is also used as the decay date, enabling decay corrections and temporal alignment of activity measurements

## Data quality and metadata considerations
- Clear unit definitions (Bq/kg fresh mass; mass in grams)
- Explanations accompany each field to support data interpretation and reuse
- A general notes field allows for additional context or caveats

## Relevance for monitoring and policy decisions
- Provides standardized radiochemical metrics to assess environmental radioactivity in water
- Facilitates trend analysis and policy evaluation by linking sample identifiers to clear measurement and uncertainty details
- Supports transparency and comparability through explicit metadata (sample description, site, date, and detection limits)

## Data governance and accessibility implications
- The need to maintain metadata quality and ensure data can be shared and reused
- Potential barriers include data access, duplication of effort, and metadata gaps; addressing these requires clear documentation, open sharing where appropriate, and adherence to data management standards at the source.