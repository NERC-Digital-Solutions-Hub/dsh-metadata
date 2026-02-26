# Dataset Documentation

- UK Countryside Survey dataset documenting national estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification. Estimates are total lengths (in metres) for each linear feature type per 1km square per Land Class. Negative values in LC2007 are to be treated as zero.
- Data include geometry (shape) and a range of fields describing land class, year, area, and specific linear features.

## Data structure and key variables
- Core fields:
  - FID: Feature ID
  - LC2007: ITE Land Class (numeric)
  - LC2007_COD: Land Class code (text)
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class
  - LFTOTAL: Total length of linear features
  - LF_1: Hedges (metres per 1km square per land class)
  - LF_3: Wall
  - LF_4: Line of trees/shrubs/relict hedge/fence
  - LF_5: Line of trees/shrubs/relict hedge
  - LF_6: Bank/grass strip
  - LF_7: Fence
  - Shape_Length, Shape_Area: Geometric metadata
- Feature definitions emphasize six major types of linear features and note that hedges take precedence in reporting when combined with other features, to avoid double counting.

## Reporting approach and interpretation
- Reporting is hierarchical to prevent double counting of multi-element features.
- Hedge features are prioritized; walls and fences are not counted where a hedge is present.
- Results express stock as metres of linear feature per 1km square per Land Class.

## Use limitations and governance
- Use must be acknowledged with the specified attribution: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Data sharing: underlying data should be shared publicly where appropriate, but this can pose barriers; metadata quality and completeness may hinder reuse.
- Metadata issues: inadequate metadata can impede verification of data suitability; data may require transformation to be usable.
- Data quality and management: data should be quality assured, cleaned, transformed, analyzed, and clearly presented (e.g., in reports or dashboards); data governance processes should be in place to ensure datasets meet standards and remain up to date.

## Publications, references, and resources
- Countryside Survey website provides overview and links to methodologies and documents.
- Foundational references include:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No. 4/07 – Statistical Report
  - Bunce et al. (1996, 2007) ITE Merlewood Land Classification references
- Useful data and metadata links:
  - ITE Land Classification 2007 vector dataset and related methodological papers
  - Countryside Survey technical and historical documentation (e.g., 1984 habitat mapping methodology)

## Practical implications for monitoring frameworks
- Strengths: provides standardized, nationally scaled metrics of linear landscape features with clear hierarchical reporting to avoid double counting; explicit data fields and classifications support structured monitoring.
- Challenges to anticipate: data gaps or limited access; inter-organizational data silos; need for robust metadata; openness vs. copyright/usage restrictions; ensuring timely updates and governance for shared datasets.