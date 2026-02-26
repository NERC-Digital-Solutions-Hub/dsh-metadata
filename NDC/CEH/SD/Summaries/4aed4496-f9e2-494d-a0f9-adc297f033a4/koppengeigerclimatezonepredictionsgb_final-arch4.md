# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

- Overview
  - Spatially explicit 1 km gridded predictions of Köppen-Geiger climate types for the UK and Isle of Man.
  - Based on both historical (observed) and future (modelled) climate data.
  - These predictions underpin assessment of habitat exposure to climate change and evaluation of current UK plant monitoring schemes (as discussed in Wilson & Pescott, 2023).

- Data sources and collection
  - Historical periods (up to 2019): HadUK-Grid monthly precipitation and temperature data at 1 x 1 km resolution; 1961-1990 used as the climate normal; other periods averaged to create long-term means.
  - Future periods: UKCP18 Local data (2.2–5 km resolution, depending on source) for 2021-2040 and 2061-2080, resampled to 1 km to match HadUK-Grid; 12-member ensemble mean used (convection-permitting model) due to closer alignment with observed patterns.
  - Geographic scope: UK and Isle of Man; Shetland region excluded due to edge unreliability of UKCP18 Local data.

- Data processing and classification
  - 1 km grid squares classified by Köppen-Geiger climate types using definitions adapted from Beck et al. (2018) and Peel et al. (2007).
  - 5 x 5 km UKCP18 Local data resampled to 1 km via bilinear interpolation to align with HadUK-Grid.
  - All analyses conducted in R; methodological details available in Wilson & Pescott (2023).

- Data products and structure
  - GeoTIFF files: maps of Köppen-Geiger climate classification at 1 km for the UK and Isle of Man.
  - Metadata and lookups:
    - kgClimateTypeRasterLookup.csv provides mappings between GeoTIFF codes and climate type descriptions.
    - Table S2 describes climate type codes (e.g., Cfa, Cfb, Dfb, ET) and their numeric GeoTIFF codes.
    - Table S1 provides climate type descriptions and criteria; Table S2 provides final numeric codes for each type.
  - Output purpose: discrete climate category values per 1 km grid square, enabling spatial analysis of exposure gradients.

- Quality control and limitations
  - Dual-sourced data: HadUK-Grid for historical and UKCP18 Local for future predictions; ensemble mean used to improve reliability.
  - Excluded areas: Shetland area removed due to model reliability concerns near dataset boundary.
  - Emissions scenario note: UKCP18 Local data provided for worst-case (RCP8.5); differences between scenarios in the near term are relatively small.
  - Limitations acknowledged: regional data gaps, potential disparities in data quality and metadata across sources, and reliance on interpolation for downscaling.

- Time coverage
  - Historical periods: early 20th century (1901-1930), mid-late 20th century (1961-1990), and last decade (2010-2020).
  - Future periods: 2021-2040 and 2061-2080.

- Usage and implications for data leadership
  - Provides a standardized, gridded climate-type framework to assess habitat exposure to climate change and to evaluate alignment with ecological monitoring schemes.
  - Emphasizes data provenance, reproducibility (R-based workflow), and the importance of metadata (Table S1/S2, kgClimateTypeRasterLookup.csv) for discoverability and reuse.
  - Highlights governance considerations: sourcing from multiple datasets, handling of projections and downscaling, and clear documentation of exclusions and assumptions for cross-organization collaboration.

- References and data provenance
  - Core methodological and validation references include Beck et al. (2018), Hollis et al. (2019), Kendon et al. (2021), Lowe et al. (2018), Met Office (2019), Peel et al. (2007), and Wilson & Pescott (2023).