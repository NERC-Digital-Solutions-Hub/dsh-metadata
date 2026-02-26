# Dataset Documentation

## Overview
- Dataset provides national estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
- Outputs are total lengths (in 000s km) for each linear feature type by Land Class, including lower and upper 95% confidence intervals.
- Data include year of survey, land class, feature codes and descriptions, and area of the land class (00s ha).
- Notes indicate possible negative values in the lower/mean estimates due to the statistical model; treat negative values as zero.

## Data structure and fields
- YEAR: numeric, year of survey.
- LAND_CLASS: text, ITE Land Class (Bunce et al., 2007; 1996).
- FEATURENO: text, linear feature code.
- FEATURE: text, linear feature description.
- LOWER_ESTIMATE: numeric, lower 95% confidence interval for length of feature by land class (000s km).
- MEAN_ESTIMATE: numeric, mean length of feature by land class (000s km).
- UPPER_ESTIMATE: numeric, upper 95% confidence interval for length of feature by land class (000s km).
- LAND_CLASS_AREA: numeric, total area of the relevant Land Class (00s ha).

## Linear feature codes and descriptions
- _1: Hedge — a line of woody vegetation managed so trees don’t take their natural shape; may be present with other features.
- _3: Wall — built structure of stone or blocks; may include related fences/grass strips; sometimes with other features.
- _4: Line of trees/shrubs/relict hedge/fence — line of trees/shrubs, natural shapes or originally planted hedges with a fence.
- _5: Line of trees/shrubs/relict hedge — line of trees/shrubs, natural shapes; may include avenues; may include banks/grass strips.
- _6: Bank/grass strip — earth or stone-faced bank or grass strip with/without a fence.
- _7: Fence — permanent post-and-wire/rail structure, with grass strip, ditch or stream; fences may be with hedges.
- TOTAL: total length of linear features.
- Important: a hedge can be beside a wall or fence; reporting ensures no double counting of multi-element features.

## Reporting rules and data integrity
- Results are reported using a hierarchical system of classes; no double counting of multi-element features (e.g., hedges take precedence).
- If a hedge is present with a wall or fence, hedge length is counted separately; wall/fence lengths do not include hedge segments.

## Use limitations and rights
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to be used: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © NERC - Centre for Ecology & Hydrology. All rights reserved.”
- The document provides general copyright and data rights information to be applied to copies, publications, and presentations.

## Related resources and references
- Countryside Survey Website: overview, methodologies, and links to documents.
- Key references and reports:
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008).
  - Countryside Survey 1990: main report (Barr et al., 1993).
  - CS Technical Report No.4/07: Statistical Report (Scott, 2007) — how national estimates are generated from 1 km survey squares.
  - ITE Merlewood Land Classification of Great Britain (Bunce et al., 1996; Bunce et al., 2007) — overview and relevance of land classification.
  - ITE Land Classification 2007 vector dataset (Bunce et al., 2007).
  - Additional background handbooks and reports (e.g., Barr 1991; 1990 Countryside Survey Field Handbook).
- Links to the above documents are provided in the dataset documentation for further methodological context.