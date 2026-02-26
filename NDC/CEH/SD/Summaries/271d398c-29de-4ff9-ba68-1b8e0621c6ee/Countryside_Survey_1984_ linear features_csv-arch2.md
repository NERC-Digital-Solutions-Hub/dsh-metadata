# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Outputs expressed as total lengths in thousands of kilometers (000s km) for each linear feature type by Land Class, including lower and upper 95% confidence interval estimates.
- Includes year of survey, land class, feature codes/descriptions, mean estimates, and land class area.

## Data structure and contents
- Core fields:
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class (text)
  - FEATURENO: Linear feature code (text)
  - FEATURE: Linear feature description (text)
  - LOWER_ESTIMATE: Lower 95% CI of length (000s km)
  - MEAN_ESTIMATE: Mean length estimate (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of length (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)
- Data notes:
  - There may be negative MEAN_ESTIMATE values due to the statistical model; treat negatives as zero.
  - Reporting uses a hierarchical class system to avoid double counting multi-element features.

## Linear feature codes and reporting rules
- Codes and descriptions:
  - _1: Hedge — a line of woody vegetation that has been managed; may be alongside other features.
  - _3: Wall — built stone or block wall; may include walls with fences/banks/grass strips or lines of trees/shrubs.
  - _4: Line of trees/shrubs/relict hedge/fence — trees/shrubs in natural form; may include banks/grass strips.
  - _5: Line of trees/shrubs/relict hedge — trees/shrubs in natural form; includes avenues; may include banks/grass strips.
  - _6: Bank/grass strip — earth/stone-faced bank or grass strip with/without a fence.
  - _7: Fence — permanent post-and-wire/rail structure; may be with grass strip, ditch, or stream.
  - TOTAL: Total length of linear features.
- Reporting principle:
  - Features are reported hierarchically with no double counting of multi-element features.
  - A hedge-containing feature is reported as hedge, and the lengths of walls/fences that occur with a hedge are not included in the hedge length; likewise, hedge lengths exclude lengths counted as walls or fences separately.
  - Hedges are given precedence over other linear features when co-occurring, reflecting their ecological importance.

## Field data collection and use
- During field survey, linear landscape features were recorded as coded data, enabling flexible reporting combinations via the hierarchical system.
- Emphasizes standardized reporting of six major feature types and avoidance of double counting.

## Use limitations and rights
- All use of Countryside Survey data must be acknowledged.
- Required acknowledgement text:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Access and references
- Countryside Survey Website: general project overview and methodologies.
  - http://www.countrysidesurvey.org.uk/
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07 Statistical Report
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
  - Bunce et al. (2007) ITE Land Classification 2007 vector dataset
  - Additional historic methodology references (1981, 1984) linked in the document