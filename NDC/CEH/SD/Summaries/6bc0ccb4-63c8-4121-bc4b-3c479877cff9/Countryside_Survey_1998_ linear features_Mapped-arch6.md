# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
- Estimates are total lengths (metres) for each linear feature type per 1 km square per Land Class; negative values may occur due to the statistical model and should be treated as zero.
- During field survey, linear landscape features were recorded as detailed codes; reporting uses a hierarchical six-feature-class system with no double counting.

## Data Structure and Key Variables
- FID: Feature ID (autonumber). Shape: Geometry.
- LC2007: ITE Land Class (numeric). LC2007_COD: ITE Land Class (text code).
- CSYEAR: Year of survey.
- LCAREA: Total area of relevant Land Class (units: hectares).
- LF_1 to LF_7: Lengths (metres) per 1 km square for each feature type within each land class.
  - LF_1: Hedges
  - LF_3: Wall
  - LF_4: Line of trees/shrubs/relict hedge/fence
  - LF_5: Line of trees/shrubs/relict hedge
  - LF_6: Bank/grass strip
  - LF_7: Fence
- LFTOTAL: Total length of linear features (metres).
- Shape_Length, Shape_Area: Geometry metrics for the Land Class shape.

## Feature Classification and Reporting Rules
- Six major linear feature types are used for reporting.
- Hedge-related features take precedence ecologically; walls and fences are not counted where a hedge is present (no double counting of multi-element features).
- A hedge may accompany walls or fences, but lengths for walls/fences with hedge are reported separately and exclude hedge portions.
- Codes:
  - _1: Hedges
  - _3: Wall
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence
  - TOTAL: Total length of linear features

## Data Quality and Limitations
- Negative LC2007 values may appear due to the statistical model; treat as zero.
- Data are derived from a 1 km square sampling framework and aggregated by Land Class; there is potential patchiness in data coverage.
- The hierarchical reporting system is designed to avoid double counting when multiple feature types co-occur.

## Use Limitations and Acknowledgements
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement text to use on all copies, publications, and presentations: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.

## Access and References
- Countryside Survey Website: general overview, project links, and methodologies.
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Haines-Young et al. (2000) Accounting for nature: assessing habitats in the UK countryside
  - Scott (2007) CS Technical Report No.4/07 Statistical Report
  - Bunce et al. (1996, 2007) ITE Land Classification literature and data
- Related datasets and metadata: ITE Land Classification 2007 vector dataset; various background reports and methodological documents accessible via linked sources.