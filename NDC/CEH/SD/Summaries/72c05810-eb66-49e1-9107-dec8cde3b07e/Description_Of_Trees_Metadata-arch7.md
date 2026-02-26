# Description_Of_Trees_Metadata

## Overview
- Metadata describing per-tree attributes for GIS integration.
- Note: Site identifier ties to the related dataset "Radionuclide distribution down soil profiles."

## Data fields and definitions
- Site_identifier
  - Explanation: Site identifier (numerical)
  - Units: Not applicable
  - Additional note: Same site identifier used in the related dataset.
- Tree_Identifier
  - Explanation: Individual tree identifier (numerical)
  - Units: Not applicable
- Tree_Condition_After_Wildfire_Measured_October_2020
  - Explanation: Tree condition after wildfire; measured 8 October 2020
  - Units: Not applicable
  - Values: Dead, Live
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

## Data quality and notes
- Some fields may be not recorded (NR) for certain trees.
- Wildfire condition date provides a temporal reference for the status data.

## GIS use and applications
- Enables mapping and symbolization by tree status (Dead/Live), genus, diameter at breast height (1.3 m), and height.
- Supports linking tree-level data to spatial features and to the related radionuclide dataset via Site_identifier.