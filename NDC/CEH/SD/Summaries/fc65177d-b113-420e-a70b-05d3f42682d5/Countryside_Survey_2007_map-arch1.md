# Dataset Documentation

## Overview
- Provides national estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
- Results are total lengths (metres) for each linear feature type per 1 km square per land class; negative values are to be treated as 0.
- Source: Countryside Survey data © NERC - Centre for Ecology & Hydrology.

## Data structure and key variables
- FID: Object ID; default autonumber.
- Shape: Geometry (with Shape_Length and Shape_Area describing feature geometry).
- LC2007: Numeric ITE Land Class (2007).
- LC2007_COD: Text code for ITE Land Class.
- CSYEAR: Year of survey (2007 in this dataset).
- LCAREA: Total area of relevant Land Class (00s ha).
- LF_1: Hedges (metres per 1 km square per land class).
- LF_3: Wall (metres per 1 km square per land class).
- LF_4: Line of trees/shrubs/relict hedge/fence (metres per 1 km square per land class).
- LF_5: Line of trees/shrubs/relict hedge (metres per 1 km square per land class).
- LF_6: Bank/grass strip (metres per 1 km square per land class).
- LF_7: Fence (metres per 1 km square per land class).
- LFTOTAL: Total length of linear features (metres per 1 km square per land class).
- Shape_Length, Shape_Area: Geometry descriptors.
- Units for LF_x and LFTOTAL: metres per 1 km square; per land class.

## Linear feature codes and reporting logic
- Codes: _1 = Hedges; _3 = Wall; _4 = Line of trees/shrubs/relict hedge/fence; _5 = Line of trees/shrubs/relict hedge; _6 = Bank/grass strip; _7 = Fence; TOTAL = Total length of linear features.
- A hedge feature is any feature containing a hedge element and may co-occur with other features (wall, fence).
- Hierarchical reporting: six major feature types; no double counting of multi-element features.
- Hedge precedence: when hedges are present with other features, hedge lengths are reported with precedence; stocks for walls and fences exclude lengths found with hedges.

## Data quality, limitations, and usage notes
- Negative values in data should be treated as 0.
- Use Limitation: All Countryside Survey data must be acknowledged in any copies, publications, or presentations.
- Acknowledgement text required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; Countryside Survey © NERC Centre for Ecology & Hydrology. All rights reserved.

## Use and provenance references
- Countryside Survey Website: general project overview and documentation.
- Key references:
  - Carey et al. (2008): Countryside Survey UK Results from 2007.
  - Scott (2007): CS Technical Report No.4/07 Statistical Report (how national estimates are generated from 1 km squares).
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain; ITE Land Classification 2007 vector dataset.
  - CS Technical Report No.1/07: Field Mapping Handbook.
- Data and reports are accessible via provided URLs and CEH/CSH metadata resources.