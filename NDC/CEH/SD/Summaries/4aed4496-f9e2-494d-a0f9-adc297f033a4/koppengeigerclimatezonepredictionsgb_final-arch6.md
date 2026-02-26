# Köppen-Geiger 1 km climate classification predictions for the UK, 19012080 metadata

## Overview
- Provides spatially explicit 1 km gridded classifications of predicted Köppen-Geiger climate types for past observed and future modeled climates.
- Data underlie assessments of UK habitat exposure to climate change and the representation of these gradients in plant monitoring schemes (linked to Wilson & Pescott 2023).
- Outputs support the paper by Wilson & Pescott (2023).

## Data collection and generation methods
- Historic/past periods (up to 2019): HadUK-Grid data for monthly precipitation and max/min/mean temperatures at 1 x 1 km. 1961–1990 used as a climate normal; other periods aggregated annually to long-term means.
- Future periods (2021–2040 and 2061–2080): UKCP18 Local data at 5 x 5 km resampled to 1 km via bilinear interpolation to match HadUK-Grid.
- UKCP18 Local dataset used is 2.2 km convection-permitting, with the 12-member ensemble mean selected for closer alignment with observed patterns.
- All grid squares in the UK and Isle of Man were classified into Köppen-Geiger climate types per the criteria in Table S1 (adapted from Beck et al., 2018).

## Climate type definitions and outputs
- Climate types described using the Köppen-Geiger scheme (e.g., Cfa, Cfb, Dsb, ET, etc.), including temperature and precipitation criteria (e.g., hottest month > 10°C, precipitation thresholds, summer/winter patterns).
- Recorded outputs are discrete climate categories per grid cell, not continuous values.
- Final classifications are represented in GeoTIFF files; a corresponding kgClimateTypeRasterLookup.csv provides the numeric codes for each climate type (and a Table S2 detailing codes and descriptions).

## Quality control and data handling
- Two primary data sources: HadUK-Grid (historical/contemporary) and UKCP18 Local (future projections).
- Ensemble mean from UKCP18 Local used for future projections due to better alignment with observed climate patterns.
- Exclusion: area around Shetland excluded due to unreliable positioning near dataset boundary.
- All analyses and manipulations conducted in R; methodological details available in Wilson & Pescott (2023).

## Data structure and accessibility
- Supplied outputs are GeoTIFF maps of the 1 km Köppen-Geiger climate classifications for the UK and Isle of Man.
- Supporting materials include:
  - Table S1 (climate type definitions and criteria)
  - Table S2 (descriptions of climate types and their numeric GeoTIFF codes)
  - kgClimateTypeRasterLookup.csv (mapping of climate types to codes)
- Usage relies on the dataset as described in the Wilson & Pescott (2023) methodology; see that paper for full methodological context.

## Temporal and spatial coverage
- Time periods covered:
  - Historical/contemporary: 1901–1930, 1961–1990, 2010–2020 (as snapshots for climate periods)
  - Future: 2021–2040 and 2061–2080
- Spatial resolution: 1 km grid cells across the UK and Isle of Man (with UKCP18 data upscaled to 1 km from 5 x 5 km).

## References and methodological context
- Key sources validating the approach and climate classifications:
  - Beck et al., 2018; Peel et al., 2007 (Köppen-Geiger classification framework)
  - Hollis et al., 2019 (HadUK-Grid)
  - Kendon et al., 2021; Lowe et al., 2018; Met Office, 2019 (UKCP18 Local)
  - Wilson & Pescott, 2023 (primary analysis using this dataset)