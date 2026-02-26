# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology National estimates of landscape linear feature stock (as listed above) for 2007 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007).

## Overview
- National estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification (references: Scott 2007; Bunce et al. 2007).
- Estimates are total lengths in metres for each linear feature type per 1km square per Land Class.
- Negative numbers should be treated as 0.

## Data schema and fields
- FID: Object ID. FID, Description: Default autonumber.
- Shape: Geometry. Shape, Description: Geometry.
- LC2007: Double. LC2007, Description: ITE Land Class (numeric) (Bunce et al., 2007).
- LC2007_COD: Text. LC2007_COD, Description: ITE Land Class (text code) (Bunce et al., 2007).
- CSYEAR: Number. CSYEAR, Description: Year of survey.
- LCAREA: Number. LCAREA, Description: Total area of relevant Land Class (00s ha).
- LF_1: Number. LF_1, Description: Hedges. LF_1, Units: Estimate per 1km square in each land class in metres.
- LF_3: Number. LF_3, Description: Wall. LF_3, Units: Estimate per 1km square in each land class in metres.
- LF_4: Number. LF_4, Description: Line of trees/shrubs/relict hedge/fence. LF_4, Units: Estimate per 1km square in each land class in metres.
- LF_5: Number. LF_5, Description: Line of trees/shrubs/relict hedge. LF_5, Units: Estimate per 1km square in each land class in metres.
- LF_6: Number. LF_6, Description: Bank/grass strip. LF_6, Units: Estimate per 1km square in each land class in metres.
- LF_7: Number. LF_7, Description: Fence. LF_7, Units: Estimate per 1km square in each land class in metres.
- LFTOTAL: Number. LFTOTAL, Description: Total length of linear features. LFTOTAL, Units: Estimate per 1km square in each land class in metres.
- Shape_Length: Number. Shape_Length, Description: Length of Land Class shape.
- Shape_Area: Number. Shape_Area, Description: Area of Land Class.

## Linear feature codes
- _1: Hedges. Description: A line of woody vegetation that has been managed so that trees no longer take their natural shape; hedges may be present with any feature below (also known as 'managed' hedgerows).
- _3: Wall. Description: Built structure of natural stone or manufactured blocks; may include walls with fences or banks/grass strips and/or lines of trees or shrubs.
- _4: Line of trees/shrubs/relict hedge/fence. Description: Line of trees or shrubs with natural shape; may include banks/grass strips.
- _5: Line of trees/shrubs/relict hedge. Description: Line of trees or shrubs with natural shape; may include avenues of trees; may include banks/grass strips.
- _6: Bank/grass strip. Description: Earth or stone-faced bank or grass strip with or without a fence.
- _7: Fence. Description: Permanent post and wire/rail structure; may include grass strip, ditch or stream.
- TOTAL: Total length of linear features. Description: Sum of all linear features.

## Reporting approach and data relationships
- During field surveys, linear landscape features are recorded as detailed codes.
- A hierarchical reporting system presents results for six major feature types.
- No double counting of multi-element features; a hedge is counted even if alongside other features, but wall and fence totals exclude lengths found with a hedge.
- Hedges are given precedence in reporting when found with other features due to ecological and policy relevance.

## Use limitations and attribution
- All use of Countryside Survey (CS) data must be acknowledged.
- Required acknowledgement text (to be included on copies, publications, reports, and presentations): 
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."

## Access, references, and documentation
- Countryside Survey Website: general project overview and links to relevant documents and methodologies.
  - http://www.countrysidesurvey.org.uk/
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007. NERC/Centre for Ecology & Hydrology.
  - Scott (2007). CS Technical Report No.4/07: Statistical Report (how national estimates are generated from 1km survey squares).
  - Bunce et al. (1996) ITE Merlewood Land Classification of Great Britain.
  - Bunce et al. (2007) ITE Land Classification of Great Britain 2007 (vector dataset).
  - CS Technical Report No.1/07: Field Mapping Handbook.