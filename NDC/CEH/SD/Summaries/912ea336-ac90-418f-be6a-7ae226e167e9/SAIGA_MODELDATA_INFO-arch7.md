# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

- A GIS-focused, data-rich study documenting environmental conditions at saiga calving and die-off sites, with an emphasis on predicting mass mortality events (MMEs) linked to Pasteurella multocida.
- Aims to support spatial analysis and map-based visualization of environmental predictors associated with MMEs and calving dynamics.

## Spatial scope, data architecture, and access

- Shapefile contains 214 calving/die-off sites; 135 sites have complete predictor data at suitable resolution for modelling.
- Site metadata and environmental predictor data can be merged via a common variable ID from the Shapefile attribute table.
- Outputs include a 135-site dataset of climate/ vegetation predictors plus site metadata and a Dieoff variable (1 = die-off, 0 = normal calving).
- The dataset and shapefile are available via a dedicated data link (includes documentation and provenance details).

## Environmental predictor data sources

- Climate data: ERA-Interim reanalysis (daily aggregates derived from higher-frequency data for temperature, dew point, soil moisture, snow depth, wind gusts, precipitation).
- Precipitation: ERA-Interim data supplemented with GPCC interpolated gauge-based products (from 1988 onward) due to precipitation uncertainties in ERA.
- Vegetation and snow: NDVI and NDVI anomalies from MODIS (Vienna/BOKU) and SPOT/PROBA-V LifeWatch WB for snow anomalies; snow depth data also used for snow-melt calculations.
- Data periods: covering 1998–2016 (snow/NDVI anomalies) and earlier periods for other variables; subset of sites (94 with MODIS NDVI, ~96–95 with anomaly data) used for specific analyses.

## Data extraction, processing and metric generation

- Temporal reference: “zero hour” is calving onset or the index-day onset for die-off; predictors are aggregated over periods up to this date.
- Disease progression: evidence suggests rapid onset once signs appear; models use 3, 5, and 10 day windows before onset, plus other fixed-date periods (end of winter, green-up).
- Raster extraction: climate and environmental rasters extracted at site locations (from the shapefile), then aggregated to daily/periodic metrics.
- Metrics computed over multiple windows:
  - Precipitation totals for 0, 3, 5, 10 days before onset; also cumulative 2 months to onset; days with precipitation.
  - Temperature metrics: average, minimum, maximum, and variability over 0, 3, 5, 10 days before onset; includes overall temperature variation and daily minimum/maximum differences.
  - Snow metrics: snow melt date (last 3 consecutive snow days), total snow cover days, and days between snow melt and onset.
  - NDVI metrics: daily NDVI and NDVI anomalies interpolated to daily values; mean/min NDVI over 5/15/30/40 days to onset; NDVI anomaly statistics (April/May weeks; SPOT/PROBA-V anomalies).
  - Snow and NDVI anomalies: various anomaly measures (mean, min) for specific weeks and periods.
- Data interpolation: NDVI and snow anomaly datasets interpolated to daily values before aggregation.
- Two alternative metric sets were created to handle missing calving dates:
  - Real onset dates (where known) and metrics up to 9 May and 14 May for standardised comparisons.
  - A mixed dataset (STGNONSET) using real dates where available and estimates up to 9 May where not, enabling larger statistical analyses.

## Core variables, naming conventions, and dataset structure

- Core field names tracked in the dataset (site metadata, timing, and predictors) with multiple suffix options:
  - Core fields (e.g., Calving_ST, Calving_PK, Onset, Dieoff, etc.).
  - Suffix _STGN for metrics up to 9 May; _PKGN for metrics up to 14 May.
  - Suffix _STGNONSET for mixed real/generalised onset data (real dates plus STG values).
- Predictor variables include totals, means, maxima/minima, and various derived metrics for precipitation, temperature, humidity, wind, soil moisture, snow depth, and NDVI/snow/NDVI anomalies.
- Table 1 in the document enumerates the core predictor field names (and their sources), with both summary and source metadata.
- Datasets are designed to be joined to site metadata via IDs from the Shapefile attribute table.

## Datasets and how to use them in GIS workflows

- Two linked datasets:
  - Shapefile with 214 sites and metadata (Betpak-dala population context; Year, Calving dates, Dieoff status, and onset-related fields).
  - A companion attribute table of 135 sites containing the environmental predictor metrics aggregated to the specified time windows, plus derived variables (STGN, PKGN, STGNONSET variants).
- The environment predictor variables can be joined to the shapefile by the variable ID to create a spatial database suitable for GIS analysis and map-based visualization.
- The dataset supports modelling in published work (Kock et al., 2018) and can be used to reproduce or extend the multivariate models of MME risk.

## Modelling context and interpretation for GIS work

- Purpose is to model the probability of an MME at calving aggregations using environmental predictors.
- The dataset provides a spatially explicit set of predictors across multiple temporal windows, enabling exploration of where and when certain climatic or vegetation conditions coincide with calving and die-off events.
- The approach accounts for data gaps and date uncertainties by creating generalized onset metrics (STGNONSET) in addition to metrics based on known onset dates.

## Uncertainties, data quality, and notes for analysts

- Onset dates are missing for many sites; the methodology includes generalized date estimates to enable robust statistical analysis.
- Differences between ERA-Interim precipitation and GPCC data are acknowledged; GPCC data are used to supplement ERA where available.
- NDVI data have limitations (subset of sites; varying time coverage) and are interpolated to daily values for metric calculation.
- The dataset emphasises transparency in data provenance and metadata, with explicit field naming conventions and sources.

## References (context for GIS researchers)

- Kock et al. 2018: Saigas on the brink: multi-disciplinary analysis of the factors influencing a mass die-off event (Science Advances) – modelling framework and results linked to these predictors.
- Dee et al. 2011: ERA-Interim reanalysis data description and performance.
- Supporting data sources: GPCC, MODIS NDVI, SPOT/PROBA-V LifeWatch WB, and related methodological papers on NDVI/snow anomaly metrics.