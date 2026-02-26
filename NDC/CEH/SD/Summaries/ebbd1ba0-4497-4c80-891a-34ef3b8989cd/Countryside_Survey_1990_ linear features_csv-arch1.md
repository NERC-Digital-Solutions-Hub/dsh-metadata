# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology National estimates of landscape linear feature stock (as listed below) for 1990 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007).

- Purpose and scope
  - Provides national estimates of landscape linear feature stock for 1990.
  - Estimates are calculated using the 2007 ITE Land Classification.
  - Units are total lengths in '000s km per Land Class and feature, with lower, mean, and upper 95% confidence interval estimates.
  - Includes Land Class area (00s ha) for each relevant Land Class.
  - Methodology references: Scott (2007) and Bunce et al. (2007, 1996).

- Data structure and fields
  - YEAR: Year of Survey (1990)
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
  - MEAN_ESTIMATE: Mean length of feature (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
  - LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)
  - Note: Mean estimates may be negative due to the statistical model; treat negative values as zero.

- Linear feature codes and meanings
  - _1: Hedge — A line of woody vegetation managed to maintain its shape; may be alongside other features.
  - _3: Wall — Built structure of stone or blocks; may include walls with fences or banks/grass strips and/or trees/shrubs.
  - _4: Line of trees/shrubs/relict hedge/fence — Trees/shrubs in natural shape; may include banks/grass strips; includes hedges with associated fences.
  - _5: Line of trees/shrubs/relict hedge — Line of trees/shrubs in natural shape; may include avenues; includes banks/grass strips.
  - _6: Bank/grass strip — Earth or stone-faced bank or grass strip with/without a fence.
  - _7: Fence — Permanent post/wire/rail structure; may accompany grass strip, ditch, or stream.
  - TOTAL: Total length of linear features.
  - Important reporting rule: When reporting stock, hedges are prioritized; there is no double counting of multi-element features (a hedge is counted as hedges even if adjacent to walls/fences; but walls/fences within a hedge are not double-counted).

- Reporting conventions and interpretation
  - Results use a hierarchical six major feature types reporting system.
  - Hedge features take precedence over other linear features when co-located.
  - No double counting of multi-element features.

- Use limitations and rights
  - All use of Countryside Survey data must be acknowledged.
  - Required acknowledgement: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
  - Data access and rights are governed by copyright and database rights.

- Related resources and references
  - Countryside Survey website: overview and methodologies (http://www.countrysidesurvey.org.uk/)
  - Key reports and background:
    - Carey et al. (2008) Countryside Survey: UK Results from 2007
    - Countryside Survey 1990: main report (1993)
  - Technical and methodological references:
    - Scott (2007) CS Technical Report No.4/07 — Statistical report
    - Bunce et al. (1996) ITE Merlewood Land Classification
    - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
    - Barr et al. (1991) 1990 Countryside Survey Field Handbook (field methodology)
  - Access links and DOIs are provided in the dataset documentation for these sources.