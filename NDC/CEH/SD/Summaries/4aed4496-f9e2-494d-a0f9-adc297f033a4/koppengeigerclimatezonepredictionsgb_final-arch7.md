# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Overview
- Spatially explicit 1 km gridded classifications of predicted Köppen-Geiger climate types for the UK and Isle of Man.
- Based on past observed climate data (HadUK-Grid) and future modelled data (UKCP18 Local) to support assessment of habitat exposure to climate change and evaluation of UK plant monitoring scheme coverage (Wilson & Pescott, 2023).

## Data sources and generation
- Historic/present periods (up to 2019): HadUK-Grid monthly precipitation and temperature data (max, min, mean) at 1 km. 1961–1990 used as a climate normal; other periods averaged to long-term means.
- Future periods (2021–2040 and 2061–2080): UKCP18 Local data at 5x5 km, resampled to 1 km via bilinear interpolation. Uses the 12-simulation convection-permitting ensemble; the 12-member mean is used.
- Processing details:
  - Classify each 1 km grid square into Köppen-Geiger types using criteria from Table S1 (Beck et al., 2018; adapted).
  - Exclude the Shetland area due to unreliability near the model edge.
  - Analyses performed in R; see Wilson & Pescott (2023) for methodological details.

## Data products and structure
- GeoTIFF maps: 1 km Köppen-Geiger climate classification predictions for the UK and Isle of Man.
- Supporting lookup: kgClimateTypeRasterLookup.csv describing climate type codes and descriptions (and Table S2 mappings to GeoTIFF codes).
- Climate types included reflect categories where mean annual precipitation is at least 20× mean annual temperature (per classification scheme in Table S1).

## Climate type definitions and codes
- Uses Köppen-Geiger scheme with categories such as C (temperate), D (cold), ET (polar tundra), including subtypes defined by rainfall patterns, summer heat, and dryness.
- Each climate type is assigned a numeric code used in the GeoTIFFs (e.g., Cfa, Cfb, Dfb, ET, etc.).

## Quality control and limitations
- Dual data sources for validation: HadUK-Grid (historical) and UKCP18 Local (future projections).
- Temporal coverage: historical periods 1901–1930, 1961–1990, 2010–2020; future 2021–2040 and 2061–2080.
- Spatial considerations: Shetland excluded due to boundary unreliability.
- UKCP18 Local data are from the worst-case RCP8.5 scenario; marginal differences across scenarios for near-term projections are noted.

## Practical usage for GIS specialists
- Use the 1 km GeoTIFF climate maps to visualize and analyze shifting climate classes across space and time.
- Decode raster values with kgClimateTypeRasterLookup.csv to map climate categories to human-readable labels.
- Integrate with habitat, biodiversity, and monitoring datasets to assess exposure gradients and coverage of plant monitoring schemes.
- Reproducibility supported by explicit data sources, processing steps (including resampling), and R-based workflow referenced to Wilson & Pescott (2023).

## References
- Beck, H. E., et al. (2018). Present and future Köppen-Geiger climate classification maps at 1-km resolution.
- Hollis, D., et al. (2019). HadUK-Grid: A new UK dataset of gridded climate observations.
- Kendon, E., et al. (2021). Update to UKCP Local (2.2 km) projections.
- Lowe, J. A., et al. (2018). UKCP18 science overview report.
- Met Office (2019). UKCP18-Land report.
- Peel, M. C., Finlayson, B. L., & McMahon, T. A. (2007). Updated world map of the Köppen-Geiger climate classification.
- Wilson, O. J., & Pescott, O. L. (2023). Assessing exposure of UK habitats to climate change and monitoring representation.