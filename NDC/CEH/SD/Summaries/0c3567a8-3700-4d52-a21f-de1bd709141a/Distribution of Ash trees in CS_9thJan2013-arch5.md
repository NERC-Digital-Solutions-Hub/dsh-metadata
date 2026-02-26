# Distribution of Ash trees ( Fraxinus excelsior ) in Countryside Survey data

## Overview
- A detailed account of the extent and distribution of ash trees in Great Britain using Countryside Survey (CS) data, with emphasis on ash in woodlands under 0.5 ha, individual trees outside woodland, hedgerows and other linear features, and vegetation plots.
- Aims to inform understanding of ash distribution in the context of ash dieback and to create landscape-scale products from CS datasets.

## Data scope and purpose
- Purpose: quantify extent, abundance, and distribution of Fraxinus excelsior to assess potential impacts of ash dieback and to aid monitoring and modelling.
- Scope: national estimates for GB; breakdown by area (woodlands <0.5 ha), individual trees outside woodland, hedgerows/linear features, and vegetation plots.
- Data sources: Countryside Survey 2007 data, with overlap/consistency checks against the National Forestry Inventory (NFI) to avoid duplication; CS focuses on current land cover rather than stocked woodland status.

## Datasets and data types
- Areas (woodlands <0.5 ha)
  - Estimated areal extent of ash within small broadleaved woodlands (<0.5 ha): 38.51 thousand hectares.
  - Distribution by country and landscape context (fields, hedgerows, river corridors, hedges).
- Individual trees outside woodland
  - Estimated 2.2 million individual ash trees outside woodlands in GB; majority in England.
  - Distribution maps by landclass show concentration patterns; veteran trees (aged >2 m DbH indicator) recorded with added contextual data.
- Woody linear features (hedgerows and lines of trees)
  - Total ash-containing woody linear features: 98.9 thousand km across GB; predominantly in England (hedgerows ~66.3 thousand km; lines of trees ~19.7 thousand km; belts negligible).
  - Ash as a hedgerow component and as standard hedgerow trees.
- Vegetation plots
  - Occupancy data across plot types (boundary, hedge diversity plots, hedge plots, arable margins, roadside, streamside, field plots, small habitat patches).
  - Ash present in a substantial portion of hedgerow-related plots (e.g., 30% in hedge plots, 23.8% mean cover in boundary plots, ~24.8% in streamside plots).

## Methods and data processing
- Sampling framework
  - CS uses stratified random sampling of 1 km squares across GB, aligned with ecological landclasses to enable scaling to national estimates.
  - Data recorded at multiple spatial components: areas, individual trees (point data), linear features, and vegetation plots.
- Areas and national estimates
  - Use mid-point percentages of cover bands (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%) to derive area estimates per landclass and sum to GB totals.
  - Excluded woodland parcels covered by NFI to avoid duplication; CS-based areas reflect current land cover.
- Individual trees outside woodland
  - Counted as point features in 1 km squares; included small clumps if below the Minimum Mappable Unit (mmu) of 20 m × 20 m.
  - Veteran trees recorded with additional attributes (epiphytes, dead wood, hollow trunk).
  - Spatial analysis overlays individual trees with linear data to identify hedgerow trees.
- Woody linear features
  - Recorded as hedgerows (natural shape) and belts/lines (including belts of trees or scrub).
  - For ash, estimation used proportion bands from vegetation and D plots to derive mean ash length per 1 km square, then scaled by landclass area to national totals.
  - Different recording approaches for natural vs. unnatural shapes; supplementary data from D plots used to refine hedgerow ash estimates.
- Vegetation plots
  - Plots include linear (1 × 10 m along features) and area plots (2 × 2 m and nested 14 m² plots) within each 1 km square.
  - Change analysis uses a change index to assess occupancy shifts between surveys, accounting for nested design.

## Key findings
- Areal extent and country patterns
  - Ash is the second most abundant tree species in small woodland patches (<0.5 ha) in GB (38.5 thousand ha), behind Oak.
  - England hosts the majority of ash in small woodlands (≈32.1 thousand ha); Scotland and Wales have substantially less.
- Individual trees outside woodland
  - Approximately 2.2 million individual ash trees outside woodlands; England ~1.8 million, Scotland ~148 thousand, Wales ~240 thousand.
  - Ash is the second most common species among individual trees.
- Hedgerows and linear features
  - Ash is the most common hedgerow tree species and a major component of hedgerows and lines of trees.
  - Ash-containing woody linear features total about 98.9 thousand km GB-wide, with the vast majority in England (hedgerows ~66.3 thousand km; lines of trees ~19.7 thousand km).
- Vegetation plots and distribution patterns
  - Ash occurs in about 30% of hedgerow plots; ash presence is also notable in boundary, roadside, streamside, and field plots, with mean shade/cover varying by plot type.
  - Increases in ash occupancy were detected on linear plots between 1978 and 2007, and in area plots between 1990 and 2007, indicating recent expansion in various landscape components.
- Spatial and temporal context
  - Maps provide indicative spatial patterns by landclass rather than precise pixel-level maps; a novel effort to produce landscape-scale products using CS data, complemented by LCM 2007 and, in the future, broader linear products integrating CS data with LiDAR and OS data.

## Outputs, maps, and limitations
- Outputs include national estimates by area, number of trees, and length of ash in linear features, plus distributional maps by landclass.
- Spatial explicitness
  - The study provides indicative maps rather than high-resolution pixel-level maps; overlay with Land Cover Map 2007 enables GB-scale estimation but not precise site-level mapping.
- Limitations and considerations
  - Differences between CS and NFI reporting (CS reflects current land cover; NFI reports stocked areas) necessitated overlap avoidance.
  - Not all factors driving ash distribution are modelled; data integration with climate, soil, and other drivers suggested for future modelling.

## Future work and data reuse
- Develop a monitoring protocol for ash diseases and tree health impacts within CS.
- Create a linear-product that scales from 1 km squares to GB using CS data, LIDAR, and Land Cover data.
- Extend analyses to correlate ash distribution with multiple explanatory variables (climate, soil, deposition) and to explore associations with other species.
- Potential complementarity with FC woodland surveys by extending CS measurements (e.g., DbH, veteran trees) where appropriate to avoid duplication.
- Explore integration with GB woodland survey datasets to better attribute distribution changes to drivers and to model future ash dieback scenarios.

## Data quality, governance, and reuse notes
- Data collected under a national framework with standardized sampling and reporting to support comparisons over time.
- Data governance considerations include de-duplication with NFI data, consistent species identification, and clear documentation of plot and survey methodologies.
- The study demonstrates how CS datasets can be transformed into landscape-scale products for ecological monitoring and disease impact assessment, with potential for integration into broader data governance and sharing initiatives.