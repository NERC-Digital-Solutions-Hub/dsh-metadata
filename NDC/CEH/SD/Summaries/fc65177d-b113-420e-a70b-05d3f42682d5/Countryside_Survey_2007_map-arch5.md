# Dataset Documentation

## Overview
- Countryside Survey data for 2007 providing national estimates of landscape linear feature stock using the ITE Land Classification.
- Estimates are expressed as total lengths (metres) per 1km square per Land Class; negative numbers should be treated as 0.

## Data content and structure
- Attributes include:
  - FID: Object ID (default autonumber)
  - Shape: Geometry (vector feature)
  - LC2007: Numeric ITE Land Class (1990s/2007 classification)
  - LC2007_COD: Text code for ITE Land Class
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class (00s ha)
  - LF_1 to LF_7: Lengths (metres) of specific linear features per 1km square per land class
  - LFTOTAL: Total length of linear features
  - Shape_Length: Length of Land Class shape
  - Shape_Area: Area of Land Class (square metres)
- Units: lengths in metres; Shape_Area in square metres.
- Data type: Vector dataset with geometry and associated attribute fields.

## Linear feature codes and interpretation
- _1: Hedges
- _3: Wall
- _4: Line of trees/shrubs/relict hedge/fence
- _5: Line of trees/shrubs/relict hedge
- _6: Bank/grass strip
- _7: Fence
- TOTAL: Total length of linear features
- Reporting uses a hierarchical classification; when reporting results, there is no double counting of multi-element features (e.g., hedges take precedence over walls/fences when co-occurring).

## Reporting approach and data lineage
- Results are reported for six major feature types.
- Hedge elements are prioritized in reporting when present with other features.
- The dataset records a detailed coding scheme that enables reporting in multiple ways based on code combinations.

## Use limitations and licensing
- All use of Countryside Survey data must be acknowledged.
- Suggested acknowledgment text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
- Acknowledgement and copyright apply to copies of data, publications, and presentations.

## Provenance and references
- Countryside Survey website and associated project documentation.
- Key references:
  - Carey, P.D. et al. (2008) Countryside Survey: UK Results from 2007.
  - Scott, W.A. (2007) CS Technical Report No.4/07 Statistical Report.
  - Bunce, R.G.H. et al. (1996) ITE Merlewood Land Classification of Great Britain.
  - Bunce, R.G.H. et al. (2007) ITE Land Classification of Great Britain 2007.
  - CS Technical Report No.1/07 Field Mapping Handbook.

## Data governance and stewardship considerations
- Clear field definitions and codes support data quality, interoperability, and discoverability.
- Documentation facilitates understanding of lineage and methodological choices (e.g., no double counting, hedge precedence).
- Ensure proper metadata management, licensing compliance, and attribution in datasets shared with others.
- Reference materials (methodologies and technical reports) should be accessible to users to support reuse and reproducibility.