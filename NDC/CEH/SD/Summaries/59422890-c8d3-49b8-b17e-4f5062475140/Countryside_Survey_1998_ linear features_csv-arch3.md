# Dataset Documentation

- Countryside Survey data © NERC - Centre for Ecology & Hydrology
- National estimates of landscape linear feature stock for 1998 calculated using the 2007 ITE Land Classification (Scott, 2007; Bunce et al, 2007). Estimates are given as total lengths in '000s km for each linear feature type per Land Class including lower and upper confidence limits.

## Data fields and content
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (Bunce et al., 2007; Bunce et al., 1996)
- FEATURENO: Linear feature code (see below)
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% confidence interval estimate of feature length for the relevant Land Class (000s km)
- MEAN_ESTIMATE: Mean estimate of feature length for the relevant Land Class (000s km)
- UPPER_ESTIMATE: Upper 95% confidence interval estimate of feature length for the relevant Land Class (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

## Linear feature codes
- _1: Hedge — a line of woody vegetation managed to maintain a distinctive shape; may be alongside other features
- _3: Wall — built structure of stone/manufactured blocks; may include walls with fences or banks/grass strips
- _4: Line of trees/shrubs/relict hedge/fence — trees/shrubs in natural shape; may include banks/grass strips
- _5: Line of trees/shrubs/relict hedge — line of trees/shrubs; may include avenues; may include banks/grass strips
- _6: Bank/grass strip — earth/stone-faced bank or grass strip with/without a fence
- _7: Fence — permanent post-and-wire/rail structure; may be with grass strip, ditch or stream
- TOTAL: Total length of linear features
- Note: Results are reported using a hierarchical class system; reporting hedges takes precedence when a hedge is present with other features, and there is no double counting of multi-element features

## Reporting approach
- A hierarchical six-major-type system is used
- If a feature contains multiple elements (e.g., hedge with a wall), the hedge length is counted for hedges, while wall/fence lengths are not double-counted
- Hedge features are prioritized due to ecological importance and policy relevance

## Use limitations and governance
- All use of Countryside Survey data must be acknowledged
- Required acknowledgement and copyright notice to be used on all copies, publications, and presentations:
  - Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology
  - Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data quality considerations include:
  - Possible negative MEAN_ESTIMATE values due to the statistical model; treat as zero
  - 95% confidence intervals (LOWER_ESTIMATE and UPPER_ESTIMATE) indicate uncertainty
- Data may require metadata enhancement and transformation to be readily usable; gaps in metadata can hinder verification and reuse
- Public sharing of datasets used can be a barrier to data use in some contexts

## Data sources, provenance, and references
- Countryside Survey project overview and methodology:
  - Countryside Survey Website: http://www.countrysidesurvey.org.uk/
  - Carey et al. (2008): Countryside Survey: UK Results from 2007
  - Haines-Young et al. (2000): Accounting for nature: assessing habitats in the UK countryside
  - Scott (2007): CS Technical Report No.4/07 Statistical Report
  - Bunce et al. (1996): ITE Merlewood Land Classification of Great Britain
  - Bunce et al. (2007): ITE Land Classification 2007 vector dataset
  - Barr et al. (1998) and related works on Countryside Survey 2000 methodology
  - Countryside Survey Habitat Mapping Methodology references

- Related metadata and background:
  - Links to NERC CEH and associated publications for detailed background and data processing methods

## Practical use notes
- Data are presented as 1998 national estimates linked to 2007 ITE Land Classification
- Useful for monitoring and evaluating landscape-scale habitat features and informing policy decisions
- Ensure correct interpretation of confidence intervals and apply appropriate data quality considerations when using the estimates
- Follow governance and licensing requirements when sharing or publishing analyses based on this dataset