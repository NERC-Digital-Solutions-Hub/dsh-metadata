# Historic Standardized Groundwater level Index (SGI) for 54 UK boreholes (1891-2015) Bloomfield JP, Marchant BJ and Wang L

## Project Overview
- Historic Droughts was a four-year, £1.5m project (2014–2018) funded by UK Research Councils to develop interdisciplinary understanding of past droughts in the UK and to improve tools for drought management.
- Aims to link hydrometeorological and social systems to understand past droughts and inform future water resource management.

## Inventory
- Involves eight UK institutions and delivers the Historic Droughts Inventory, a knowledge base of past drought characteristics, impacts, and responses.
- Inventory components:
  - i) Hydro-meteorological timelines of rainfall, river flows, and groundwater with consistent drought indicators.
  - ii) References to past droughts from newspapers, legislation, agricultural media, and oral histories.
- SGI dataset is one of the groundwater-related datasets within the Inventory, alongside reconstructed groundwater levels.

## Description of the dataset
- The SGI series are standardised monthly groundwater levels based on reconstructed groundwater level time series for UK boreholes.
- Standardisation uses a non-parametric normal scores transform for each calendar month.
- Includes probability estimates for SGI being below 0, -1, -1.5, and -2.
- Time period covered: 1891–2015.
- Site locations span Principal Aquifers in the UK, with most boreholes in southern/eastern England on the Chalk aquifer.

## Motivation
- Produced by the British Geological Survey as part of Historic Droughts to define and monitor groundwater droughts for long-historic records and to support drought management planning.
- SGI enables direct comparison with meteorological drought indices (e.g., SPI) and other hydrological drought indicators (e.g., SSI).

## Data sources
- Reconstructed groundwater level data prepared for the Historic Droughts Inventory (Bloomfield et al., 2018) underpin the SGI standardisation.

## Standardisation method
- Monthly normal scores transform applied to reconstructed groundwater levels for each calendar month.
- Process involves ranking observations within a month, applying inverse normal CDF to generate SGI values.

## Uncertainty and probability estimation
- Uncertainty in reconstructions quantified via Generalised Likelihood Uncertainty Estimation (GLUE).
- Behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5) converted to SGI series.
- Probabilities for SGI thresholds derived from the proportion of behavioural SGI series within specified intervals.

## Data formats and files
- Datasets provided as CSV files (one per site) with headers:
  - Date: Year-Month-Day (format: YYYY-MM-DD), with days reported as the first of the month.
  - SGI: Standardised groundwater level value.
  - Prob0: probability SGI < 0.
  - Prob1: probability SGI < -1.
  - Prob15: probability SGI < -1.5.
  - Prob2: probability SGI < -2.
- File naming convention examples: HistoricDroughts_BGSAquiMod_Output_Feb2018_SGI_Rockleyver1 (per site).
- An additional Metadata_forGWLandSGI_reconstructions.csv file lists site metadata, including:
  - Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS-site_name, Aquifer, MORECS_ID, etc.

## Metadata and spatial context
- Metadata file provides site coordinates (Easting/Northing) and aquifer information for GIS integration.
- Site list comprises 54 UK boreholes located on various Principal Aquifers (predominantly Chalk).

## Motivation for GIS use
- Enables time-series visualization and mapping of groundwater drought status across the UK.
- Facilitates cross-comparison with meteorological drought indices (SPI) and hydrological drought indicators (SSI).
- Standardised format and accompanying probabilities support uncertainty-aware GIS analyses.

## Usage considerations
- Datasets are designed for interoperability with GIS and time-series analysis workflows.
- The per-site CSV structure supports modular loading into map-based visualizations and analyses.
- Consistent site metadata supports alignment with other hydrogeological datasets and basemaps.

## Acknowledgements
- Funded by the Natural Environment Research Council through the Historic Droughts project (NE/L010151/1).

## References
- Allen et al. 1997; Barker et al. 2016; Bloomfield et al. 2018; Bloomfield & Marchant 2013; Beven & Freer 2001; McKee et al. 1993; WMO 2012.
- Related project outputs and metadata described in the Historic Droughts inventory documentation.