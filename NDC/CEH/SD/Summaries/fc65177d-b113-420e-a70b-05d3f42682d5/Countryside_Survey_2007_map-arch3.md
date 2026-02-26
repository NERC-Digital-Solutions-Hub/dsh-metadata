# Dataset Documentation

## Purpose and scope
- Provides national estimates of landscape linear feature stock for 2007, calculated using the 2007 ITE Land Classification.
- Estimates are total lengths (in metres) per 1 km square per land class; negative values should be treated as zero.
- Data supports reporting and analysis of hedges, walls, fences, and related linear features to inform environmental monitoring and policy decisions.

## Data structure and content
- Core fields include:
  - FID, Shape (geometry), LC2007 (numeric land class), LC2007_COD (text code), CSYEAR (survey year), LCAREA (area of land class), Shape_Length, Shape_Area.
  - LF_1 to LF_7: length estimates for specific linear features (e.g., hedges, walls, lines of trees/shrubs, banks/grass strips, fences) reported per 1 km square per land class.
  - LFTOTAL: total length of linear features.
- Reporting uses a hierarchical class system with no double counting for multi-element features.
- Six major feature types:
  - Hedge (_1)
  - Wall (_3)
  - Line of trees/shrubs/relict hedge/fence (_4)
  - Line of trees/shrubs/relict hedge (_5)
  - Bank/grass strip (_6)
  - Fence (_7)
  - TOTAL: total length of linear features
- Important reporting rule: hedges take precedence; if a hedge exists alongside other features, hedge lengths are reported, and associated wall/fence lengths are not double-counted.

## Feature definitions and reporting
- Hedges (_1): managed lines of woody vegetation; may accompany other features.
- Walls (_3): stone/manufactured walls, possibly with fences or banks/grass strips.
- Lines of trees/shrubs/relict hedge/fence (_4): lines with natural-shaped trees/shrubs; may include banks/grass strips.
- Lines of trees/shrubs/relict hedge (_5): natural-shaped lines; may include avenues and banks/grass strips.
- Bank/grass strip (_6): earth/stone bank or grass strip, with or without a fence.
- Fence (_7): permanent post/wire/rail structure, may be alongside a grass strip, ditch, or stream.
- TOTAL: aggregate length across all linear features.

## Data quality, metadata, and processing
- During field survey, results are captured as detailed codes enabling multiple reporting formats.
- The dataset uses a consistent coding scheme to support flexible reporting across land classes and feature types.
- Negative values are to be treated as zero to maintain meaningful totals.

## Use limitations and governance
- Use must acknowledge Countryside Survey data owned by NERC - CEH; includes copyright/DB rights notice on copies, publications, and presentations.
- Data sharing and accessibility may be constrained by metadata quality and the need to publicly share underlying datasets.
- Data may require transformation or cleaning to meet specific reporting standards or software requirements.

## Provenance and references
- Countryside Survey data and methodology references:
  - Carey et al. (2008) Countryside Survey: UK Results from 2007.
  - Scott (2007) CS Technical Report No.4/07: Statistical Reporting of national estimates from 1 km survey squares.
  - Bunce et al. (1996, 2007): ITE Land Classification of Great Britain; supporting classification framework.
  - CS Technical Report No.1/07: Field Mapping Handbook.
- ITE Land Classification 2007 dataset details and vector data descriptions.

## Access and further information
- Countryside Survey website: general project overview and links to methodologies and documents.
- Referenced metadata and technical reports for background and methodology details.