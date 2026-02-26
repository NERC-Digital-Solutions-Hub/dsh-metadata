# Dataset Documentation

- Countryside Survey dataset documenting national estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007).
- Estimates are presented as total lengths in thousands of kilometers (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence interval estimates.

- Key data elements (columns):
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of length (000s km)
  - MEAN_ESTIMATE: Mean length (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of length (000s km)
  - LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

- Linear feature types (codes and descriptions):
  - _1: Hedges (also known as managed hedgerows)
  - _3: Wall
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence
  - TOTAL: Total length of linear features

- Reporting and data structure notes:
  - Results are reported using a hierarchical class system; reporting avoids double counting of multi-element features.
  - Hedges take precedence in reporting when found with other features; hedge lengths are not counted again as part of walls or fences.

- Interpretation and caveats:
  - Negative values may appear in MEAN_ESTIMATE due to the statistical model; treat such values as zero.
  - Datasets may lack context at finer scales (e.g., local administration boundaries) and require careful interpretation when aggregating.
  - Data quality and access challenges may arise when unifying with other datasets or working with different formats.

- Use limitations and attribution:
  - All use of Countryside Survey data must be acknowledged.
  - Required copyright/acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.
  - Encouraged to reference related publications and methodological reports listed (e.g., Countryside Survey: UK Results from 2007; Technical Report No. 4/07; ITE Land Classification 2007).

- Access and references:
  - Countryside Survey website provides project overview and linkages to methodologies and reports.
  - Foundational sources include Scott (2007) Statistical Report, Bunce et al. (2007) ITE Land Classification, and earlier Bunce et al. (1996) ITE Land Classification work, among others.