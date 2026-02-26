# Dataset Documentation

- Countryside Survey data © NERC - Centre for Ecology & Hydrology
- National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification. Estimates are presented as total lengths (in 000s km) for each linear feature type per Land Class, including lower and upper 95% confidence interval estimates.

## Data Structure and Content
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (text)
- FEATURENO: Linear feature code (text)
- FEATURE: Linear feature description (text)
- LOWER_ESTIMATE: Lower 95% CI estimate of feature length for the relevant Land Class (000s km)
- MEAN_ESTIMATE: Mean estimate of feature length for the relevant Land Class (000s km)
- UPPER_ESTIMATE: Upper 95% CI estimate of feature length for the relevant Land Class (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

Note: Some MEAN_ESTIMATE values may be negative due to the statistical model; treat these as zero.

## Linear Feature Codes
- _1: Hedge — a line of woody vegetation managed to maintain a specific shape; may be present with other features.
- _3: Wall — built stone/man-made wall structures (may include fences/banks/grass strips or trees/shrubs).
- _4: Line of trees/shrubs/relict hedge/fence — natural-shaped line of trees/shrubs; may include banks/grass strips.
- _5: Line of trees/shrubs/relict hedge — natural-shaped line of trees/shrubs; includes avenues; may include banks/grass strips.
- _6: Bank/grass strip — earth/stone-faced bank or grass strip with/without a fence.
- _7: Fence — permanent post-and-wire/rail structure; may appear with grass strip, ditch or stream.
- TOTAL: Total length of linear features.

## Reporting and Classification Principles
- Reporting uses a hierarchical class system to avoid double counting of multi-element features.
- A hedge feature is considered ecologically important and is given precedence when reporting alongside other features.
- The length of walls and fences found with a hedge is not included in the hedge’s length and is not double-counted.

## Use, Access, and Rights
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- For more information and methodologies, visit:
  - Countryside Survey Website: http://www.countrysidesurvey.org.uk/
  - Countryside Survey: UK Results from 2007 (2008) publication
  - Technical Reference: Scott, W.A. (2007). CS Technical Report No.4/07 (Statistical Report)
  - ITE Land Classification references (Bunce et al. 1996, 2007)
  - CS Field Mapping Methodology (Technical Report No.1/07)

## Practical Notes for Data Leaders
- Data provenance: derived from the 1 km survey sample squares; methodology described in CS Technical Report No.4/07.
- Data quality: includes 95% confidence intervals; negative MEAN_ESTIMATE values should be treated as zero.
- Data gaps and scope: reflects national estimates for 2007; consult linked reports for methodology and limitations; assess applicability to current or longitudinal analyses.
- Community and collaboration: references and methodology support integration with broader Countryside Survey datasets and ITE Land Classification framework.