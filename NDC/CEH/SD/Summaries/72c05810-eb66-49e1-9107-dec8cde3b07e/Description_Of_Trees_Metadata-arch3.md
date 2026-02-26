# Description_Of_Trees_Metadata

## Purpose and scope
- Metadata for a dataset describing individual trees to support environmental health monitoring, post-wildfire assessment, and informing policy decisions.
- Enables linking tree measurements with other environmental datasets through site and tree identifiers.

## Data fields and explanations
- Site_identifier: numerical site ID; same identifier as used in the dataset "Radionuclide distribution down soil profiles."
- Tree_Identifier: numerical identifier for each tree.
- Tree_Condition_After_Wildfire_Measured_October_2020: status of the tree as of 8 October 2020 (Dead or Live).
- Tree_Genus: genus of the tree (noted as common name in explanation).
- Tree_Diameter_Measured_At_Height_Of_1.3 m_Above_Ground_cm: diameter at breast height (DBH) in centimeters.
- Tree_Height_m: height of the tree in meters.
- NR not recorded: indicates missing value (not recorded) for Tree_Height_m in this dataset.

## Units and measurement details
- Diameter field: centimeters (cm).
- Height field: meters (m).
- Condition date: 8 October 2020.

## Data quality and gaps
- Height value is missing (NR).
- Some metadata fields indicate non-applicable units; potential need for standardization.
- Completeness depends on data provenance and access to originators for verification.

## Governance and use for monitoring
- Data should be quality assured, cleaned, transformed, and shared with clear provenance.
- Enables cross-dataset linkage via Site_identifier and Tree_Identifier.
- Supports assessment of post-wildfire tree condition and growth metrics for policy evaluation and decision-making.

## Recommendations for data management
- Address and annotate missing Tree_Height_m values where possible.
- Ensure consistent metadata standards and units across fields.
- Maintain data provenance and share underlying data responsibly to support transparency and reuse.