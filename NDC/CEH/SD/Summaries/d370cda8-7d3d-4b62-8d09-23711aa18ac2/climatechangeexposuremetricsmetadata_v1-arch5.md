# Assessing the exposure of UK habitats to 20th- and 21st-Century climate change

## Purpose and scope
- Provides spatially explicit (1 km) climate-change exposure metrics underpinning an assessment of UK habitats' exposure to climate change.
- Compares four time-period pairs to quantify exposure: 1901-1930 vs 1961-1990; 1961-1990 vs 2010-2019; 2010-2019 vs 2021-2040; and 2021-2040 vs 2061-2080.
- Includes a linked assessment of how well current UK plant monitoring schemes cover these exposure gradients.

## Data sources and processing
- Historical and present climate data from HadUK-Grid (1 x 1 km): monthly precipitation, max/min/mean temperatures; baseline 1961-1990 used for normal references.
- Future projections from UKCP18 Local (5 x 5 km, downsampled to 1 km via bilinear interpolation) for 2021-2040 and 2061-2080.
- UKCP18 Local dataset used at 2.2 km resolution with a 12-member convection-permitting ensemble; the 12-member ensemble mean is used for analysis.
- For each period, 37 bioclimatic variables are generated from monthly data; variables are scaled and reduced with PCA. The first two principal components (PC1 and PC2) explain the majority of variance and summarize climatic space.
- Climate-change exposure is quantified as the Euclidean distance in PC1/PC2 space between corresponding pixels across adjacent time periods, producing a dimensionless exposure index.

## Data products and structure
- Supplied GeoTIFF files represent the climate-change exposure metrics for the UK and the Isle of Man.
- The exposure metric is dimensionless (Euclidean distance in the PCA-defined climate space).

## Quality control and provenance
- Methodological details and quality control are provided in Wilson & Pescott (2023); additional methodological context is in the referenced sources:
  - HadUK-Grid: Hollis et al. (2019)
  - UKCP18 Local: Kendon et al. (2021); Lowe et al. (2018); Met Office (2019)
- The dataset integrates historical, present, and multiple future periods using ensemble means to improve consistency with observed patterns.

## Relevance for data stewardship
- Provenance: clearly documents data origins (HadUK-Grid, UKCP18 Local) and the processing chain (downscaling, PCA, exposure computation).
- Metadata considerations: ensure detailed records of data sources, resolutions, time periods, ensemble usage, PCA components, and the exposure calculation method; include references to Wilson & Pescott (2023) for QC context.
- Versioning and updates: plan for future updates as new climate projections become available; preserve the lineage of each processing step and the exact ensemble used.
- Data formats and interoperability: GeoTIFFs are standardized for spatial data; ensure consistent coordinate reference system and grid alignment across all tiles and time periods.
- Access and licensing: confirm data licensing and sharing permissions; document any embargoes or usage restrictions in metadata.

## Challenges and considerations for Data Stewards
- Gaps in user needs and project scope may complicate metadata and documentation alignment.
- Timely access to input data (HadUK-Grid, UKCP18 Local) and the integration of multiple datasets across resolutions.
- Ensuring data creators (data producers) meet standards for metadata, formats, and documentation across diverse systems.
- Handling large, multi-period, high-resolution datasets and potential non-interoperable legacy components.
- Maintaining data quality and traceability across updates and when combining ensemble means with multiple time periods.

## References (data provenance and methods)
- Hollis, D., McCarthy, M., Kendon, M., Legg, T., & Simpson, I. (2019). HadUK-Grid: A new UK dataset of gridded climate observations.
- Kendon, E., Short, C., Pope, J., Chan, S., Wilkinson, J., et al. (2021). Update to UKCP Local (2.2km) projections.
- Lowe, J. A., et al. (2018). UKCP18 science overview.
- Met Office (2019). UKCP18-Land science report.
- Wilson, O.J. & Pescott, O.L. (2023). Assessing the exposure of UK habitats to 20th- and 21st-Century climate change. Journal of Applied Ecology.