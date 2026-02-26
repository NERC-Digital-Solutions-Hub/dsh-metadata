# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Overview
- Dataset underpinning assessment of UK habitat exposure to climate change.
- Spatially explicit 1 km gridded classifications of predicted Köppen-Geiger climate types (based on past observed and future modelled climate data).
- Supports the Wilson & Pescott (2023) study on climate exposure and monitoring coverage.

## Collection and generation methods
- Historic periods (up to 2019): HadUK-Grid data (monthly precipitation; max, min, mean temperatures) at 1 x 1 km resolution.
  - 1961–1990 used as a climate normal; other periods averaged to form long-term means.
- Future periods: UKCP18 Local data (2021–2040; 2061–2080) at 5 x 5 km, resampled to 1 x 1 km using bilinear interpolation.
- UKCP18 Local dataset used is the 2.2 km version; 12 simulations of a convection-permitting model; 12-member ensemble mean used for best agreement with observed patterns.
- Classification: 1 km grid squares assigned Köppen-Geiger climate types per definitions in Table S1 (Beck et al., 2018; Peel et al., 2007).
- Climate type coding: Table S2 provides the mapping of climate types (e.g., Cfa, Cfb, Dfb, ET, etc.) to descriptions and numeric codes; GeoTIFF files encode the climate type category, with a separate kgClimateTypeRasterLookup.csv for lookup.
- Temporal scope includes historical periods (1901–1930, 1961–1990, 2010–2020) and future periods (2021–2040, 2061–2080).

## Data structure and formats
- Supplied GeoTIFF files: maps of Köppen-Geiger climate classification at 1 km resolution for the UK and Isle of Man.
- Accompanying metadata:
  - kgClimateTypeRasterLookup.csv: numeric codes and descriptive mappings for climate types.
  - Table S1 and Table S2 referenced for detailed climate type criteria and coding.
- All analyses and data manipulations conducted in R.

## Quality control and limitations
- Data sources:
  - Historical/contemporary: HadUK-Grid (gridded observations).
  - Future predictions: UKCP18 Local (2.2 km) ensemble simulations; use of 12-member ensemble mean.
- Geographic coverage caveat:
  - Shetland area excluded due to proximity to model domain edge and unreliability.
- General limitations:
  - UKCP18 Local data are only available under the RCP8.5 scenario; however, changes in near-term predictions are similar across scenarios.
  - 5 km to 1 km resampling via bilinear interpolation may introduce interpolation artifacts.
  - For the dataset, climate types are discrete categories rather than continuous variables.
- Documentation and provenance:
  - Methods and justification provided in Wilson & Pescott (2023); supplementary material elaborates on classifications and data handling.
  - All components linked to established climate classification frameworks (Beck et al., Peel et al.).

## Usage notes and context
- Purpose-built for assessing exposure of UK habitats to climate change and evaluating coverage of plant monitoring schemes against climate exposure gradients.
- The dataset forms a basis for downstream analyses in ecology and conservation planning, with explicit reference to the associated publication and supplementary materials.
- Users should consult Table S1/S2 and the Wilson & Pescott (2023) paper for full methodological details and caveats.

## Related references
- Beck, H. E. et al. 2018. Present and future Köppen-Geiger climate classification maps at 1-km resolution. Scientific Data.
- Hollis, D. et al. 2019. HadUK-Grid: A new UK dataset of gridded climate observations. Geoscience Data Journal.
- Kendon, E. et al. 2021; Lowe, J. A. et al. 2018; Met Office 2019. UKCP Local data references.
- Peel, M. C. et al. 2007. Updated world map of the Köppen-Geiger climate classification.
- Wilson, O.J. & Pescott, O.L. 2023. Assessing exposure of UK habitats to climate change (Journal of Applied Ecology).