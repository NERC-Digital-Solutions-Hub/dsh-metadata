# Dataset Documentation

- Countryside Survey data © NERC - Centre for Ecology & Hydrology

- Purpose and scope
  - Provides national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
  - Estimates are given as total lengths in thousands of kilometers (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence limits.
  - Data fields include YEAR, LAND_CLASS, FEATURENO, FEATURE, LOWER_ESTIMATE, MEAN_ESTIMATE, UPPER_ESTIMATE, and LAND_CLASS_AREA.
  - Notes may include negative MEAN_ESTIMATE values due to the statistical model; treat such values as zero.

- Data structure and fields
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code (text)
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
  - MEAN_ESTIMATE: Mean feature length (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
  - LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

- Linear feature codes and descriptions
  - _1: Hedge — managed line of woody vegetation; may be alongside other features
  - _3: Wall — built structure (stone, blocks; may include fences/banks)
  - _4: Line of trees/shrubs/relict hedge/fence — line of trees/shrubs in natural shape
  - _5: Line of trees/shrubs/relict hedge — line of trees/shrubs, including avenues
  - _6: Bank/grass strip — earth/stone-faced bank or grass strip
  - _7: Fence — post-and-wire or rail structure; may include adjacent grass strip, ditch, or stream
  - TOTAL: Total length of linear features
  - Reporting uses a hierarchical system of six major feature types; hedges have precedence when reported with other features

- Reporting rules and interpretation
  - No double counting of multi-element features; hedges are reported separately from walls and fences
  - Hedges are considered ecologically more important and policy-relevant, thus given reporting precedence when alongside other features

- Use limitations and acknowledgement
  - All use of Countryside Survey data must be acknowledged
  - Required acknowledgment: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

- Access to further information and references
  - Countryside Survey Website: overview and methodologies
    - http://www.countrysidesurvey.org.uk/
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No. 4/07 — Statistical Report (how national estimates are generated from 1 km survey squares)
  - Bunce et al. (1996, 2007) ITE Land Classification and related documentation
  - ITE Land Classification 2007 vector dataset and related methodology papers

- Context and origin
  - Field survey recorded linear landscape features as codes; reporting relies on a structured, non-overlapping classification to enable robust national estimates and cross-study comparability.