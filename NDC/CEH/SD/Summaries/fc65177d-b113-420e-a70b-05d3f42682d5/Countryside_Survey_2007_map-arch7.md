# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

- The document describes national estimates of landscape linear feature stock for 2007, derived using the 2007 ITE Land Classification. Estimates are given as total lengths (in metres) for each linear feature type per 1 km square and per Land Class. Negative values should be treated as 0.

## Data schema and fields

- FID: Object ID (default autonumber)
- Description: Default description for FID
- Shape: Geometry
- Shape_Length: Length of Land Class shape
- Shape_Area: Area of Land Class (square metres)
- LC2007: Double — ITE Land Class (numeric) (Bunce et al., 2007)
- LC2007_COD: Text — ITE Land Class (text code)
- CSYEAR: Number — Year of survey
- LCAREA: Number — Total area of relevant Land Class (00s ha)
- LF_1: Number — Hedges (metres per 1 km square per land class)
- LF_3: Number — Wall (metres per 1 km square per land class)
- LF_4: Number — Line of trees/shrubs/relict hedge/fence (metres per 1 km square per land class)
- LF_5: Number — Line of trees/shrubs/relict hedge (metres per 1 km square per land class)
- LF_6: Number — Bank/grass strip (metres per 1 km square per land class)
- LF_7: Number — Fence (metres per 1 km square per land class)
- LFTOTAL: Number — Total length of linear features (metres per 1 km square per land class)

- Reporting attributes related to land classification:
  - LC2007_COD: textual code for Land Class
  - CSYEAR: year of survey
  - LCAREA: total area of the relevant Land Class (in 00s hectares)

## Linear feature codes and classification

- _1: Hedge — Woody vegetation, managed so trees do not take natural shape (also known as hedgerows); may be present with other features
- _3: Wall — Built structure of stone or blocks; may include walls with fences or banks/grass strips and/or lines of trees or shrubs
- _4: Line of trees/shrubs/relict hedge/fence — Trees/shrubs in their natural shape; may include banks/grass strips
- _5: Line of trees/shrubs/relict hedge — Line of trees/shrubs; may include avenues; may include banks/grass strips
- _6: Bank/grass strip — Earth/stone-faced bank or grass strip with or without a fence
- _7: Fence — Permanent post and wire/rail structure; may include grass strip, ditch or stream
- TOTAL: Total length of linear features

- During field surveys, the features were recorded as these codes. A six-type hierarchical reporting approach is used, ensuring no double counting of multi-element features. A hedge is given precedence when reporting alongside other features; hedges may coexist with walls or fences, but lengths for walls/fences excluding hedge portions are reported separately.

## Reporting methodology

- Features are reported using a hierarchical system of six major feature types.
- No double counting: multi-element features are counted in a way that avoids duplication.
- Hedges are prioritized in reporting when co-occurring with other linear features.

## Use limitations and licensing

- All use of Countryside Survey data must include the acknowledgement:
  - “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology”
- Countryside Survey © Database Right/Copyright NERC - Centre for Ecology & Hydrology. All rights reserved.

## Access, references, and resources

- Countryside Survey Website: General overview and project links
  - http://www.countrysidesurvey.org.uk/
- Key references:
  - Carey, P.D. et al. (2008) Countryside Survey: UK Results from 2007. NERC/Centre for Ecology & Hydrology.
  - Scott, W.A. (2007) CS Technical Report No.4/07 Statistical Report — how national estimates are generated from 1 km survey squares
  - Bunce, R.G.H. et al. (1997-2007) ITE Land Classification documents (including 2007 vector dataset)
- Related methodology and field mapping:
  - CS Technical Report No.1/07 Field Mapping Handbook — Countryside Survey Habitat Mapping Methodology
- Links to metadata and project documentation:
  - Statistical reports and land classification references available via CEH/EID Chub metadata pages (as cited in the document)