# Description_Of_Trees_Metadata

- Overview: Metadata describing a tree dataset, including identifiers, post-wildfire condition, genus, and biometric measurements (diameter and height); notes linkage to a related dataset via site identifier.
- Key fields and meanings:
  - Site_identifier: numerical; same site identifier as used in the dataset 'Radionuclide distribution down soil profiles' (facilitates cross-dataset linkage).
  - Tree_Identifier: numerical; unique identifier for each tree.
  - Tree_Condition_After_Wildfire_Measured_October_2020: categorical; values Dead or Live; measured on 8 October 2020.
  - Tree_Genus: common name of the tree genus.
  - Tree_Diameter_Measured_At_Height_Of_1.3 m_Above_Ground_cm: diameter in centimeters measured at 1.3 meters above ground.
  - Tree_Height_m: height of the tree in meters.
  - NR not recorded: indicates missing data for the field.
- Data quality and usability notes:
  - Measurements include explicit units; helps consistency and comparability.
  - Some fields may have missing values (NR); affects analyses requiring complete data.
  - Clear definitions support data discovery, reuse, and cross-dataset integration.
- Data governance implications for Data Leaders:
  - Metadata supports data discovery, quality checks, and proper data integration with related datasets.
  - Enables assessment of data readiness for analysis, particularly post-wildfire tree status and biometric measurements.
  - Facilitates coordination and coherence across datasets through shared site identifiers.