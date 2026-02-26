# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
- Estimates are presented as total lengths (in metres) for each linear feature type per 1 km square per Land Class.
- Note: LC2007 may contain negative values due to the statistical model; treat negative values as zero.

## Data structure and fields (key GIS-relevant attributes)
- FID: Feature ID (auto-number)
- Shape: Geometry (spatial feature)
- LC2007: ITE Land Class (numeric)
- LC2007_COD: ITE Land Class (text code)
- CSYEAR: Year of survey
- LCAREA: Total area of relevant Land Class (00s ha)
- LF_1 to LF_7: Estimated length per 1 km square in each land class for:
  - LF_1: Hedges
  - LF_3: Wall
  - LF_4: Line of trees/shrubs/relict hedge/fence
  - LF_5: Line of trees/shrubs/relict hedge
  - LF_6: Bank/grass strip
  - LF_7: Fence
- LFTOTAL: Total length of linear features
- Shape_Length: Length of the Land Class shape
- Shape_Area: Area of Land Class

## Feature types and reporting rules
- Six major feature types are reported:
  - Hedge (_1)
  - Wall (_3)
  - Line of trees/shrubs/relict hedge/fence (_4)
  - Line of trees/shrubs/relict hedge (_5)
  - Bank/grass strip (_6)
  - Fence (_7)
  - TOTAL: Total length of linear features
- During field survey, linear landscape features were coded; reporting uses a hierarchical classification to avoid double counting.
- Key rules for map-based reporting:
  - No double counting of multi-element features (e.g., hedges may accompany walls or fences, but lengths of walls/fences found with hedges are not double-counted).
  - Hedges are given precedence in reporting when found alongside other features.
  - Walls and fences are reported excluding portions that are part of hedges.
- For GIS visualization, data are structured to allow per-Land Class, per-1km-square analysis with corresponding feature-type lengths.

## Use limitations and licensing
- All CS data usage must be acknowledged.
- Acknowledgement text: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Data are © NERC-Centre for Ecology & Hydrology. All rights reserved.

## Resources and references
- Countryside Survey Website: general project overview and documentation links
- 2007 UK Results from Countryside Survey (Carey et al., 2008)
- Supporting methodological and background documents:
  - Accounting for nature: assessing habitats in the UK countryside (Haines-Young et al., 2000)
  - CS Technical Report No. 4/07 (Scott, 2007): statistical derivation from 1 km squares
  - ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
  - Related Lands Classification and Field Handbook references

## Notes for GIS workflows
- Data are presented per 1 km square within Land Classes; use LC2007 and LC2007_COD to categorize map layers.
- When aggregating, apply the no-double-count principle to avoid inflating totals in combined maps.
- Be mindful of potential negative LC2007 values; convert to zero for visualizations and analyses requiring non-negative lengths.
- Include proper attribution in any published maps or reports.