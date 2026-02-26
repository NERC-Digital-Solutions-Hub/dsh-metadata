# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1998 calculated using the 2007 ITE Land Classification; results are total lengths in metres for each linear feature type per 1km square per Land Class.
- Negative values may appear in the LC2007 column due to the statistical model; treat these as zero.
- Data are organised per 1km square and Land Class, with geometric shape information included.

## Data structure and fields
- FID: Object ID; Description: Feature ID (autonumber).
- Shape: Geometry.
- LC2007: Double; ITE Land Class (numeric) (Bunce et al., 2007).
- LC2007_COD: Text; ITE Land Class (text code) (Bunce et al., 2007).
- CSYEAR: Number; Year of survey.
- LCAREA: Number; Total area of relevant Land Class (00s ha).
- LF_1: Number; Hedges (metres per 1km square per land class).
- LF_3: Number; Wall (metres per 1km square per land class).
- LF_4: Number; Line of trees/shrubs/relict hedge/fence (metres per 1km square per land class).
- LF_5: Number; Line of trees/shrubs/relict hedge (metres per 1km square per land class).
- LF_6: Number; Bank/grass strip (metres per 1km square per land class).
- LF_7: Number; Fence (metres per 1km square per land class).
- LFTOTAL: Number; Total length of linear features (metres per 1km square per land class).
- Shape_Length: Number; Length of Land Class shape.
- Shape_Area: Number; Area of Land Class (square metres).

- Linear features codes:
  - _1 = Hedge
  - _3 = Wall
  - _4 = Line of trees/shrubs/relict hedge/fence
  - _5 = Line of trees/shrubs/relict hedge
  - _6 = Bank/grass strip
  - _7 = Fence
  - TOTAL = Total length of linear features

## Feature reporting and hierarchy
- Results are reported using a six-type hierarchical system; there is no double counting of multi-element features.
- A hedge feature is considered when present and takes precedence; estimates for walls and fences do not include portions that are part of hedges.

## Use limitations
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement and copyright notice requirements apply to all copies, publications, and presentations.
- Acknowledgement statement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey ©; All rights reserved.
- Data are sourced from the Countryside Survey project and related documentation and may reference additional methodological reports.

## Access and references
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Key publications and methodologies (examples):
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - Accounting for nature: assessing habitats in the UK countryside (Haines-Young et al., 2000)
  - CS Technical Report No.4/07 Statistical Report (Scott, 2007)
  - ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
  - ITE Merlewood Land Classification (1996)
- Data and methodological references provide background for how national estimates are generated from 1km survey squares and how Land Classification is applied.