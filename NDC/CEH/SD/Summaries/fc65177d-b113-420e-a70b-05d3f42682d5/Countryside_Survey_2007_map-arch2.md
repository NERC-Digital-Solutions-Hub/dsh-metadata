# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology National estimates of landscape linear feature stock (as listed above) for 2007 calculated using the 2007 ITE Land Classification (refer to Scott, 2007; Bunce et al, 2007)

## Overview
- Purpose: Provide national estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
- Output: Estimates are total lengths (in metres) per 1 km square for each linear feature type within each Land Class.
- Data handling note: Negative numbers should be treated as 0.
- Dataset scope: Field-surveyed linear landscape features recorded as a set of detailed codes, later reported through a hierarchical classification system to avoid double counting.

## Data structure and key fields
- Identifiers and geometry
  - FID: Object ID; automatically generated
  - Shape: Geometry; Shape_Length and Shape_Area describe feature geometry
- Land classification and year
  - LC2007: ITE Land Class (numeric)
  - LC2007_COD: ITE Land Class code (text)
  - CSYEAR: Year of survey
- Area and feature length data
  - LCAREA: Total area of the relevant land class (in 0s ha)
  - LF_1, LF_3, LF_4, LF_5, LF_6, LF_7: Estimated lengths per 1 km square for each feature type (in metres)
  - LFTOTAL: Total length of all linear features (in metres)
- Shape descriptors
  - Shape_Length: Length of Land Class shape
  - Shape_Area: Area of Land Class (in square metres)

## Linear feature types and codes
- _1: Hedges
  - Description: A line of woody vegetation managed to keep trees from taking natural shape; hedges may accompany other features.
- _3: Wall
  - Description: Built structures of stone/blocks, including walls with fences or banks/grass strips; may be combined with other features.
- _4: Line of trees/shrubs/relict hedge/fence
  - Description: Line of trees/shrubs in natural shape; may include banks/grass strips; includes hedges with fences.
- _5: Line of trees/shrubs/relict hedge
  - Description: Line of trees/shrubs in natural shape, including avenues; may include banks/grass strips.
- _6: Bank/grass strip
  - Description: Bank or grass strip with or without a fence.
- _7: Fence
  - Description: Permanent post-and-wire/rail structure; may include grass strip, ditch, or stream.
- TOTAL: Total length of linear features
  - Description: Aggregate total length across features

## Reporting methodology
- Hierarchical reporting: Results are presented using a hierarchical system of six major feature types, derived from combinations of detailed codes.
- No double counting: When reporting stock, multi-element features (e.g., hedge plus wall) are not double-counted; hedges are given precedence due to ecological and policy relevance.
- Code independence: A hedge can be present with walls or fences, but the lengths of walls/fences are not counted where a hedge is present.

## Use and limitations
- Acknowledgement requirement: All use of Countryside Survey data must include the stated acknowledgement.
- Copyright: Countryside Survey data are owned by NERC - Centre for Ecology & Hydrology; all rights reserved.
- Data use context: Data are intended to support monitoring and policy evaluation of environmental health over time, enabling standardized reporting and cross-study comparisons.

## Resources and references
- Countryside Survey Website: General overview, methodology, and links to related documents.
- Key reports:
  - Carey et al. (2008): Countryside Survey UK Results from 2007
  - Scott (2007): CS Technical Report No. 4/07 — Statistical Report
  - Bunce et al. (1996, 2007): ITE Land Classification references
- Field methodologies:
  - Countryside Survey Habitat Mapping Methodology (CS Technical Report No.1/07)