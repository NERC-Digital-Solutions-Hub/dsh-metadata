# Dataset Documentation

- National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification. Results are presented as total lengths (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence intervals.
- Year of Survey: 2007. Data are derived from field-surveyed linear landscape features and reported within a hierarchical classification system to avoid double counting.
- Data owners and accessibility: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; access via the Countryside Survey website and related technical reports.

## Data structure and content

- Key fields:
  - YEAR: Year of survey (2007)
  - LAND_CLASS: ITE Land Class
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
  - MEAN_ESTIMATE: Mean length (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
  - LAND_CLASS_AREA: Total area of relevant Land Class (00s ha)
- Notes:
  - Estimates may include negative MEAN_ESTIMATE values due to the statistical model; treat negatives as zero.
  - Results are reported for six major feature types using a hierarchical class structure; when a feature co-occurs with others (e.g., hedges with walls or fences), hedges are given reporting precedence to reflect ecological importance.

## Linear feature codes

- _1 = Hedge: A line of woody vegetation managed to keep trees in a non-natural shape; hedges may occur with other features.
- _3 = Wall: Built structure of stone or blocks (including combined walls with fences or banks).
- _4 = Line of trees/shrubs/relict hedge/fence: Trees/shrubs in natural shape, may include banks/grass strips; can include hedges with fencing.
- _5 = Line of trees/shrubs/relict hedge: Line of trees/shrubs in natural shape; may include avenues; may include banks/grass strips.
- _6 = Bank/grass strip: Earth or stone-faced bank or grass strip, with or without a fence.
- _7 = Fence: Permanent post-and-wire/rail structure; may occur with grass strips, ditches, or streams.
- TOTAL: Total length of linear features.
- These codes were captured during field mapping and reported within a system that prevents double counting (e.g., hedges take precedence).

## Data derivation and reporting

- Field survey information on linear features was recorded using detailed codes, enabling reporting in multiple ways without double counting.
- A hierarchical reporting approach prioritizes hedges when present with other features.
- The dataset includes a separate TOTAL row summarizing the overall length across features.

## Limitations, usage notes, and acknowledgements

- Use limitations:
  - All use of Countryside Survey data must be acknowledged.
  - Required acknowledgement: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.”
  - Copyright: Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data provenance and context:
  - Derived from field observations within 1 km survey squares.
  - Methodological background and estimation details documented in related technical reports (see references).

## Access, governance, and related resources

- Countryside Survey website provides general project overview, dataset methodology, and links to documents.
- Key references:
  - Countryside Survey: UK Results from 2007 (2008) NERC/CEH
  - Scott, W.A. (2007). CS Technical Report No.4/07 – Statistical Report
  - Bunce et al. (1996, 2007) – ITE Land Classification of Great Britain
  - ITE Merlewood Land Classification of Great Britain (1996); ITE Land Classification 2007 (2007)
  - CS Technical Report No.1/07 – Field Mapping Handbook