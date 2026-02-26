# Dataset Documentation

- Countryside Survey data © NERC - Centre for Ecology & Hydrology
- National estimates of landscape linear feature stock for 1990 calculated using the 2007 ITE Land Classification; estimates are total lengths in '000s km for each linear feature type per Land Class, including lower and upper 95% confidence interval estimates.

## Data structure and fields

- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (Bunce et al., 2007; Bunce et al., 1996)
- FEATURENO: Linear feature code
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% confidence interval estimate of feature length for the relevant Land Class (000s km)
- MEAN_ESTIMATE: Mean estimate of feature length for the relevant Land Class (000s km)
  - Note: may include negative values due to the statistical model; treat as zero
- UPPER_ESTIMATE: Upper 95% confidence interval estimate of feature length for the relevant Land Class (000s km)
- LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)

## Linear feature codes

- _1: Hedge — a line of woody vegetation managed to alter natural shape; hedges may be present with other features
- _3: Wall — built stone/manufactured wall, may include fences or banks; may appear with other features
- _4: Line of trees/shrubs/relict hedge/fence — line of trees/shrubs in natural shape; may include banks/grass strips
- _5: Line of trees/shrubs/relict hedge — line of trees/shrubs including avenues; may include banks/grass strips
- _6: Bank/grass strip — earth/stone-faced bank or grass strip with/without a fence
- _7: Fence — permanent post/wire/rail structure with grass strip, ditch, or stream
- TOTAL: Total length of linear features
- Important reporting rule: no double counting of multi-element features; hedges have precedence and lengths of walls/fences found with a hedge are not included in wall/fence totals

## Reporting logic and data quality

- During field survey, results recorded as a hierarchical set of classes to enable reporting the stock of features without double counting
- Hedges are given ecological and policy priority in reporting when found alongside other features
- Lower/upper and mean estimates are provided per Land Class; negative mean values may occur due to model and should be treated as zero

## Use, limitations, and attribution

- All use of Countryside Survey data must be acknowledged with the exact acknowledgement:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data is linked to the Countryside Survey project and methodologies; use of the data should refer to the Countryside Survey website and the listed publications for background and methodology.

## Related resources and references

- Countryside Survey Website: general project overview and links to methodologies
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Barr et al. (1993) Countryside Survey 1990: main report
- Scott (2007) CS Technical Report No. 4/07: Statistical methods for deriving national estimates from 1 km squares
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007; ITE Land Classification vector dataset
- Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain
- Barr et al. (1991) 1990 Countryside Survey Field Handbook (handbook for mapping methodology)

## Practical notes for GIS use

- Data describes national estimates by Land Class for 1990; to map, join to ITE Land Classification surfaces or corresponding GIS layers by LAND_CLASS
- Values are in thousands of kilometers; LAND_CLASS_AREA is in hundreds of hectares; ensure unit handling during visualization
- Use the confidence intervals to convey uncertainty in map products (e.g., choropleth classes or error ribbons) and document the CI interpretation
- Acknowledge hedges’ precedence when summarizing by landscape type and avoid double counting with walls/fences in map presentations