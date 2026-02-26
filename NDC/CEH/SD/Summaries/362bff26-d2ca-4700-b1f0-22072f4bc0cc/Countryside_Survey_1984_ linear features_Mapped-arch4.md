# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- Provides national estimates of landscape linear feature stock for 1984, derived using the 2007 ITE Land Classification.
- Estimates are total lengths (in metres) for each linear feature type per 1km square per Land Class.
- Note: negative values may appear in the LC2007 column due to the statistical model; treat these as zero.
- Data are organized as vector GIS attributes with geometry, enabling spatial reporting and analysis.

## Data structure and content
- Core fields:
  - FID: Feature ID (autonumber)
  - LC2007: Land Class (numeric)
  - LC2007_COD: Land Class (text code)
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class (00s ha)
  - LF_1 to LF_7: lengths/indices for specific linear features in metres (per 1km square per land class)
  - LFTOTAL: Total length of linear features (metres)
  - Shape_Length: Length of the Land Class shape
  - Shape_Area: Area of Land Class
- Linear features categories:
  - _1: Hedge (managed hedgerows)
  - _3: Wall (stone/mortar walls; may include associated fences/banks)
  - _4: Line of trees/shrubs/relict hedge/fence
  - _5: Line of trees/shrubs/relict hedge
  - _6: Bank/grass strip
  - _7: Fence
  - TOTAL: Total length of linear features
- Reporting approach:
  - A hierarchical system reports six major feature types.
  - No double counting of multi-element features; a hedge element takes precedence when co-occurring with walls or fences.
  - Hedgerows are considered ecologically priority and reported first when encountered with other features.

## Feature definitions and reporting methodology
- Hedges (_1): Managed lines of woody vegetation; can accompany other features.
- Walls (_3): Built stone/manufactured walls; may include fences or banks/grass strips and/or lines of trees.
- Lines of trees/shrubs/relict hedge/fence (_4): Trees/shrubs with natural shapes, may include banks/grass strips.
- Lines of trees/shrubs/relict hedge (_5): Natural-shaped lines; can include avenues of trees and banks/grass strips.
- Bank/grass strip (_6): Earth/stone-faced bank or grass strip, with or without a fence.
- Fence (_7): Permanent post/rail/wire structures; may be together with grass strips, ditches, or streams.
- TOTAL: Sum of all linear features.
- The dataset integrates field-record codes to enable reporting in multiple configurations while preventing double-counting across feature types.

## Use limitations and governance
- Use of Countryside Survey data must be acknowledged in all copies, publications, and presentations.
- Required attribution: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” with copyright notice.
- All rights reserved; adhere to the specified acknowledgment wording on every use.

## Publications, references, and additional resources
- Countryside Survey project overview and methodologies available on the Countryside Survey Website.
- Key references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007
  - Scott (2007) CS Technical Report No.4/07 Statistical Report (how national estimates are derived from 1km squares)
  - Bunce et al. (1996, 2007) ITE Land Classification and related methodologies
- Dataset and related documents provide background, methodologies, and the linkage between land classification and linear feature reporting.

## Access and further information
- Countryside Survey Website: overview and links to relevant documents and methodologies
  - http://www.countrysidesurvey.org.uk/
- References for in-depth understanding:
  - CS Technical Reports and ITE Land Classification literature
- The documentation emphasizes discoverability, metadata, and links to broader data systems to support policy and practice.