# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

## Overview
- Examines environmental conditions at calving sites of the Betpak-dala saiga population, the region where mass mortality events (MMEs) have occurred.
- MMEs (notably 1981, 1988, 2015) are linked to Pasteurella multocida infections; triggers may involve environmental factors affecting host immunity.
- The dataset provides environmental predictors for modeling the probability of MMEs at calving aggregations and complements the modeling described in Kock et al. (2018).

## Scope and purpose
- Contains environmental predictor variables for 135 calving/die-off sites (out of 214 with location data) with sufficient data resolution.
- The full 214-site shapefile and site metadata are available; 135 sites have the required predictor data for modeling.
- Aims to identify correlations and potential environmental triggers (climate, vegetation, snow dynamics) associated with MMEs, enabling predictive modeling.

## Data sources
- Climate data: ERA-Interim daily reanalysis from ECMWF (temperature, dew point, soil moisture, snow depth, wind gust, precipitation); daily aggregates derived from 3–6 hourly data.
- Precipitation: GPCC interpolated gauge-based products supplement ERA data (available from 1988 onward).
- Vegetation: NDVI from MODIS (7-day filtered/smoothed) and NDVI anomalies from SPOT/PROBA-V (LifeWatch WB project).
- Snow: Snow depth data and snow anomaly data; snow-melt date computed from ERA snow depth; snow-related metrics include snow cover duration.
- Additional NDVI anomaly datasets (GIMMs-based) exist but are not part of the attached dataset; available on request.
- Site metadata: Shapefile with 214 sites; 135 sites accompanied by predictor data and metadata in the attached dataset.

## Predictors and processing
- Time windows: predictors aggregated over 3, 5, and 10 days before onset of calving/MME; also precipitation over 0, 3, 5, and 10 days, plus 2 months before onset.
- Onset definition: zero hour set to calving start or index-case onset; incubation and onset may occur from several days to ~12 hours before signs; where dates were missing, analyses used fixed reference dates (9 May and 14 May) as standard onset points.
- Temperature and variability: metrics include average and max daily temperature variation (0, 3, 5, 10 days), overall temperature range (3/5/10 days), and max min-temperature differences (3/5/10 days).
- Humidity and dew point: multiple metrics for mean and max humidity/dew point over 3–10 days; several fields indicate ERA-Interim or validated equivalents.
- Precipitation: total precipitation on onset, over 3/5/10 days, and cumulative totals; number of wet days; GPCC-based precipitation over corresponding windows.
- Snow metrics: snow-melt date (last three consecutive snow-cover days), length of snow cover, and related snow-cover anomalies.
- NDVI metrics: mean and min NDVI over various windows (40/30/15/10/5 days; including April and May weeks; March/April wave references), and NDVI anomaly metrics (April weeks 3–4, May week 1, etc.) with standardization (NDVI × 10000 or SD units for anomalies).
- Data naming conventions: four predictor-generation approaches:
  - Core fields (up to onset; many missing values)
  - Suffix _STGN (metrics up to 9 May)
  - Suffix _PKGN (metrics up to 14 May)
  - Suffix _STGNONSET (mixed real/onset-derived values for modeling)
- Core variable naming and table references are documented (Table 1 in the source) to support dataset integration.

## Dataset structure and access
- Dataset includes 135 sites with predictor variables and a Dieoff variable (1 = MME, 0 = normal calving).
- For each site: year, calving/die-off dates, onset estimates (or obs_deaths), and many predictor fields with multiple timing variants.
- Onset-related fields may be real dates or generalized estimates (STGNONSET) to enable robust statistical analysis despite missing exact onset dates.
- Spatial and metadata linkage via a unique ID; mergeable with the site metadata in the Shapefile attribute table using that ID.
- The dataset, accompanying metadata, and the Shapefile are accessible via the CEH data portal link provided in the original documentation (and linked to the 214-site shapefile).

## Modelling context and usage
- Predictor variables were used to model the probability of an MME at calving aggregations; results and modeling approaches are detailed in Kock et al. (2018).
- For analysts:
  - You can merge these predictors with site metadata to reproduce or extend multivariate analyses.
  - Consider different onset-date assumptions (real dates vs. STGN/STGNONSET) and multiple time windows (3/5/10 days) to test robustness.
  - The dataset supports exploration of correlations between climate/vegetation/snow metrics and MMEs, as well as predictive modelling of outbreak likelihood.

## References and access
- Key references:
  - Kock, R. et al. 2018. Saigas on the brink: multi-disciplinary analysis of the factors influencing a mass die-off event. Science Advances.
  - Dee, D. P. et al. 2011. The ERA-Interim reanalysis: configuration and performance.
  - Radoux, J. et al. 2015; Rousseau, C. et al. 2015; Schamm, K. et al. 2014; Vuolo, F. et al. 2012.
- Data access:
  - Shapefile and site metadata with documented provenance at the CEH Data Portal (link provided in the original document).
  - The attached dataset includes the 135 sites with predictor variables and the Dieoff variable.