# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
- Estimates reported as total lengths (000s km) by Land Class and linear feature type.
- Based on Countryside Survey field data; key for understanding hedges, walls, fences, and related linear features in Great Britain.

## Data structure and fields
- YEAR: Year of Survey (1990 for this dataset).
- LAND_CLASS: ITE Land Class (text description).
- FEATURENO: Linear feature code (e.g., _1, _3, _4, _5, _6, _7, TOTAL).
- FEATURE: Linear feature description (e.g., Hedge, Wall, Line of trees/shrubs/relict hedge/fence, etc.).
- LOWER_ESTIMATE: Lower 95% confidence interval of length (000s km).
- MEAN_ESTIMATE: Mean length estimate by Land Class (000s km). Note: negative values may occur due to the statistical model; treat as zero.
- UPPER_ESTIMATE: Upper 95% confidence interval of length (000s km).
- LAND_CLASS_AREA: Total area of relevant Land Class (00s ha).
- Reporting: No double counting of multi-element features; hedges take precedence over walls/fences when co-occurring.
- Units: Lengths in 000s km; Land Class area in 00s ha.

## Linear feature codes
- _1 = Hedge (managed woody vegetation; may be alongside other features).
- _3 = Wall (stone or block wall; may include fences or banks/grass strips).
- _4 = Line of trees/shrubs/relict hedge/fence.
- _5 = Line of trees/shrubs/relict hedge (includes avenues; may include banks/grass strips).
- _6 = Bank/grass strip (earth or stone-faced bank or grass strip; may have a fence).
- _7 = Fence (permanent post/rail or similar; may be alongside grass strip, ditch, or stream).
- TOTAL = Total length of linear features.

## Reporting rules and interpretation
- Features are reported hierarchically to avoid double counting; hedges have precedence when present with other features.
- The dataset allows reporting across six major feature types; the TOTAL reflects combined lengths without double counting.
- Negative MEAN_ESTIMATE values possible due to modeling; convert to zero for practical use.

## Data quality, provenance, and classification
- Based on Countryside Survey field survey data; national estimates for 1990 derived from 1 km survey squares.
- Uses the ITE Land Classification (2007 Vector dataset) as the classification framework.
- Foundational methodological sources available (technical and main reports) detailing how estimates are generated and classified.

## Use limitations and licensing
- Acknowledgement required on all copies and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- All uses should credit Countryside Survey data; data usage rights are governed by NERC-CEH.

## Access and references
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Key references and documents:
  - Carey, P.D., et al. (2008) Countryside Survey: UK Results from 2007.
  - Countryside Survey: 1990 main report (Barr et al., 1993).
  - Scott, W.A. (2007) CS Technical Report No. 4/07 – Statistical methods.
  - Bunce, R.G.H., et al. (1996, 2007) ITE Land Classification background and methodology.
  - Barr, C.J. et al. (1991) 1990 Countryside Survey Field Handbook.