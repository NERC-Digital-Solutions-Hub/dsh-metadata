# TREE_Northumbria_Gamma_Soil

## Overview
- Document defines the data fields for UKCEH radiochemical soil analysis, focusing on K-40 and Cs-137 activity concentrations per unit dry mass.
- Metadata includes sample identifiers, description, sampling site, mass of sample analyzed, and the date used as the decay date.
- Includes ratios between fresh mass and freeze-dried mass to support standardized reporting.

## Data Fields

- CEH_Sample_Identifier: UKCEH Radiochemistry Laboratory unique sample identifier.
- CEH_Sample_Description: UKCEH sample description.
- Site: Sampling site.
- Mass_of_Sample_Analysed_g: Mass of sample analyzed (in grams).
- Sampling_Date_Used_As_Decay_Date: Date the sample was taken and used as the decay date.
- Fresh_Mass_Dry_Mass_Ratio: Fresh mass to freeze-dry mass ratio of soil.
- K-40_Bq_per_kg_DM: Activity concentration of K-40 in Bq per kg dry mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_DM: Two sigma counting error for K-40.
- K-40_<: Marker indicating the K-40 concentration is reported as below the MDA (less than).
- MDA_K-40_Bq_per_kg_DM: Minimum detectable activity concentration of K-40 in Bq per kg dry mass.
- Cs-137_Bq_per_kg_DM: Activity concentration of Cs-137 in Bq per kg dry mass.
- Counting_Error_Cs-137_Bq_per_kg_DM: Two sigma counting error for Cs-137.
- Cs-137_<: Marker indicating the Cs-137 concentration is reported as below the MDA (less than).
- MDA_Cs-137_Bq_per_kg_DM: Minimum detectable activity concentration of Cs-137 in Bq per kg dry mass.

## Units and Detection Limits
- Activity concentrations: Bq per kg dry mass (Bq/kg DM).
- Mass: grams (g).
- Decay date reference: date of sampling.

## Non-detects and Data Quality Notes
- Not measured (below MDA): When a concentration is below the minimum detectable activity (MDA), the dataset marks it accordingly.
- "<" markers accompany K-40 and Cs-137 fields to indicate concentrations are reported as less than the corresponding MDA.

## Context and Provenance
- Data originates from the UKCEH Radiochemistry Laboratory.
- Fields capture essential metadata and analytical results to enable correlation, interpretation, and potential modeling of soil radiochemical activity.