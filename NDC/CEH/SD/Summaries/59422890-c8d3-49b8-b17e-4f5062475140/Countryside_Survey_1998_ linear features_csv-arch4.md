# Dataset Documentation

## Overview
- Provides national estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
- Results are reported as total lengths in thousands of kilometers (000s km) for each linear feature type by Land Class, including lower and upper 95% confidence limits.
- Data are derived from field survey codes mapped to a hierarchical reporting system that avoids double counting of multi-element features.

## Data Schema and Features
- Primary fields:
  - YEAR: Year of Survey
  - LAND_CLASS: ITE Land Class description
  - FEATURENO: Linear feature code
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% confidence limit (000s km)
  - MEAN_ESTIMATE: Mean length estimate (000s km)
  - UPPER_ESTIMATE: Upper 95% confidence limit (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)
- Linear feature codes and interpretations:
  - _1: Hedge (managed hedgerows; may accompany other features)
  - _3: Wall (stone or block walls; may include fences/banks alongside)
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence (post-and-wire/rail, etc.)
  - TOTAL: Total length of linear features
- Reporting rules:
  - A hierarchical class system is used; when reporting stock, there is no double counting for multi-element features.
  - Hedges take precedence in reporting when found with other features; estimates for walls/fences do not include lengths found with a hedge.
  - Negative MEAN_ESTIMATE values may occur due to the statistical model; treat these as zero.

## Calculation, Interpretation, and Data Quality
- Information is recorded during field surveys as a series of detailed codes, enabling results reporting in various combinations.
- Data are processed to produce national estimates from 1 km survey squares (method described in the referenced technical report).
- Acknowledge that some data may be incomplete or imprecise due to classification and modeling; negative values are to be treated as zero.

## Use, Limitations, and Licensing
- Use of Countryside Survey data must be acknowledged.
- Acknowledgement language required on all copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and "Countryside Survey © NERC- Centre for Ecology & Hydrology. All rights reserved."
- Data rights and copyright are asserted; licensing details and rights holder are specified.

## Access and References
- Countryside Survey Website provides project overview and methodological documents.
- Key references and supporting documentation:
  - Carey et al. 2008: Countryside Survey UK Results from 2007
  - Haines-Young et al. 2000: Accounting for nature: assessing habitats in the UK countryside
  - Scott 2007: CS Technical Report No.4/07 Statistical Report
  - Bunce et al. 1996, 2007; related ITE Land Classification publications
- Related metadata and methodology are available through listed links and NERC CEH resources.