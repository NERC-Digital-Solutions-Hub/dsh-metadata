# Dataset Documentation

- Countryside Survey data © NERC - Centre for Ecology & Hydrology
- National estimates of landscape linear feature stock for 2007 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007)
- Estimates are given as total lengths in 000s km for each linear feature type per Land Class, including lower and upper confidence limits

## Overview
- Provides national estimates of six major linear landscape features for 2007
- Based on the 1 km survey sample squares and the ITE Land Classification
- Results are designed to inform policy decisions, environmental health monitoring, and future decision-making

## Data structure and fields
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class
- FEATURENO: Linear feature code (see codes below)
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% confidence interval of length (000s km)
- MEAN_ESTIMATE: Mean length of feature (000s km)
- UPPER_ESTIMATE: Upper 95% confidence interval of length (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

- Note: Some MEAN_ESTIMATE values may be negative due to the statistical model; treat these as zero

## Linear feature codes and reporting logic
- _1 = Hedge: line of woody vegetation managed to keep a shape; may be present with other features
- _3 = Wall: built stone/manufactured wall (may include related features like fences or banks)
- _4 = Line of trees/shrubs/relict hedge/fence: natural-shaped line including hedges with possible fences
- _5 = Line of trees/shrubs/relict hedge: natural line including avenues; may include banks/grass strips
- _6 = Bank/grass strip: earth/stone bank or grass strip with/without a fence
- _7 = Fence: permanent post/wire/rail structure with or without adjacent features
- TOTAL: Total length of linear features

- Reporting uses a hierarchical class system; no double counting of multi-element features
- Hedge features take precedence in reporting when found with walls or fences

## Data quality, limitations, and caveats
- Data use requires acknowledgement and copyright notice
- Potential data gaps and access issues common in environmental datasets
- Metadata completeness is important for verifying data suitability
- Data often require transformation to an analyzable format
- Some data may be difficult to share openly due to governance or governance constraints

## Use and governance
- All CS data usage must be acknowledged with the provided attribution
- Data should be stored, shared, and kept up to date following data governance practices
- Public sharing of underlying data may be restricted by governance considerations

## Access, references, and sources
- Countryside Survey Website: overview and methodologies (http://www.countrysidesurvey.org.uk/)
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07 Statistical Report
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
  - ITE Land Classification 2007 vector dataset
- Additional field methodology and reporting guides:
  - CS Technical Report No.1/07 Field Mapping Handbook