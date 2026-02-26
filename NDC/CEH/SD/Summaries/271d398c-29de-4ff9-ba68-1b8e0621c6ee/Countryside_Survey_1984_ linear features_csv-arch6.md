# Dataset Documentation

## Overview
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology (CEH)
- Purpose: Provide national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Reporting unit: Total lengths in thousands of kilometers (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence limits.
- Main fields:
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class description
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s km)
  - MEAN_ESTIMATE: Mean length estimate (000s km)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)

## Data structure and coding
- Linear features are reported using a hierarchical, non-overlapping scheme to avoid double counting.
- Six major feature types are reported:
  - _1: Hedge (line of woody vegetation managed to keep shape; may be alongside other features)
  - _3: Wall (stone/man-made wall; may include fences or banks)
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge (includes avenues)
  - _6: Bank/grass strip
  - _7: Fence (permanent posts/wires; may include grass strip, ditch, or stream)
  - TOTAL: Total length of linear features
- Reporting rule: When a hedge is present with other features, hedges have reporting precedence, and estimates for walls and fences do not include hedge portions.
- Note on data values: Negative values may appear in MEAN_ESTIMATE due to the statistical model; treat these as zero.

## Use and interpretation
- The dataset is designed for national-scale analysis of landscape linear features and supports ecological and policy-relevant insights.
- When aggregating or comparing across Land Classes, apply the hierarchical reporting rule to avoid double counting.
- Outputs are suitable for informing landscape management and biodiversity assessments, with explicit uncertainty bounds (lower/mean/upper estimates).

## Acknowledgement and limitations
- Use must acknowledge Countryside Survey data owned by NERC - CEH.
- Copyright: Countryside Survey ©; Database Right/Copyright NERC-Centre for Ecology & Hydrology; All rights reserved.
- Data limitations:
  - Background data age (1984 survey with 2007 Land Classification)
  - Potential patchiness and variation in data collection methods across features
  - Negative MEAN_ESTIMATE values can occur due to modelling; must be treated as zero

## Related materials and references
- Countryside Survey Website (project overview and methodologies)
  - http://www.countrysidesurvey.org.uk/
- Key publications:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007 – NERC/CEH
  - Scott (2007) CS Technical Report No. 4/07 – Statistical Report
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
  - Bunce et al. (2007) ITE Land Classification 2007 vector dataset
  - Barr et al. (1984) Changes in the Rural Environment etc. (Handbook and methodology)
- Data usage and methodological references:
  - ITE Land Classification descriptions and reporting logic
  - Guidance on avoiding double counting and precedence of hedges