# Drought indicator time series for European NUTS regions based on remote sensing data (2000-2015)

## Overview
- Remotely sensed drought indicators time series for Europe (2000-2015) derived from CEH’s gridded drought indicators product.
- Indicators: Vegetation Condition Index (VCI) from NDVI, Temperature Condition Index (TCI) from Land Surface Temperature, and Vegetation Health Index (VHI) as a combination of VCI and TCI.
- Data extracted for European NUTS regions (levels 0, 1, 2, and 3) and masked by a simplified land use/land cover (LULC) map with four classes (forest, crop, shrub, grass) plus an all-classes series.
- Data stored as CSV files and organized in folder structures.

## What the dataset contains
- Time series of three drought indicators (VCI, TCI, VHI) for each NUTS region and each LULC class, plus an overall series per region.
- For each region, 15 time series in total (5 per drought indicator: one for each of the 4 land cover classes plus one for the whole region).
- LULC mask derived from MODIS MCD12C1 data (0.05° resolution) for 2012.
- Data includes a quality rule: a time step is included only if at least 50% of pixels in the non-masked area have valid values.
- Two No Data values used: “--” indicates no valid pixels; “nan” indicates some valid pixels but coverage <50%.

## Motivation and context
- Generated within the DrIVER project (Drought Impacts and Vulnerability thresholds in monitoring and Early warning Research), aimed at assessing drought indices against impact data for monitoring and early warning (M&EW).
- Demonstrates the potential of remote sensing for near real-time, global-coverage, cost-effective drought monitoring.
- Addresses variability in the use of remote sensing drought indicators in operational M&EW systems and supports evaluation of indicators across vegetation types.
- Regional focus (NUTS) aligns with availability of validation impact data at that scale.
- Related findings and methodology discussed in Bachmair et al. (2018) and related references.

## Data sources and derivation
- Gridded drought indices for Europe (2000-2015) used as the primary data source (Tanguy et al., 2016).
- LULC baseline from MODIS Land Cover Type product (MCD12C1) for 2012 used to create four-class mask (forest, crop, grass, shrub).
- NDVI-derived VCI computed as (NDVI − NDVI_min,i) / (NDVI_max,i − NDVI_min,i) for monthly values.
- TCI computed similarly using LST values: (LST_max,i − LST) / (LST_max,i − LST_min,i).
- VHI = α · VCI + (1 − α) · TCI, with α commonly set to 0.5, assuming equal contribution of VCI and TCI.
- NUTS geographic reference uses the 2013 version for statistical divisions.

## Data format and structure
- Stored in CSV format.
- Data organized in folders (structure described in accompanying documentation) to reflect regions, indicators, and land cover classes.

## Data quality and handling of gaps
- Time steps with insufficient coverage (<50% valid pixels) are discarded to ensure representativeness.
- Distinguishes between no data (no valid pixels) and partial data (some valid pixels but <50% coverage).
- LULC-based differentiation allows assessment of drought indicators across land cover types, but relies on the 2012 MODIS LULC snapshot for mask application.

## Data governance and accessibility
- Rooted in the NERC Environmental Information Data Centre and the DrIVER project framework.
- Emphasizes the potential for verification against impact data and integration into M&EW systems.
- Metadata, provenance, and methodological details are provided to support data reuse and transparency.

## Acknowledgments and references
- Funded by the Natural Environment Research Council (award NE/L010038/1) as part of Belmont Forum initiatives.
- References include works on remote sensing of drought indicators and their interpretation (e.g., AghaKouchak et al., 2015; Kogan, 1995; 1996; Bachmair et al., 2016; 2018; Tanguy et al., 2016).

## Relevance for monitoring framework authors
- Demonstrates end-to-end monitoring data production: from remote sensing indicators to region-based time series with land cover differentiation.
- Highlights practical considerations for monitoring systems: data availability, metadata quality, data transformation needs, threshold-based inclusion criteria, and governance around data sharing.
- Provides a replicable approach for generating Europe-wide drought indicators aligned with administrative regions (NUTS) and supports validation with impact data at the same spatial scale.