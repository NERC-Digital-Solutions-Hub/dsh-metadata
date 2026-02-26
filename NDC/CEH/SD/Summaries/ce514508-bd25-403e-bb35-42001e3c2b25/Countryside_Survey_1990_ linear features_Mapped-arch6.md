# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

- Overview
  - National estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
  - Estimates are total lengths in metres for each linear feature type per 1km square per Land Class.
  - Note: there may be negative values in the LC2007 field due to the statistical model; treat these as zero.
  - Data are stored with fields including identifiers, geometry, land class codes, survey year, area, and length estimates for each feature type.

- Data structure and key fields
  - FID: Feature ID (autonumber)
  - LC2007: ITE Land Class (numeric)
  - LC2007_COD: ITE Land Class (text code)
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class (00s ha)
  - LF_1: Hedge length estimate per 1km square in metres
  - LF_3: Wall length estimate per 1km square in metres
  - LF_4: Line of trees/shrubs/relict hedge/fence length in metres
  - LF_5: Line of trees/shrubs/relict hedge length in metres
  - LF_6: Bank/grass strip length in metres
  - LF_7: Fence length in metres
  - LFTOTAL: Total length of linear features (metres)
  - Shape_Length and Shape_Area: geometry-related metrics

- Linear features and definitions
  - _1 = Hedges: A managed line of woody vegetation; can accompany other features
  - _3 = Wall: Built stone/manufactured wall; may include fences or banks/grass strips
  - _4 = Line of trees/shrubs/relict hedge/fence: Line of natural-shaped trees/shrubs, may include banks/grass strips
  - _5 = Line of trees/shrubs/relict hedge: Line of natural-shaped trees/shrubs, includes avenues
  - _6 = Bank/grass strip: Earth/stone bank or grass strip, with/without fence
  - _7 = Fence: Permanent post/wire/rail structure; may be alongside a grass strip, ditch, or stream
  - TOTAL: Total length of linear features

- Reporting and data processing notes
  - Hierarchical reporting: no double counting of multi-element features; hedges have precedence when co-occurring with walls or fences
  - Hedge feature is defined as any feature containing a hedge element; hedges may be alongside walls/fences, but lengths of walls/fences found with a hedge are not included in their totals

- Use limitations and acknowledgement
  - All use of Countryside Survey data must be acknowledged
  - Required acknowledgement: "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology" and “Countryside Survey © Database Right/Copyright NERC- Centre for Ecology & Hydrology. All rights reserved.”

- Access to further information and references
  - Countryside Survey Website: general overview and links to methodologies
  - Key reports:
    - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
    - Countryside Survey 1990: main report (Barr et al., 1993)
    - CS Technical Report No.4/07 (Scott, 2007) on statistical estimation
    - ITE Merlewood Land Classification references (various, Bunce et al.)
  - Relevant datasets and background materials available via listed URLs and publications