# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Aim and scope
- Supports assessment of UK habitat exposure to climate change.
- Evaluates how well current UK plant monitoring schemes cover climate exposure gradients (see Wilson & Pescott 2023).

## What the data are
- Spatially explicit, 1 km gridded maps of predicted Köppen-Geiger climate types for the UK and Isle of Man.
- Based on both past observed climate data and future modeled projections.
- Used to underpin the Wilson & Pescott (2023) study.

## Data sources and collection methods
- Historical/current climate: HadUK-Grid — monthly precipitation and max/min/mean temperatures at 1 x 1 km.
- Baseline normalization: 1961–1990 period used as a climate normal; other periods averaged to create long-term means.
- Future projections: UKCP18 Local (2.2 km) data for 2021–2040 and 2061–2080 at 5 x 5 km, resampled to 1 km via bilinear interpolation (12-member ensemble mean chosen for better alignment with observed patterns).
- Emissions context: UKCP18 Local projections available under RCP8.5; little difference between scenarios for near-term changes.
- Geographic exclusion: Shetland area excluded due to proximity to model domain edge and reliability concerns.

## Climate classification and data processing
- Classification system: Köppen-Geiger types per definitions adapted from Beck et al. 2018 (Table S1) applied to each 1 km cell.
- Output codings: GeoTIFF files encode climate categories; supplementary codes and lookups provided (Table S2; kgClimateTypeRasterLookup.csv).

## Output products
- GeoTIFF rasters: 1 km climate classification maps for the UK and Isle of Man across time periods.
- Lookup table: kgClimateTypeRasterLookup.csv linking climate type codes to descriptions and numeric codes.

## Quality, validation, and limitations
- Dual data sources (HadUK-Grid and UKCP18 Local) with ensemble averaging to improve reliability.
- Exclusion of unreliable northern edge (Shetland) due to model boundary issues.
- Analyses performed in R; methodological details available in Wilson & Pescott (2023).

## Data structure and access
- Supplied GeoTIFF files containing 1 km Köppen-Geiger classifications.
- Associated CSVs provide climate-type code mappings (S2) and table-based descriptions (S1/S2 references in documentation).

## References and context
- Becke et al. 2018; Hollis et al. 2019; Kendon et al. 2021; Lowe et al. 2018; Met Office 2019; Peel et al. 2007; Wilson & Pescott 2023.