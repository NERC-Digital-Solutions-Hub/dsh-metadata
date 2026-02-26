# Description_Of_Trees_Metadata

## Overview
- Metadata schema for tree observations at sites, including identifiers and measured attributes.
- Key fields cover identification, health status after wildfire, taxonomy, and physical measurements.
- Units specified where applicable (diameter in cm; height in m); many fields are non-numeric (Not applicable).

## Data Fields and Definitions
- Site_identifier
  - Explanation: Site identifier (numerical)
  - Units: Not applicable
  - Notes: Same site identifier as in the dataset “Radionuclide distribution down soil profiles”
- Tree_Identifier
  - Explanation: Individual tree identifier (numerical)
  - Units: Not applicable
- Tree_Condition_After_Wildfire_Measured_October_2020
  - Explanation: Tree condition after wildfire (measured 8 October 2020)
  - Units: Not applicable
  - Values: Dead; Live
- Tree_Genus
  - Explanation: Genus of tree (common name)
  - Units: Not applicable
- Tree_Diameter_Measured_At_Height_Of_1.3_m_Above_Ground_cm
  - Explanation: Diameter of tree measured at 1.3 m above ground
  - Units: cm
- Tree_Height_m
  - Explanation: Height of tree
  - Units: m
  - Note: NR indicates not recorded
- NR
  - Explanation: Not recorded indicator for missing data

## Data Quality and Integration Notes
- NR (not recorded) indicates missing measurements in the dataset.
- Site_identifier can be linked with related datasets (e.g., Radionuclide distribution down soil profiles) to enable cross-dataset analyses.
- Mixed data types (numeric identifiers, categorical condition, and numeric measurements) may require careful data cleaning and type casting for analysis.

## How Data Support Can Help (Potential Data Products)
- Clean and validate data, ensuring consistent types and handling NR values.
- Combine with related datasets to support comprehensive analyses of wildfire effects and site-level context.
- Create self-serve outputs such as:
  - Dashboards showing counts of Dead vs Live trees by site.
  - Summaries of diameter and height distributions by genus.
  - Reports linking tree health with location and accompanying environmental datasets.
- Promote outputs and gather feedback to improve data capture (e.g., reducing NR occurrences) and data utility.