# Dataset Documentation

- Purpose: National estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification. Estimates are total lengths (metres) per 1km square per Land Class, with potential negative LC2007 values considered as zero.
- Scope: Provides a dataset describing six major linear feature types and their total lengths, enabling reporting without double counting across multi-element features.

## Data structure and key fields

- FID: Object ID; Feature ID (autonumber).
- Shape: Geometry (spatial representation) and Shape_Length, Shape_Area.
- LC2007: ITE Land Class (numeric) used for classification.
- LC2007_COD: ITE Land Class (text code).
- CSYEAR: Year of survey (1990).
- LCAREA: Total area of relevant Land Class.
- LF_1: Hedges (metres per 1km square, per land class).
- LF_3: Wall (metres per 1km square, per land class).
- LF_4: Line of trees/shrubs/relict hedge/fence (metres per 1km square, per land class).
- LF_5: Line of trees/shrubs/relict hedge (metres per 1km square, per land class).
- LF_6: Bank/grass strip (metres per 1km square, per land class).
- LF_7: Fence (metres per 1km square, per land class).
- LFTOTAL: Total length of linear features (metres per 1km square, per land class).
- Shape_Length, Shape_Area: Geometry measurements.

## Feature definitions and reporting rules

- Features coded as:
  - _1: Hedges
  - _3: Wall
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence
  - TOTAL: Total length of linear features
- Field recording: During the field survey, linear landscape features were captured with detailed codes allowing flexible reporting depending on code combinations.
- Hierarchical reporting: A six-type hierarchical system ensures no double counting of multi-element features. Hedges are given precedence when found with other features; hedges are ecologically prioritized in reporting, and estimates for walls/fences do not include hedge portions.

## Data use, limitations and governance

- Acknowledgement: Use of Countryside Survey data requires acknowledgement. Copyright: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Use limitations: The document specifies acknowledgement language to be used in copies, publications, and presentations.
- Data provenance: Based on 1990 field survey data, with results reported in relation to the 2007 ITE Land Classification.
- Negative values: LC2007 column may contain negative values due to the statistical model; treat these as zero in practice.
- Documentation and methodology references: The dataset and its methodology are described in associated Countryside Survey reports and technical documentation.

## Access, provenance and references

- Countryside Survey Website: General project overview and links to relevant documents and methodologies.
- Key references include:
  - Countryside Survey: UK Results from 2007 (overview and background)
  - Countryside Survey 1990: main report
  - CS Technical Report No.4/07: Statistical method for generating national estimates from 1km squares
  - ITE Land Classification of Great Britain (2007) and related foundational papers
  - Various field handbooks and methodological guides for mapping and classification

## Practical notes for data leaders

- Data system perspective:
  - The dataset is designed to support broad reporting across land classes while avoiding double counting, aiding policy relevance.
  - Metadata and provenance are clearly defined, with explicit acknowledgement and licensing requirements.
  - The data are linked to a standardized classification (ITE Land Classification 2007), enabling cross-study comparability.
- Data discovery and collaboration:
  - The dataset is accompanied by extensive methodological references, facilitating validation and reuse.
  - Users should consult the Countryside Survey Website and referenced reports to understand background, limitations, and proper attribution.
- Data quality and gaps:
  - Field-derived codes and hierarchical aggregation help manage complex feature configurations, but users should be aware of potential data sparsity in certain land classes and the handling of negative LC2007 values.