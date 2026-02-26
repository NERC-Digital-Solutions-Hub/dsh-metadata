# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

## Overview
- Study of environmental conditions at calving/die-off sites for the Betpak-dala saiga population in central Kazakhstan.
- Focus on factors associated with mass mortality events (MMEs) caused by Pasteurella multocida, occurring mainly in May during calving aggregations.
- Dataset supports modelling the probability of MMEs using environmental predictor variables; part of a broader multi-disciplinary analysis (Kock et al. 2018).

## Data sources and predictors
- Climate data: ERA-Interim daily reanalysis from ECMWF (temperature, humidity, precipitation, soil moisture, snow depth, wind).
- Precipitation data: GPCC gauge-based products to supplement ERA (from 1988 onwards).
- Vegetation data: NDVI metrics from MODIS (absolute NDVI; 7-day filtered) and NDVI anomalies from SPOT/PROBA-V LifeWatch WB project.
- Snow data: Snow depth and snow anomaly metrics; snow melt timing derived from ERA snow depth.
- Predictor variables represent indicators of haemorrhagic septicaemia risk, vegetation response, and winter severity (e.g., NDVI, snow depth/anomalies, temperature/precipitation metrics).

## Data extraction and processing
- Timeframe defined by a “zero hour”: start of calving or index-case onset of death.
- Predictors aggregated over 3, 5, and 10-day windows before onset, plus two broader pre-onset periods (two months prior to onset).
- For precipitation: totals over windows, plus number of days with precipitation (wet-weather duration).
- Temperature variability metrics computed to capture daily and broader weather pattern changes over 0/3/5/10 days before onset.
- Snow melt date derived from last three consecutive snow-cover days; metrics include total snow-cover days and days between snow melt and calving/onset.
- NDVI and snow/NDVI anomaly data interpolated to daily values and aggregated over multiple periods (including fixed-date windows like May 9 and May 14 due to missing exact calving dates).
- Dataset includes 135 sites with multiple metric variants:
  - Core metrics (STGN, PKGN) tied to real onset dates (many missing values).
  - Generalized dates (Calving_STGN = May 9, Calving_PKGN = May 14) for standardized metrics.
  - STGNONSET and related fields combine real dates with estimations to enable robust modelling.
- Dataset structure uses a common ID system to merge site metadata with environmental predictors.
- Core metric naming and suffix conventions:
  - Core fields, Core_STGN (up to May 9), Core_PKGN (up to May 14).
  - Onset-based predictors and STGNONSET fields for mixed-origin dates.
- Data records include Dieoff (0 = normal calving, 1 = die-off) and Year, with site metadata and provenance described in the associated Shapefile and documentation.

## Dataset structure and availability
- Full set: 214 calving/die-off sites with location metadata and predictor data (Shapefile + metadata).
- Analysed subset: 135 sites with sufficient predictor data for modelling.
- Outputs can be merged via variable IDs between the environmental dataset and site metadata.
- Core predictor variables are documented in Table 1 (as referenced in the dataset documentation).
- References for data sources and methods include ERA-Interim (Dee et al. 2011), GPCC (Schamm et al. 2014), MODIS NDVI (Vuolo et al. 2012), SPOT/PROBA-V NDVI anomalies (Radoux et al. 2015), and snow anomalies (Rousseau et al. 2015).

## Applications for monitoring and policy
- Enables modelling of MME probability at saiga calving aggregations to inform risk monitoring and early-warning systems.
- Demonstrates integration of multiple environmental data streams (climate, vegetation, snow) to identify potential environmental triggers or precursors.
- Provides a transparent workflow for data extraction, processing, and variable construction, supporting reproducibility and governance in monitoring frameworks.
- The modelling context is detailed in Kock et al. (2018), with data and metadata available for replication and further policy-relevant analysis.

## Data governance, quality, and access considerations
- Metadata and data provenance are emphasized, with explicit links between predictor variables and data sources.
- Data quality considerations include handling missing onset dates, harmonizing datasets with differing temporal resolutions, and ensuring timely updates where possible.
- Public sharing of underlying datasets is a known barrier; the documentation highlights openness and data-management standards, and provides a process for data sharing via the dataset’s metadata and Shapefile attributes.
- Data processing involves substantial transformation and standardization (e.g., daily interpolation of NDVI/snow anomalies, multi-day aggregations), underscoring the need for clear documentation and governance around data transformations.

## References
- Dee, D. P. et al. 2011. The ERA-Interim reanalysis: configuration and performance of the data assimilation system.
- Kock, R. et al. 2018. Saigas on the brink: multi-disciplinary analysis of the factors influencing a mass die-off event.
- Pinzon, J. E. & Tucker, C. J. 2014. A Non-Stationary 1981-2012 AVHRR NDVI3g Time Series.
- Radoux, J. et al. 2015. Seasonal metrics and anomaly detection based on SPOT-VEGETATION archive in Europe.
- Rousseau, C. et al. 2015. Snow cover anomalies from 2000 to 2014.
- Schamm, K. et al. 2014. Global gridded precipitation over land: GPCC first guess daily product.
- Vuolo, F. et al. 2012. Data service platform for MODIS Vegetation Indices time series processing.