# Dataset Documentation
Countryside Survey data © NERC - Centre for Ecology & Hydrology
National estimates of landscape linear feature stock (as listed below) for 1998 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007).   Estimates are given as total lengths in '000s km for each linear feature type per Land Class including lower and upper confidence limit estimates.

## Overview
- Purpose: Provide national estimates of landscape linear feature stock for 1998, categorized by ITE Land Classification, with confidence intervals.
- Data content: Records include year, land class, a linear feature code, feature description, and length estimates (lower, mean, upper) plus land class area.
- Units: Lengths reported in thousands of kilometers (000s km); land class area in hundreds of hectares (00s ha).
- Hierarchy and reporting: Results are reported using a hierarchical classification to avoid double counting of multi-element features; hedges have precedence over walls and fences when they co-occur.
- Key caveat: Mean estimates may be negative due to the statistical model; treat negative mean values as zero.

## Data fields (primary variables)
- YEAR: Year of Survey
- LAND_CLASS: ITE Land Class (text description)
- FEATURENO: Linear feature code (text)
- FEATURE: Linear feature description
- LOWER_ESTIMATE: Lower 95% confidence limit of length (000s km)
- MEAN_ESTIMATE: Mean length (000s km)
- UPPER_ESTIMATE: Upper 95% confidence limit of length (000s km)
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)

## Linear feature codes (examples)
- _1: Hedge — a line of woody vegetation kept in a managed form; may be alongside other features
- _3: Wall — built stone/man-made wall; may include associated fences or banks
- _4: Line of trees/shrubs/relict hedge/fence — trees/shrubs in a line; may include fences
- _5: Line of trees/shrubs/relict hedge — natural-line tree/shrub arrangement; may include avenues
- _6: Bank/grass strip — earth/stone bank or grass strip with/without a fence
- _7: Fence — permanent post/rail/wire structure; may be alongside a grass strip, ditch, or stream
- TOTAL: Total length of linear features
- Note: A hedge feature is recorded if it contains a hedge element; hedge lengths are reported separately from walls/fences to avoid double counting.

## Reporting rules and data integrity
- When reporting, results can be reported in various ways depending on how codes are combined.
- No double counting for multi-element features; hedges take precedence when co-occurring with other feature types.

## Use limitations and attribution
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text (to be used on copies, publications, and presentations):
  - "Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Countryside Survey resources
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Key publications and methodologies:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
  - Scott (2007) CS Technical Report No.4/07: Statistical Report
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain
  - Additional background documents and metadata links provided in the dataset description.