# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Provides national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Estimates are reported as total lengths in thousands of kilometers (000s km) for each linear feature type per Land Class, including lower and upper 95% confidence limits.
- Data fields include YEAR, LAND_CLASS, FEATURENO, FEATURE, LOWER_ESTIMATE, MEAN_ESTIMATE, UPPER_ESTIMATE, and LAND_CLASS_AREA (total area of the relevant Land Class).

## Data structure and fields
- YEAR: Year of Survey.
- LAND_CLASS: ITE Land Class description.
- FEATURENO: Linear feature code (see codes below).
- FEATURE: Linear feature description.
- LOWER_ESTIMATE: Lower 95% CI for length (000s km).
- MEAN_ESTIMATE: Mean length (000s km); note that negative values may occur due to the statistical model (treat as zero).
- UPPER_ESTIMATE: Upper 95% CI for length (000s km).
- LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha).

## Linear feature codes
- _1: Hedge — a line of woody vegetation managed to limit natural shape, may be present with other features.
- _3: Wall — built structure of stone or blocks; may include walls with fences, banks, or lines of trees.
- _4: Line of trees/shrubs/relict hedge/fence — trees/shrubs with natural shape; may include banks/grass strips.
- _5: Line of trees/shrubs/relict hedge — line of trees/shrubs, includes avenues; may include banks/grass strips.
- _6: Bank/grass strip — earth/stone-faced bank or grass strip, with or without a fence.
- _7: Fence — permanent posts and wires/rails; may include grass strips, ditches, or streams.
- TOTAL: Total length of linear features.

## Reporting rules and data relationships
- Results are reported using a hierarchical class system to avoid double counting.
- When a hedge is present with other features (wall or fence), hedge length takes precedence; walls/fences are not counted where a hedge is present.
- If multiple elements are involved, the total stock is reported without double counting multi-element features.
- Hedgerows are given ecological/policy precedence in reporting.

## Use limitations and acknowledgement
- All use of Countryside Survey data must include an acknowledgement.
- Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” plus copyright notice.
- Countryside Survey ©/Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Context and resources
- Countryside Survey Website: overview and links to relevant documents and methodologies.
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007.
  - Scott (2007) CS Technical Report No.4/07 (Statistical methodology for national estimates from 1km survey squares).
  - Bunce et al. (1996, 2007) ITE Land Classification sources and datasets.
- Related datasets and documentation provide background on methodologies and classification schemes used to generate these national estimates.