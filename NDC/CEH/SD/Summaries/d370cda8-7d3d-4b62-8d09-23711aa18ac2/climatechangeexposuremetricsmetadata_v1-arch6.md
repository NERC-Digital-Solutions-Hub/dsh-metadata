# Assessing the exposure of UK habitats to 20th- and 21st-Century climate change

## Overview
- Provides spatially explicit, 1 km gridded metrics of climate change exposure for UK habitats.
- Linked to an assessment of how well current UK plant monitoring schemes cover exposure gradients.
- Four comparisons between five time periods:
  - 1901-1930 vs 1961-1990
  - 1961-1990 vs 2010-2019
  - 2010-2019 vs 2021-2040
  - 2021-2040 vs 2061-2080

## Data collection and generation
- Climate data sources:
  - HadUK-Grid (monthly precipitation and max/min/mean temperatures) at 1 x 1 km for historical/present periods.
  - UKCP18 Local data (5 x 5 km) for future periods (2021-2040 and 2061-2080), resampled to 1 km to match HadUK-Grid.
- Time periods:
  - Historical and contemporary: 1901-1930, 1961-1990, 2010-2020
  - Future: 2021-2040, 2061-2080
- Modeling approach:
  - For each period, 37 bioclimatic variables were generated from monthly data.
  - Variables were scaled and reduced with Principal Components Analysis.
  - The first two principal components (PC1 and PC2) summarize climate space:
    - PC1: warmer/drier to cooler/wetter gradient (58.25% of variance)
    - PC2: wetter (especially winter) to more temperature-stable conditions (21.43%)
  - Euclidean distance in PC1/PC2 space between corresponding pixels across adjacent time points is used as the climate-change exposure index.

## Output and data structure
- Output format: GeoTIFF files.
- Coverage: Maps of the climate-change exposure metric for the UK and the Isle of Man.
- Metric characteristics: The exposure index is a dimensionless Euclidean distance in PC space.

## Usage and interpretation (for data use and analysis)
- Enables exploration of spatial exposure gradients to climate change across UK habitats.
- Serves as a basis for cross-referencing habitat/climate risk with plant monitoring schemes to assess coverage of exposure gradients.
- Suitable for creating dashboards, reports, or self-serve analyses that compare regions and time periods.
- Can be combined with other data layers (e.g., habitat maps, biodiversity surveys) to identify priority areas for monitoring or conservation planning.

## Quality, provenance, and references
- Quality control and methodological details described in Wilson & Pescott (2023) (peer-reviewed context).
- Key data sources and related documents:
  - Hollis, D., McCarthy, M., Kendon, M., Legg, T., & Simpson, I. (2019). HadUK-Grid.
  - Kendon, E. et al. (2021). Update to UKCP Local (2.2km) projections.
  - Lowe, J. A. et al. (2018). UKCP18 science overview.
  - Met Office (2019). UKCP18-Land.
  - Wilson, O.J. & Pescott, O.L. (2023). Assessing the exposure of UK habitats to 20th- and 21st-Century climate change.

## Access and format notes (data integration considerations)
- Data are provided as GeoTIFFs at 1 km resolution, aligned to enable cross-time comparisons.
- The underlying approach uses a dimensionality-reduced climate space (PC1-PC2) to summarize multi-variable climate signals into a simple, comparable exposure metric.
- The Euclidean distance metric is dimensionless, facilitating integration with other spatial datasets and indicators.