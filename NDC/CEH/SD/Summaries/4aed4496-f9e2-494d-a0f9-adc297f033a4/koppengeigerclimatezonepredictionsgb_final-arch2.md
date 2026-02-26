# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Overview
- Provides spatially explicit 1 km gridded classifications of predicted Köppen-Geiger climate types for the UK and Isle of Man.
- Supports assessment of habitat exposure to climate change and evaluation of how well current UK plant monitoring schemes cover exposure gradients (as discussed in Wilson & Pescott, 2023).
- Classifications are based on both past observed and future modeled climate data to underpin the associated paper.

## Collection/generation methods
- Historic periods (up to 2019): Use HadUK-Grid monthly precipitation and temperature data at 1 km resolution; 1961–1990 used as climate normal; other periods averaged to create long-term means.
- Future periods (2021–2040 and 2061–2080): Use UKCP18 Local data at 5x5 km, resampled to 1 km via bilinear interpolation; 12 simulations from a convection-permitting model; ensemble mean used for consistency with observed patterns.
- Grid squares in the UK and Isle of Man classified into Köppen-Geiger types using criteria from Table S1 (adapted from Beck et al., 2018; Peel et al., 2007).
- Analyses and data manipulations conducted in R; see Wilson & Pescott (2023) for methodological details.

## Nature and units of recorded values
- Maps record discrete Köppen-Geiger climate category per 1 km grid square.
- GeoTIFF files encode climate types; a lookup CSV (kgClimateTypeRasterLookup.csv) provides mappings and final numeric codes.
- Examples of climate types include Cfa, Cfb, Cfc, Csa, Csb, Csc, Dfb, Dfc, ET, with descriptions (e.g., temperate with/without dry season, polar tundra) and associated code numbers for raster files.

## Quality control
- Two primary data sources: HadUK-Grid (historical/contemporary) and UKCP18 Local (future projections).
- HadUK-Grid: gridded observations from weather stations.
- UKCP18 Local: 12 simulations; ensemble mean chosen for closer alignment with observed patterns (2.2 km dataset used as context; worst-case scenario considered for certain periods).
- Temporal coverage: historical (1901–1930, 1961–1990, 2010–2020) and future projections (2021–2040, 2061–2080); Shetland area excluded due to model reliability limits.
- All analyses performed in R; detailed methodological notes available in Wilson & Pescott (2023) Supplementary Information.

## Details of data structure
- Supplied GeoTIFF files: 1 km climate-classification maps for the UK and Isle of Man.
- Supporting materials include a climate type lookup CSV (kgClimateTypeRasterLookup.csv) and summary tables (Table S2 with codes and descriptions; Table S1 for classification criteria).
- Numeric codes in GeoTIFFs correspond to specific Köppen-Geiger climate types; documentation enables straightforward reuse and integration with other monitoring data.

## References
- Key sources for methodology and data handling include Beck et al. (2018), Hollis et al. (2019), Kendon et al. (2021), Lowe et al. (2018), Met Office (2019), Peel et al. (2007), and Wilson & Pescott (2023).