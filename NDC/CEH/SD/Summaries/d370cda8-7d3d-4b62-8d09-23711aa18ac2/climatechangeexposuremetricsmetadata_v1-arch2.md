# Overview

- The dataset underpins an assessment of the exposure of UK habitats to climate change and a linked evaluation of how well current UK plant monitoring schemes cover exposure gradients (see Wilson & Pescott, 2023).
- It provides a spatially explicit climate-change exposure index to support consistent environmental health and policy performance assessment over time.

## Objective and scope

- Produce a standardized, time-resolved measure of climate-change exposure for UK habitats to enable scrutiny of environmental health and policy performance.
- Compare exposure gradients against existing plant monitoring schemes.

## Data description

- Spatial resolution: 1 x 1 km (UK and Isle of Man).
- Time periods and comparisons (four pairwise comparisons across five periods):
  - 1901–1930 v 1961–1990
  - 1961–1990 v 2010–2019
  - 2010–2019 v 2021–2040
  - 2021–2040 v 2061–2080
- Exposure metric: Euclidean distance in climate space (PC1/PC2) between adjacent time points.
- Output format: GeoTIFF maps; the exposure metric is dimensionless.

## Data sources and processing

- Historical/contemporary data: HadUK-Grid (monthly precipitation; max/min/mean temperatures) at 1 km resolution; 1961–1990 used as the normal period; other periods created from annual means.
- Future projections: UKCP18 Local data (5 km × 5 km) for 2021–2040 and 2061–2080, downsampled to 1 km via bilinear interpolation; 12 simulations used as ensemble mean for better agreement with observations.
- Derived variables: For each period, 37 bioclimatic variables derived from monthly data; dimensionality reduced with PCA.
- PCA summary: PC1 ( warmer/drier vs cooler/wetter; 58.25% variance) and PC2 ( wetter vs temperature-stable; 21.43% variance) used to define climate-space coordinates.

## Quality control and references

- Methodological quality and details described in Wilson & Pescott (2023).
- Key data sources and related methods:
  - Hollis et al. (2019) HadUK-Grid
  - Kendon et al. (2021) UKCP18 Local projections
  - Lowe et al. (2018); Met Office (2019) UKCP18-related reports
  - Wilson & Pescott (2023) for exposure assessment methodology

## Data structure and usage

- Delivered as GeoTIFF files containing the climate-change exposure metrics.
- The Euclidean distance in PC1/PC2 space is a dimensionless exposure index per 1 km pixel.

## Relevance for Analysts Monitoring the Environment

- Demonstrates a standardized approach to convert historical and projected climate data into an actionable exposure metric across time.
- Facilitates cross-dataset comparability (habitat exposure vs monitoring coverage) and supports policy performance assessment.
- Data storage and accessibility aligned with typical monitoring workflows (datasets stored/uploaded to appropriate portals).

## Practical considerations and limitations

- UKCP18 Local projections at 2.2–5 km resolution require interpolation to 1 km; ensemble mean used rather than individual realizations.
- PCA-based reduction captures major gradients but may omit finer-scale variability.
- Exposure is a proxy for climate change impact; interpretation should consider model uncertainties and spatial heterogeneity.

## Related outputs and implications

- Part of a broader assessment linking climate exposure to habitat health and plant-monitoring coverage (Wilson & Pescott, 2023).

## References

- Hollis, D., et al. (2019). HadUK-Grid: A new UK dataset of gridded climate observations.
- Kendon, E., et al. (2021). Update to UKCP Local (2.2km) projections.
- Lowe, J. A., et al. (2018). UKCP18 science overview report.
- Met Office (2019). UKCP18-Land science report.
- Wilson, O.J., & Pescott, O.L. (2023). Assessing the exposure of UK habitats to 20th- and 21st-Century climate change.