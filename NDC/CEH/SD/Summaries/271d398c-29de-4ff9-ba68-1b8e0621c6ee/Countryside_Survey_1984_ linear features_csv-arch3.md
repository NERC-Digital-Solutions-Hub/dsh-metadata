# Dataset Documentation

## Overview
- Presents national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Measurements are in total lengths (000s km) for each linear feature type by Land Class, with lower, mean, and upper 95% confidence interval estimates.
- Data derived from Countryside Survey field surveys and designed to support environmental monitoring and policy analysis.

## Data structure and content
- Core fields:
  - YEAR: Year of Survey (1984 for this dataset)
  - LAND_CLASS: ITE Land Class description
  - FEATURENO: Linear feature code (see below)
  - FEATURE: Linear feature description
  - LOWER_ESTIMATE: Lower 95% CI of feature length (000s km)
  - MEAN_ESTIMATE: Mean estimated length (000s km)
  - UPPER_ESTIMATE: Upper 95% CI of feature length (000s km)
  - LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha)
- Feature codes and descriptions (examples):
  - _1: Hedge (managed hedgerows; may co-occur with other features)
  - _3: Wall
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence
  - TOTAL: Total length of linear features
- Reporting approach:
  - Six major feature types; hierarchical reporting ensures no double counting of multi-element features.
  - Hedges have precedence; hedge length estimates do not include lengths of walls or fences recorded with a hedge.
  - Note: negative values may appear in MEAN_ESTIMATE due to the statistical model; treat as zero.

## Provenance and methodology
- Data origin: Countryside Survey data by NERC - Centre for Ecology & Hydrology.
- Methodology highlights:
  - Estimates derived from the 1 km survey square sample framework (as per Scott 2007).
  - Uses the ITE Land Classification (2007 vector dataset) for land class assignment (see Bunce et al. references).
  - Field recording used a detailed code system to capture linear landscape features, enabling flexible reporting across different classifications.
- Key references:
  - Scott, W.A. (2007). CS Technical Report No.4/07 Statistical Report
  - Bunce, R.G.H. et al. (1997/2007) ITE Merlewood Land Classification and ITE Land Classification 2007
  - Additional foundational documents: 1981/1984 Merlewood materials and countryside survey methodology handbooks

## Use limitations and governance
- Data use and attribution:
  - All use must acknowledge Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Acknowledgement statement required on all copies, publications, and presentations.
- Accessibility and metadata:
  - Some metadata gaps can hinder reuse; users may need to contact dataset originators to verify data standards and completeness.
  - Transformation or reformatting of data may be necessary to align with specific analyses.
- Data sharing and governance:
  - Public sharing of underlying datasets is a consideration; governance processes should ensure data quality, openness where appropriate, and up-to-date storage.
- Data quality considerations:
  - Lack of data in some areas or at desirable standards; potential silos between organizations when integrating with other datasets.
  - Ensuring data remains current and well-documented is an ongoing priority.

## Access and additional resources
- Countryside Survey website provides project overview, methodologies, and links to relevant documents.
- Key publications and technical reports referenced for background and methodological details.