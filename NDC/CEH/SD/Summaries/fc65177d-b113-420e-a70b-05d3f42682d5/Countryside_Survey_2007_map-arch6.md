# Dataset Documentation

- Overview
  - National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
  - Estimates are reported as total lengths (in metres) per 1km square per Land Class.
  - Negative values should be treated as 0.

- Data structure and fields
  - FID: Object ID (default autonumber).
  - Description: Description of the feature (default).
  - Shape: Geometry type and description (geospatial shape data).
  - LC2007: Numeric ITE Land Class code (per Bunce et al., 2007).
  - LC2007_COD: Text code for ITE Land Class.
  - CSYEAR: Year of survey.
  - LCAREA: Total area of the relevant Land Class (in 00s ha).
  - LF_1 to LF_7: Estimated length (in metres per 1km square) for each feature type:
    - LF_1: Hedges
    - LF_3: Wall
    - LF_4: Line of trees/shrubs/relict hedge/fence
    - LF_5: Line of trees/shrubs/relict hedge
    - LF_6: Bank/grass strip
    - LF_7: Fence
  - LFTOTAL: Total length of linear features (metres per 1km square per land class).
  - Shape_Length / Shape_Area: Geometry metrics (length and area).

- Linear feature coding and interpretation
  - TOTAL: Total length of linear features.
  - Hedge, Wall, Line of trees/shrubs/relict hedge/fence, Line of trees/shrubs/relict hedge, Bank/grass strip, Fence correspond to codes:
    - _1 = Hedge
    - _3 = Wall
    - _4 = Line of trees/shrubs/relict hedge/fence
    - _5 = Line of trees/shrubs/relict hedge
    - _6 = Bank/grass strip
    - _7 = Fence
  - Multi-element features are recorded without double counting; a hedge may be present with walls or fences, but walls and fences counts exclude portions that are hedges.

- Reporting and data integrity rules
  - When reporting stock, use a hierarchical system of six major feature types.
  - Hedges are considered ecologically and policy-relevantly prioritized; hedges take precedence when co-occurring with other features.

- Use limitations and attribution
  - All use of Countryside Survey (CS) data must be acknowledged.
  - Acknowledgement text: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology. Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”
  - Data are © NERC-CEH with all rights reserved; applicable to copies, publications, and presentations.

- Access and references
  - Countryside Survey Website: general project overview, methodologies, and documents.
  - Key references:
    - Carey et al. (2008): Countryside Survey UK Results from 2007.
    - Scott (2007): CS Technical Report No.4/07 (Statistical Report) on how national estimates are generated.
    - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain.
    - CS Technical Report No.1/07: Field Mapping Handbook.
  - Relevant datasets and methodology documents are linked through the Countryside Survey and associated repositories.

- Practical notes for data work
  - Suitable for creating maps or dashboards of landscape linear features by land class and feature type.
  - When integrating with other datasets, align by CSYEAR, LC2007 codes, and ensure units are consistent (metres per 1km square per land class).
  - Treat any negative values as zero before analysis; preserve shape geometry for spatial analyses.