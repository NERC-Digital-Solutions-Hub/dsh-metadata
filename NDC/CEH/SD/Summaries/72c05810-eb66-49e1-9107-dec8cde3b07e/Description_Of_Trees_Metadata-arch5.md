# Description_Of_Trees_Metadata

## Overview
- Metadata record for tree measurements following a wildfire, capturing identifiers, condition, genus, and physical measurements.
- Designed to support discovery, interoperability, and reuse across datasets within a managed data governance framework.

## Key fields and definitions
- Site_identifier
  - Explanation: Site identifier (numerical)
  - Notes: Same site identifier as in the related dataset “Radionuclide distribution down soil profiles”
- Tree_Identifier
  - Explanation: Individual tree identifier (numerical)
- Tree_Condition_After_Wildfire_Measured_October_2020
  - Explanation: Tree condition after wildfire; measured 8 October 2020
  - Possible values: Dead, Live
- Tree_Genus
  - Explanation: Genus of tree (common name)
- Tree_Diameter_Measured_At_Height_Of_1.3 m_Above_Ground_cm
  - Units: cm
  - Explanation: Diameter of tree measured at 1.3 m above ground
- Tree_Height_m
  - Units: m
  - Explanation: Height of tree
  - Note: NR (not recorded)

## Metadata quality and governance considerations
- Some fields indicate non-applicable units, but data types remain numerical or categorical as appropriate.
- Missing values flagged (e.g., Tree_Height_m NR) should be documented and handled in data quality checks.
- Provenance link to related datasets should be maintained (e.g., Site_identifier cross-reference with Radionuclide distribution dataset).
- Consistency in field naming and definitions supports interoperability across systems and portals.

## Data sharing and accessibility
- Metadata includes sufficient context to upload and catalogue the dataset in data portals.
- Cross-dataset linking (via Site_identifier) enhances discoverability and combined analyses with related datasets.

## Potential challenges for data stewards
- Ensuring completeness of records where certain fields are NR/not recorded.
- Maintaining consistent naming conventions and unit usage across datasets.
- Handling integration with multiple systems and formats while preserving metadata fidelity.

## Recommendations for action
- Validate and update missing values (e.g., Tree_Height_m) or explicitly document NR as a data gap.
- Ensure standardized metadata templates are used for consistency (definitions, units, dates).
- Maintain linkage to related datasets (e.g., Radionuclide distribution down soil profiles) for robust provenance.
- Document measurement dates and potential measurement uncertainties to support reuse and comparison.