# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
- Outputs are total lengths in metres for each linear feature type per 1km square per Land Class.
- Note: the dataset may include negative values in the LC2007-related columns due to the statistical model; treat negatives as zero.
- Data are drawn from Countryside Survey methods and are intended for consistent monitoring of environmental health over time.

## Data Structure and Variables
- Key identifiers and geometry:
  - FID: Feature ID (object auto-number)
  - Shape: Geometry; Shape_Length; Shape_Area
- Classification and timing:
  - LC2007: ITE Land Class (numeric)
  - LC2007_COD: ITE Land Class (text code)
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class
- Linear features (per 1km square, per land class):
  - LF_1: Hedges
  - LF_3: Wall
  - LF_4: Line of trees/shrubs/relict hedge/fence
  - LF_5: Line of trees/shrubs/relict hedge
  - LF_6: Bank/grass strip
  - LF_7: Fence
  - LFTOTAL: Total length of linear features
- Descriptive fields:
  - Each LF_* field described as “Estimate per 1km square in each land class in metres”
  - TOTAL described as “Total length of linear features”

## Feature Typologies and Reporting Rules
- Six major feature types are reported; information is stored as hierarchical codes enabling multiple reporting formats.
- No double counting: hedges are counted separately from walls and fences; if a hedge is present with other features, its length is not double-counted with those features.
- Hedges are prioritized in reporting when co-occurring with other features due to ecological and policy relevance.
- A hedge can be present with walls, fences, or related features; however, wall and fence lengths do not include portions that are part of hedges.

## Use, Access, and Documentation
- Use of Countryside Survey data must be acknowledged.
- Acknowledgement language (copyright):
  - “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
  - “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Countryside Survey Website provides project overview, methodologies, and additional documents.
- Related reports and methodologies are cited (UK results from 2007, 1990 main report, 2007 ITE Land Classification, field handbook, technical reports).

## Limitations and Context
- Data are designed for standardised environmental monitoring outputs (e.g., maps, charts, reports).
- The dataset is grounded in 1990 national estimates derived from 1km survey squares using the 2007 ITE Land Classification framework.
- Negative LC2007-derived values should be treated as zero in analyses.

## References and Further Reading
- Countryside Survey website and project documents
- Carey et al. (2008) Countryside Survey: UK Results from 2007
- Barr et al. (1993) Countryside Survey 1990: main report
- Scott (2007) CS Technical Report No.4/07
- Bunce et al. (2007) ITE Land Classification of Great Britain 2007
- Bunce et al. (1981, 1996) Merlewood Land Classification literature
- Field Handbook (1990) and related methodological materials