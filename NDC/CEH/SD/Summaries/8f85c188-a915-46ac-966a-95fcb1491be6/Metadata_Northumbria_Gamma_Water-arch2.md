# TREE_Northumbria_Gamma_Water

## Overview
- Radiochemical water sampling dataset linked to UKCEH radiochemistry laboratory.
- Records activity concentrations of K-40 and Cs-137 in water samples, expressed as Bq per kg fresh mass (FM) at the day of sampling.
- Includes sample identifiers, site information, sample mass, and date used as the decay date.
- Data are prepared for quality assurance, cleaning, transformation, and standardized presentation (reports, maps, charts) and are stored/uploaded to appropriate data portals.

## Data Elements and What They Represent
- CEH_Sample_Identifier: unique sample identifier.
- CEH_Sample_Description: description of the sample.
- Site: sampling site.
- Mass_of_Sample_Analysed_g: mass of the sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date: date the sample was taken and used as decay date.
- K-40_Bq_per_kg_FM: activity concentration of potassium-40 at the day of sampling (Bq/kg FM).
- Counting_Error_K-40_Bq_per_kg_FM: two-sigma counting error for K-40 (Bq/kg FM).
- K-40_<: indicator that the value is reported as a '<' (less than) value; corresponds to MDA_K-40_Bq_per_kg_FM.
- MDA_K-40_Bq_per_kg_FM: minimum detectable activity concentration for K-40 (Bq/kg FM).
- Cs-137_Bq_per_kg_FM: activity concentration of cesium-137 at the day of sampling (Bq/kg FM).
- Counting_Error_Cs-137_Bq_per_kg_FM: two-sigma counting error for Cs-137 (Bq/kg FM).
- Cs-137_<: indicator that the Cs-137 value is reported as a '<' value; corresponds to MDA_Cs-137_Bq_per_kg_FM.
- MDA_Cs-137_Bq_per_kg_FM: minimum detectable activity concentration for Cs-137 (Bq/kg FM).
- General_Notes: any additional notes.

## Data Quality, Standardization, and Usage
- Units are standardized: Bq per kg fresh mass for activity; mass in grams; dates for sampling/decay.
- "<" markers denote values below the MDA threshold and are linked to MDA fields.
- Data verification and quality assurance are implied prior to analysis, with datasets stored and made accessible through appropriate portals.

## How Analysts Use This Dataset
- Verify and quality-control data from established sources; clean and transform as needed.
- Analyze using standardised methods to assess environmental radiochemical status against standards.
- Present findings via clear formats (reports, maps, charts) for monitoring environmental health and policy performance over time.

## Relevance to Monitoring Challenges
- Increases dataset value by enabling integration with other relevant data sources for comprehensive monitoring.
- Supports access to underlying data to promote transparency and broader use in environmental assessments.