# TREE_Northumbria_Gamma_Water

## Overview
- Dataset appears to capture radiochemical analysis of water samples, focusing on K-40 and Cs-137 activity concentrations as of the sampling day, with associated measurement metadata and quality indicators.

## Key data elements
- CEH_Sample_Identifier
  - UKCEH radiochemistry laboratory unique sample identifier.
- CEH_Sample_Description
  - Description of the UKCEH sample.
- Site
  - Sampling site.
- Mass_of_Sample_Analysed_g
  - Mass of sample analysed (grams).
- Sampling_Date_Used_As_Decay_Date
  - Date the sample was taken and used as the decay date.
- K-40_Bq_per_kg_FM
  - Activity concentration of K-40 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_K-40_Bq_per_kg_FM
  - Two sigma counting error for K-40 in Bq per kg fresh mass.
- K-40_< 
  - Indicator that the value is a "<" (less than) value; relates to MDA column.
- MDA_K-40_Bq_per_kg_FM
  - Minimum Detectable Activity concentration for K-40 in Bq per kg fresh mass.
- Cs-137_Bq_per_kg_FM
  - Activity concentration of Cs-137 in Bq per kg fresh mass at the day of sampling.
- Counting_Error_Cs-137_Bq_per_kg_FM
  - Two sigma counting error for Cs-137 in Bq per kg fresh mass.
- Cs-137_< 
  - Indicator that the value is a "<" (less than) value; relates to MDA column.
- MDA_Cs-137_Bq_per_kg_FM
  - Minimum Detectable Activity concentration for Cs-137 in Bq per kg fresh mass.
- General_Notes
  - General notes (unspecified content).

## Data quality and metadata considerations
- Units
  - K-40 and Cs-137 values use Bq per kg fresh mass; sample mass uses grams. Some identifier-related fields list Units = n/a.
- Quality metrics
  - Two-sigma counting errors accompany activity concentrations.
  - MDA fields indicate detection limits for each radionuclide.
  - “<” markers indicate sub-threshold concentrations needing special handling.
- Provenance and context
  - Sampling date doubles as decay date; sample origin and description are recorded.
- Metadata completeness
  - Availability of site, sample description, and general notes supports context, but some fields are broad or n/a, suggesting room for richer metadata to improve discoverability and reuse.

## Practical implications for data leadership
- Data system perspective
  - The dataset embodies a structured radiochemical measurement product with explicit quality indicators (counting error, MDA) and clear provenance (sample ID, site, description, date).
- Data gaps and constraints
  - Some fields have n/a for units or broad general notes; potential gaps in metadata that could hinder discoverability and cross-system integration.
- Data use and governance considerations
  - Ensure consistent handling of "<" values and reporting of MDA when aggregating or comparing samples.
  - Maintain linkage between sampling date and decay corrections for temporal analyses.
  - Establish a clear data dictionary and data quality rules to support across-network data sharing and reuse.