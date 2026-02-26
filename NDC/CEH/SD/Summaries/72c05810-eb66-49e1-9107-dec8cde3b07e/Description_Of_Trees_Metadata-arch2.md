# Description_Of_Trees_Metadata

## Purpose and scope
- Metadata describing tree observations related to wildfire effects, with measurements taken on 8 October 2020.
- Supports standardized reporting and downstream analysis of environmental health and forest condition after wildfire.

## Key fields and definitions
- Site_identifier
  - Units: Not applicable
  - Explanation: Site identifier (numerical). Note: same site identifier as that used in the file "Radionuclide distribution down soil profiles" included in this dataset.
- Tree_Identifier
  - Units: Not applicable
  - Explanation: Individual tree identifier (numerical).
- Tree_Condition_After_Wildfire_Measured_October_2020
  - Units: Not applicable
  - Explanation: Tree condition after wildfire. Measured 8 October 2020. Possible values: Dead, Live.
- Tree_Genus
  - Units: Not applicable
  - Explanation: Genus of tree (common name).
- Tree_Diameter_Measured_At_Height_Of_1.3_m_Above_Ground_cm
  - Units: cm
  - Explanation: Diameter of tree measured at a height of 1.3 m above ground.
- Tree_Height_m
  - Units: m
  - Explanation: Height of tree. NR indicates not recorded.

## Data quality and handling
- Units are specified for diameter (cm) and height (m); other fields are Not applicable.
- NR (not recorded) appears for Tree_Height_m, indicating missing data in some records.

## Context for analysts
- Enables linking of tree data with other datasets via Site_identifier.
- Provides standardized attributes to support cross-dataset analyses of post-wildfire forest structure and health.

## Challenges and considerations
- Need to address missing Tree_Height_m values to improve completeness.
- Opportunity to increase dataset value by combining with additional data and ensuring accessible underlying data for broader analysis.