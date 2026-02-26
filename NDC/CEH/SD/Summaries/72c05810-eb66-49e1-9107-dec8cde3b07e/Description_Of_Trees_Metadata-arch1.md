# Description_Of_Trees_Metadata

- What this dataset is
  - Metadata describing per-tree measurements taken after a wildfire (measured 8 October 2020).
  - Links to a broader dataset via a site identifier and a tree identifier.

- Core fields and what they mean
  - Site_identifier: numerical site ID (used to reference the broader dataset, including the radionuclide distribution dataset).
  - Tree_Identifier: numerical identifier for each tree.
  - Tree_Condition_After_Wildfire_Measured_October_2020: post-wildfire status for the tree (Dead or Live).
  - Tree_Genus: genus (common name) of the tree.
  - Tree_Diameter_Measured_At_Height_Of_1.3_m_Above_Ground_cm: diameter at breast height (DBH) in centimeters.
  - Tree_Height_m: height of the tree in meters.
  - NR not recorded: indicates missing values (not recorded) for fields where present.
  - Units: various (e.g., diameter in cm, height in m).

- Data quality and limitations
  - Some values may be missing (NR not recorded), notably Tree_Height_m.
  - Measurements are cross-sectional, taken at a single time point (post-wildfire).
  - Metadata uses categorical "Dead" vs "Live" for condition; potential need for consistent encoding if combining with other datasets.
  - Consistency concerns: ensure consistent Tree_Genus naming and handling of missing data.

- Analytical opportunities for analysts
  - Correlation analyses between post-wildfire survival (Dead/Live) and tree attributes:
    - Diameter at breast height (DBH) and tree height.
    - Genus/species and survival probability.
  - Predictive modeling to estimate survival likelihood after wildfire based on DBH, height, and genus.
  - Stratified analyses by Site_identifier to explore regional variation or site-level effects.
  - Integration with the radionuclide distribution dataset to examine whether exposure metrics relate to post-wildfire survival or tree growth metrics.
  - Survival analyses or logistic regression using Tree_Condition_After_Wildfire_Measured_October_2020 as the outcome.
  - Data harmonization checks to prepare for meta-analyses across datasets (e.g., unit standardization, handling NR values).

- Data linking and provenance
  - Site_identifier ties this metadata to other datasets collected at the same sites (e.g., radionuclide distribution down soil profiles).
  - Tree_Identifier provides traceability to individual-tree measurements within site data.

- Practical data-handling recommendations
  - Clean and standardize units (confirm all height and diameter measurements are numeric and consistently scaled).
  - Address missing values (e.g., impute or flag NR not recorded; document impact on analyses).
  - Encode Tree_Condition_After_Wildfire_Measured_October_2020 as a binary variable for modeling.
  - Validate the measurement date and ensure temporal alignment when combining with other time-sensitive datasets.
  - Maintain provenance by recording data sources and any transformations applied.