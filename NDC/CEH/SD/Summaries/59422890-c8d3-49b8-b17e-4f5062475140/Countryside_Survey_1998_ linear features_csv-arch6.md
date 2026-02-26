# Dataset Documentation

## Overview
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology
- Purpose: National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification
- Output: Total lengths in thousands of kilometers (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence interval estimates
- Coverage: Data reported by Land Class with associated land class area (00s ha)

## Data structure and fields
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (text)
- FEATURENO: Linear feature code
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% confidence interval for length (000s km)
- MEAN_ESTIMATE: Mean length for feature (000s km)
- UPPER_ESTIMATE: Upper 95% confidence interval for length (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)
- Note: Negative values may appear in MEAN_ESTIMATE due to the statistical model; treat as zero

## Linear feature codes and reporting
- _1: Hedge – hedges (woody vegetation) may be present with other features; hedges are prioritized in reporting
- _3: Wall – built stone/manufactured walls; may include associated features
- _4: Line of trees/shrubs/relict hedge/fence – natural-shaped line of trees/shrubs; may include banks/grass strips
- _5: Line of trees/shrubs/relict hedge – line of trees/shrubs; may include avenues and banks/grass strips
- _6: Bank/grass strip – earth/stone-faced bank or grass strip with/without fence
- _7: Fence – permanent post/ wire/ rail structure with grass strip, ditch, or stream
- TOTAL: Total length of linear features
- Reporting principle: Six major feature types with no double counting of multi-element features
  - Hedge lengths are reported even when accompanied by walls or fences
  - Walls and fences reporting exclude lengths that are found with a hedge

## Use and interpretation
- Derived from 1 km survey squares to generate national estimates (Scott 2007 Technical Report)
- Units: MEAN/LOWER/UPPER in 000s km; LAND_CLASS_AREA in 00s ha
- Ecological emphasis: hedges are given precedence for policy relevance
- Data can support analysis of landscape connectivity and hedgerow prevalence
- Practical data handling: map codes to readable descriptions; report mean with confidence intervals; apply zero for negative MEAN_ESTIMATE values

## Use limitations and rights
- Acknowledgement required on all copies, publications, and presentations
  - Acknowledgement: Countryside Survey data owned by NERC - CEH
  - Countryside Survey ©; Database Right/Copyright NERC-CEH; All rights reserved
- Access and methodology references:
  - Countryside Survey Website: overview and methodologies
  - Key references include: CS Technical Report No.4/07; ITE Land Classification documentation (2007 and earlier)
- Cited sources provide background on data generation, classification, and reporting conventions

## Practical notes for data product creation
- Build end-user tools that present fields: YEAR, LAND_CLASS, FEATURE, MEAN_ESTIMATE, LOWER_ESTIMATE, UPPER_ESTIMATE, LAND_CLASS_AREA
- Include mapping from FEATURENO/FEATURE to user-friendly descriptions
- Clearly display 95% confidence intervals and handle negative MEAN_ESTIMATE values as zero
- Document the non-double-counting rule and hedge precedence in any visualization or report

## References and further reading
- Countryside Survey project website and accompanying methodologies
- Related publications: 2000 ITE Land Classification overview; 2007 ITE Land Classification vector dataset; Scott (2007) Statistical Report; Bunce et al. (1996, 2007) ITE Land Classification developments
- See also: Countryside Survey: UK Results from 2007 (Carey et al., 2008) and associated technical reports