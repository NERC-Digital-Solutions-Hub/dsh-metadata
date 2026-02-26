# Overview

- The data described underpin an assessment of the exposure of UK habitats to climate change and a linked evaluation of how well current UK plant monitoring schemes cover these exposure gradients (see Wilson & Pescott, 2023).
- Dataset provides spatially explicit climate-change exposure metrics at 1 x 1 km resolution, derived from differences between observed historical and predicted future climates.
- Four comparisons are made across five time periods: 1901–1930 vs 1961–1990; 1961–1990 vs 2010–2019; 2010–2019 vs 2021–2040; and 2021–2040 vs 2061–2080.

- Collection/generation methods
  - Convert past, present, and future climate data into a measure of climatic change.
  - Historical/contemporary periods use HadUK-Grid data (monthly precipitation; max/min/mean temperatures) at 1 x 1 km; 1961–1990 used as the norm period; other periods derived from annual means.
  - UKCP18 Local data for 2021–2040 and 2061–2080 at 5 x 5 km were resampled to 1 km using bilinear interpolation to match HadUK-Grid data.
  - UKCP18 Local (2.2 km) dataset comprised 12 convection-permitting simulations; the 12-member ensemble mean was used due to closer agreement with observed patterns (per Wilson & Pescott 2023 supplementary information).

- Nature and units of recorded values
  - For each period, 37 bioclimatic variables were generated from the monthly climate data.
  - Variables were scaled and dimensions reduced with Principal Components Analysis (PCA).
  - The first two PCs summarize multivariate climate space:
    - PC1: gradient from warmer/drier to cooler/wetter.
    - PC2: gradient from wetter (notably winter) to more temperature-stable conditions.
  - PC1 explains 58.25% of variance; PC2 explains 21.43%.
  - A Euclidean distance between pixel positions in PC1/PC2 space across adjacent time points yields the climate-change exposure index for each location; applied across all four period comparisons.

- Quality control
  - Methodological details and quality considerations are described in Wilson & Pescott (2023).

- Details of data structure
  - Supplied GeoTIFF files provide maps of the climate-change exposure metrics for the UK and the Isle of Man.
  - The mapped Euclidean distance metric is dimensionless.

- References (data sources and related methodology)
  - Hollis et al. 2019. HadUK-Grid: a new UK dataset of gridded climate observations.
  - Kendon et al. 2021; Lowe et al. 2018; Met Office 2019. UKCP Local and UKCP18-related documents.
  - Wilson, O.J. & Pescott, O.L. 2023. Assessing the exposure of UK habitats to 20th- and 21st-C century climate change. Journal of Applied Ecology (not yet assigned to an issue).