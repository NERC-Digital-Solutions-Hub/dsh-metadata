# Overview

- Purpose and scope
  - Data underpin an assessment of the exposure of UK habitats to climate change and evaluate how well current UK plant monitoring schemes cover these exposure gradients.
  - Provides spatially explicit (1 km gridded) climate-change exposure metrics for the UK and the Isle of Man.

- What the data represent
  - An index of climate change exposure created by measuring the Euclidean distance in a reduced climate space (PC1/PC2) between positions of each 1 km pixel across adjacent time periods.
  - The two principal components summarize multivariate climate space: PC1 reflects warmer and drier vs cooler and wetter conditions; PC2 reflects wetter (especially winter) vs more temperature-stable conditions.
  - The Euclidean distance metric is dimensionless.

- Data content and metrics
  - For each time period, 37 bioclimatic variables are derived from monthly climate data.
  - Principal Components Analysis reduces these to PC1 and PC2, which are used to compute exposure across time.
  - Four pairwise time-period comparisons are provided (see below).

- Time periods and pairwise comparisons
  - 1901–1930 v 1961–1990
  - 1961–1990 v 2010–2019
  - 2010–2019 v 2021–2040
  - 2021–2040 v 2061–2080

- Data sources and processing
  - Historical and contemporary climate (1901–1930, 1961–1990, 2010–2020) from HadUK-Grid at 1 x 1 km:
    - Monthly precipitation and maximum/minimum/mean temperatures.
    - 1961–1990 used as a standard climate normal; other periods averaged to create long-term means.
  - Future and near-future projections (2021–2040 and 2061–2080) from UKCP18 Local data at 5 x 5 km:
    - 12 convection-permitting model simulations; ensemble mean used for exposure calculations.
    - Resampled to 1 km to match HadUK-Grid data (bilinear interpolation).
  - HadUK-Grid data are observationally-based gridded climate fields; UKCP18 Local data provide modeled projections.

- Data structure and format
  - Supplied GeoTIFF files containing the climate-change exposure metrics for the UK and Isle of Man.
  - The mapped exposure metric is a dimensionless Euclidean distance in PC space.

- Methodological quality and references
  - Methodology and details discussed in Wilson & Pescott (2023); further methodological details in the supplementary information.
  - Key data sources cited: Hollis et al. (2019) for HadUK-Grid; Kendon et al. (2021); Lowe et al. (2018); Met Office (2019) for UKCP18 Local.