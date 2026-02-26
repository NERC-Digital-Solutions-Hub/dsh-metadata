# Dataset Documentation

## Overview
- Purpose: National estimates of landscape linear feature stock for 1990 calculated using the 2007 ITE Land Classification. Provides total lengths (in metres) of each linear feature type per 1km square and land class.
- Key caution: There may be negative values in LC2007; treat these as zero.
- Projections and scope: Based on the Countryside Survey, with results reported using a hierarchical six-type system. No double counting of multi-element features; hedges are prioritized in reporting when co-occurring with other feature types.

## Dataset Structure and Fields
- FID: Object ID (and Description: Feature ID, autonumber)
- Shape: Geometry (spatial data)
- LC2007: Double (ITE Land Class numeric)
- LC2007_COD: Text (ITE Land Class code)
- CSYEAR: Number (Year of survey)
- LCAREA: Number (Total area of relevant Land Class, in hectares)
- LF_1: Number (Hedges) – metres per 1km square per land class
- LF_3: Number (Wall) – metres per 1km square per land class
- LF_4: Number (Line of trees/shrubs/relict hedge/fence) – metres per 1km square per land class
- LF_5: Number (Line of trees/shrubs/relict hedge) – metres per 1km square per land class
- LF_6: Number (Bank/grass strip) – metres per 1km square per land class
- LF_7: Number (Fence) – metres per 1km square per land class
- LFTOTAL: Number (Total length of linear features) – metres per 1km square per land class
- Shape_Length: Number (Length of Land Class shape)
- Shape_Area: Number (Area of Land Class in square metres)

## Feature Types and Reporting Rules
- Linear features include: 
  - _1 Hedge
  - _3 Wall
  - _4 Line of trees/shrubs/relict hedge/fence
  - _5 Line of trees/shrubs/relict hedge
  - _6 Bank/grass strip
  - _7 Fence
  - TOTAL (Total length)
- Reporting framework:
  - Six major feature classes with a hierarchical reporting system.
  - Hedge elements are given precedence when present with other features (e.g., hedges included without double counting walls/fences that occur with hedges).
  - No double counting of multi-element features; lengths of walls/fences do not include those that are part of a hedge.

## Data Provenance and Methodology
- Source: Countryside Survey field survey data from 1990, interpreted through the ITE Land Classification (1990/2007 framework).
- Method: National estimates are derived from 1km survey squares and then classified by Land Class using the 2007 ITE scheme.
- Documentation and technical references:
  - Scott (2007) CS Technical Report No.4/07 – Statistical method for generating national estimates from 1km squares.
  - Bunce et al. (2007) ITE Land Classification 2007 dataset.
  - Additional background reports: Countryside Survey 1990 main report; Merlewood Land Classification overview; older field handbook references.

## Use Limitations and Licensing
- Acknowledgement required on all copies, publications, and presentations:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - "Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved."
- Access and distribution should follow the Countryside Survey guidelines and citations.

## Access, References, and Related Resources
- Countryside Survey Website: General overview and project documentation
  - http://www.countrysidesurvey.org.uk/
- Key publications and reports:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Barr et al. (1993) Countryside Survey 1990: main report
  - Scott (2007) CS Technical Report No.4/07 – Statistical methods
  - Bunce et al. (2007) ITE Land Classification 2007 vector dataset
  - Bar/Clarke et al. (various) Merlewood Land Classification references

## Notes for Data Stewards
- Metadata should clearly reflect the hierarchical reporting rules and the no-double-count principle.
- Ensure clarity on data lineage: field-coded survey data translated into the six major feature classes and per-land-class aggregations.
- Maintain notes on handling of negative LC2007 values and the requirement to treat them as zero.
- Preserve licensing and acknowledgement language in all distributed copies and publications.