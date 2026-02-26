# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Overview
- Dataset underpinning assessment of UK habitat exposure to climate change and evaluation of how well current plant monitoring schemes capture exposure gradients (as discussed in Wilson & Pescott, 2023).
- Produces spatially explicit 1 km gridded classifications of predicted Köppen-Geiger climate types for past and future periods, supporting environmental health monitoring and policy scrutiny.

## Data collection and generation
- Historical/observed climate data: HadUK-Grid (monthly precipitation; max, min, mean temperatures) at 1 x 1 km.
- Normal period: 1961–1990; other periods use long-term annual means.
- Future projections: UKCP18 Local (2.2 km) data for 2021–2040 and 2061–2080, using 12 convection-permitting simulations; ensemble mean used due to closer alignment with observed patterns.
- Spatial harmonization: UKCP18 Local data resampled to 1 km to match HadUK-Grid.
- Area exclusion: Shetland region around the dataset edge excluded due to unreliability.

## Climate classification framework
- Classification basis: Köppen-Geiger climate types (Beck et al., 2018; Peel et al., 2007) applied to UK 1 km grid cells.
- Periods considered: up to 2019 (historic) and future periods (2021–2040, 2061–2080).
- Classification rules: implemented per Table S1; climate types encoded with discrete categories.
- Coding and metadata: GeoTIFF files alongside a lookup CSV (kgClimateTypeRasterLookup.csv) describing codes (e.g., Cfa, Cfb, Dfb, ET, etc.) and their numeric raster codes.
- Documentation: Table S2 provides descriptions and GeoTIFF coding for each climate type.

## Data structure and outputs
- Primary outputs: maps (GeoTIFF) of predicted Köppen-Geiger climate classification for UK and Isle of Man at 1 km resolution.
- Data captions: values are discrete climate category labels per grid cell.
- Supporting materials: Table S1/S2 and kgClimateTypeRasterLookup.csv; analyses and methods detailed in Wilson & Pescott (2023) and supplementary info.

## Quality control and methods
- Data sources: HadUK-Grid for historical data; UKCP18 Local for future projections.
- Model ensemble approach: use 12 UKCP18 Local simulations; ensemble mean selected for closer alignment to observed patterns.
- Spatial handling: resampling from 5 x 5 km to 1 km via bilinear interpolation; careful handling of edge reliability (Shetland excluded).
- Analysis environment: all analyses performed in R; methodological details available in Wilson & Pescott (2023).

## Relevance for monitoring frameworks and policy
- Provides a transparent, reproducible set of climate-type rasters to monitor exposure gradients across habitats.
- Accompanied by explicit metadata and coding schemes, aiding data governance, reuse, and communication of results to stakeholders.
- Facilitates evaluation of monitoring coverage against climate exposure, informing data needs and monitoring design.
- Highlights practical considerations for policy use: data resolution harmonization, ensemble-based projections, and edge effects in remote regions.

## Accessibility, metadata, and governance considerations
- Outputs include openly documentable GeoTIFFs and a CSV lookup file, with supplementary tables outlining climate types and codes.
- Rich metadata supports verification and interpretation, aligning with data-sharing and governance best practices.
- Noted barriers for practitioners: reliance on UKCP18 Local which is limited to certain scenarios/regions; requirement to manage data at 1 km from coarser inputs; edge reliability near dataset boundaries.

## References
- Beck, H. E. et al. (2018). Present and future Köppen-Geiger climate classification maps at 1-km resolution. Scientific Data, 5, 180214.
- Hollis, D. et al. (2019). HadUK-Grid: A new UK dataset of gridded climate observations. Geoscience Data Journal, 6(2), 151-159.
- Kendon, E. et al. (2021); Lowe, J. A. et al. (2018); Met Office (2019). UKCP Local datasets and reports.
- Peel, M. C. et al. (2007). Updated world map of the Köppen-Geiger climate classification.
- Wilson, O. J. & Pescott, O. L. (2023). Assessing the exposure of UK habitats to 20th- and 21st-century climate change, and its representation in ecological monitoring schemes. Journal of Applied Ecology.