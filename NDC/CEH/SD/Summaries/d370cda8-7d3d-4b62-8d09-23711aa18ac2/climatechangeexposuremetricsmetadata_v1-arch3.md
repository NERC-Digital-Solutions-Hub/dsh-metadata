# Assessing the exposure of UK habitats to 20th- and 21st-Century climate change

## Overview
- Data describe climate-change exposure of UK habitats and assess coverage by current UK plant monitoring schemes of these exposure gradients (as per Wilson & Pescott, 2023).
- Outputs are spatially explicit 1 km grids of a climate-change exposure index, derived from differences between observed historical and predicted future climates across four time-period comparisons.

## Time periods and comparisons
- Four comparisons between five time periods:
  - 1901–1930 vs 1961–1990
  - 1961–1990 vs 2010–2019
  - 2010–2019 vs 2021–2040
  - 2021–2040 vs 2061–2080

## Data sources and generation
- Climate data sources and processing:
  - HadUK-Grid: monthly precipitation and max/min/mean temperatures at 1 x 1 km resolution for historical and contemporary periods; 1961–1990 used as the normal baseline.
  - UKCP18 Local projections (2021–2040 and 2061–2080): 5 x 5 km resolution, downscaled to 1 km via bilinear interpolation; 12-simulation convection-permitting model ensemble; the 12-member ensemble mean used.
- Data harmonization:
  - UKCP18 Local data resampled to 1 km to match HadUK-Grid data.
  - For each period, 37 bioclimatic variables were generated from monthly climate data and then reduced using Principal Components Analysis (PCA).

## Climate exposure metric
- Exposure space:
  - The first two principal components (PC1 and PC2) capture the major climate gradients (PC1: warmer/drier to cooler/wetter; PC2: wetter to more temperature-stable).
  - PC1 explains 58.25% and PC2 21.43% of the variance.
- Exposure calculation:
  - Euclidean distance between pixels in PC1/PC2 space across adjacent time periods.
  - This distance serves as a dimensionless index of climate-change exposure for each 1 km location.

## Data structure and outputs
- Outputs:
  - GeoTIFF files of climate-change exposure metrics for the UK and the Isle of Man.
  - The mapped exposure metric is a dimensionless Euclidean distance in the PCA space.
- Spatial scope:
  - 1 km resolution across the UK and Isle of Man (data are provided as continuous surface maps).

## Quality control and references
- Methodological details and quality controls are described in Wilson & Pescott (2023) and associated supplementary materials.
- Key data sources and related references:
  - Hollis et al. (2019) HadUK-Grid dataset
  - Kendon et al. (2021), Lowe et al. (2018), Met Office (2019) UKCP18 Local projections
  - Wilson & Pescott (2023) Assessing the exposure of UK habitats to 20th- and 21st-Century climate change

## Relevance for monitoring frameworks
- Provides a transparent, reproducible metric of climate-change exposure to compare against plant monitoring coverage and gradients.
- Uses publicly available climate datasets and an explicit, multistage processing workflow (data extraction, downscaling, PCA, and distance calculations) suitable for monitoring frameworks.
- Metadata and data quality considerations include reliance on multiple data sources with different resolutions and the need for careful interpretation when transforming and sharing data; emphasizes governance around data provenance and openness.