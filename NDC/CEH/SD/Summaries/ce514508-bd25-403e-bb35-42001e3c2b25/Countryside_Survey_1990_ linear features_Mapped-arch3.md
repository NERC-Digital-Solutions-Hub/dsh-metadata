# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview and purpose
- Provides national estimates of landscape linear feature stock for 1990, calculated using the 2007 ITE Land Classification.
- Estimates are total lengths in metres for each linear feature type per 1 km square per Land Class.
- Derived from Countryside Survey results (UK, 2007); includes guidance on how to treat anomalous values due to the statistical model.

## Data content and measurement
- Features measured: six major linear feature types
  - Hedges
  - Wall
  - Line of trees/shrubs/relict hedge/fence
  - Line of trees/shrubs/relict hedge
  - Bank/grass strip
  - Fence
- Reporting metric: length estimates per 1 km square within each land class; totals summarized as LFTOTAL.
- Special reporting rule: when multiple features co-occur, reporting is hierarchical to avoid double counting; hedges have precedence and their stock ensures walls/fences are not double-counted where hedge is present.
- Data quality note: LC2007 values may include negative values from the statistical model; treat such negatives as zero.
- Metadata fields (selected):
  - FID: Feature ID (autonumber)
  - LC2007: ITE Land Class (numeric)
  - LC2007_COD: ITE Land Class (text code)
  - CSYEAR: Year of survey
  - LCAREA: Total area of relevant Land Class
  - LF_1, LF_3, LF_4, LF_5, LF_6, LF_7: lengths of specific features (metres per 1 km square per land class)
  - LFTOTAL: Total length of linear features
  - Shape_Length, Shape_Area: geometry metrics

## Data structure, reporting, and usage
- Structure supports reporting results in multiple ways by combining class codes; designed to avoid double counting of multi-element features.
- Hedgerows are treated as ecologically important and policy-relevant; when hedges coexist with walls or fences, hedge totals are reported while overlaps with walls/fences are not double-counted.
- Use case for monitoring frameworks: enables assessment of landscape connectivity, hedgerow extent, and changes over time to inform policy decisions and target setting.

## Data quality, limitations, and governance
- Acknowledgement and copyright: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all uses must include the specified acknowledgement and copyright notice.
- Barriers and considerations for policy monitoring:
  - Potential data gaps or gaps in metadata that hinder verification or reuse.
  - Need for data transformation to integrate with other datasets.
  - Public sharing requirements for underlying data can be a barrier to reuse in some contexts.
  - Ensuring data remains up to date and governance mechanisms are in place for storage, sharing, and updates.
- Documentation and references provide methodological background (including the 2007 Land Classification and statistical reporting).

## Access, usage rights, and references
- Countryside Survey website provides general project overview and links to methodologies and documentation.
- Key references:
  - Countryside Survey: UK Results from 2007 (Carey et al., 2008)
  - Countryside Survey 1990: main report (Barr et al., 1993)
  - CS Technical Report No.4/07 Statistical Report (Scott, 2007)
  - ITE Land Classification of Great Britain 2007 (Bunce et al., 2007)
  - Foundational field methods and land classification literature (various cited works)
- Usage rights: data require acknowledgement as per the provided notice; all copies/publications/presentations must credit Countryside Survey data owned by NERC-CEH.