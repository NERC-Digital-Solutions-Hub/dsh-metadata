# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Estimates are total lengths (in metres) for each linear feature type per 1 km square per Land Class.
- Note: there may be negative values in LC2007 due to the statistical model; treat these as zero.
- Data describe six major linear feature types and a total length, with associated geometry.

## Data Structure and Attributes
- FID: Object ID (auto-generated)
- Feature ID: Autonumber
- Shape: Geometry
- LC2007: Double
  - ITE Land Class (numeric) (Bunce et al., 2007)
- LC2007_COD: Text
  - ITE Land Class (text code) (Bunce et al., 2007)
- CSYEAR: Number
  - Year of survey
- LCAREA: Number
  - Total area of relevant Land Class (00s ha)
- LF_1: Number
  - Hedges — estimated length per 1 km square in each land class (metres)
- LF_3: Number
  - Wall — estimated length per 1 km square in each land class (metres)
- LF_4: Number
  - Line of trees/shrubs/relict hedge/fence — estimated length per 1 km square (metres)
- LF_5: Number
  - Line of trees/shrubs/relict hedge — estimated length per 1 km square (metres)
- LF_6: Number
  - Bank/grass strip — estimated length per 1 km square (metres)
- LF_7: Number
  - Fence — estimated length per 1 km square (metres)
- LFTOTAL: Number
  - Total length of linear features (metres)
- Shape_Length: Number
  - Length of Land Class shape
- Shape_Area: Number
  - Area of Land Class (square metres)

## Spatial and Temporal Scope
- Temporal: 1984 national estimates derived from the 1 km survey sample squares, aligned with the 2007 ITE Land Classification.
- Spatial: Per 1 km square within each Land Class; attributes map to 1984 Countryside Survey data.

## Feature Types and Reporting Rules
- Six major linear feature types are reported:
  - _1 Hedges
  - _3 Wall
  - _4 Line of trees/shrubs/relict hedge/fence
  - _5 Line of trees/shrubs/relict hedge
  - _6 Bank/grass strip
  - _7 Fence
- TOTAL: Total length of linear features.
- Reporting rule: no double counting of multi-element features; hedges take precedence when present with other features (e.g., a hedge with a wall or fence is counted as a hedge, and the accompanying wall/fence length is not counted under those other features).

## Data Use and Limitations
- All use of Countryside Survey (CS) data must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.
- Data may be distributed and used in publications, presentations, and maps; ensure the above acknowledgement is included.

## Data Quality, Provenance, and Methodology
- During field survey, linear landscape features were recorded as codes; results are reported using a hierarchical class system.
- The six major feature types are defined to avoid double counting and to allow reporting in multiple ways depending on code combinations.
- The dataset relies on the ITE Land Classification (2007) to categorize land classes and to derive 1984 stock estimates.

## Licensing, Acknowledgments, and References
- Acknowledgements and copyright notices required on all copies, publications, and presentations.
- Key references and sources:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07 Statistical Report
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007
  - Bunce et al. (1996); Bunce et al. (1981, 1984) related land classification and methodology documents
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/

## References and Further Information
- The dataset documentation references detailed methodologies, statistical approaches, and background on the ITE Land Classification and Countryside Survey procedures (see publications and the Countryside Survey website for full context).