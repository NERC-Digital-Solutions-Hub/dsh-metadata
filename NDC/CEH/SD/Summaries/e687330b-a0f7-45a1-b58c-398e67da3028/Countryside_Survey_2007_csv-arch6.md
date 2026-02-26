# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
- Reported as total lengths in '000s km for each linear feature type per Land Class, with both lower and upper 95% confidence limits.
- Data type: numbers; fields include Year of Survey, Land Class, feature codes/descriptions, and confidence interval estimates.

## Data structure and fields
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class description
- FEATURENO: Linear feature code
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
- MEAN_ESTIMATE: Mean feature length (000s km)
- UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

## Linear feature codes
- _1: Hedge – managed woody hedges; may co-occur with other features
- _3: Wall – stone/manufactured wall structures (may include related features)
- _4: Line of trees/shrubs/relict hedge/fence
- _5: Line of trees/shrubs/relict hedge
- _6: Bank/grass strip
- _7: Fence – permanent posts/wire/rail structures
- TOTAL: Total length of linear features

## Reporting, interpretation, and data governance
- Reporting uses a hierarchical class system; no double counting of multi-element features.
- Hedges have ecological/policy priority and are reported when found alongside walls or fences; estimates for walls/fences exclude hedge portions.
- During field surveys, information was recorded as codes; results can be reported in multiple ways by combining codes.
- Negative values may appear in MEAN_ESTIMATE due to the statistical model; treat negative values as zero.

## Use limitations and rights
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement and copyright notice:
  - Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.

## Related resources and references
- Countryside Survey Website: general project overview and methodologies
  - http://www.countrysidesurvey.org.uk/
- Key publications:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07 – Statistical Report
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
- Additional resources:
  - ITE Land Classification 2007 vector dataset
  - CS Technical Report No.1/07 – Field Mapping Handbook
  - Related methodological metadata: Countryside Survey habitat mapping handbook

## Practical notes for data use
- Units are in 000s of kilometers for feature lengths by Land Class.
- When combining features, apply the hierarchical rules to avoid double counting and to reflect hedges’ precedence.
- Use the confidence intervals to assess uncertainty around estimates; if needed, treat MEAN_ESTIMATE values conservatively (e.g., negative values as zero).