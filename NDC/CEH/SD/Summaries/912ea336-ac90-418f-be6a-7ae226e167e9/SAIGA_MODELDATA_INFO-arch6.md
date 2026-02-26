# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

## Overview
- Saiga antelope mass mortality events (MMEs) are linked to haemorrhagic septicaemia from Pasteurella multocida, typically occurring in May at calving aggregations.
- Focuses on Betpak-dala population in central Kazakhstan, the area with recorded MMEs (1981, 1988, 2015) and normal calving at many sites.
- Attached dataset provides environmental predictor variables for 135 calving/die-off sites (out of 214 in the full shapefile) to model MME probability.
- Dataset and modelling approach described in Kock et al. (2018); data and site metadata are available via a linked shapefile and EIDC repository.

## Data sources and environmental variables
- Climate data: ERA-Interim daily reanalysis (ECMWF) for temperature, dew point, soil moisture, snow depth, wind, precipitation; daily aggregates created from 3–6 hourly data.
- Precipitation: ERA-Interim data supplemented with GPCC gauge-based products (from 1988 onward) due to precipitation uncertainties in ERA.
- Vegetation and snow:
  - NDVI: Absolute NDVI from 7-day filtered MODIS data (2001–2016 subset; 94 sites) and NDVI anomalies from SPOT/PROBA-V LifeWatch WB (1998–2016; subset ~96–95 sites).
  - Snow: Snow anomaly data from LifeWatch WB (1998–2016) and MODIS-derived snow presence data.
- Site metadata: 214-site shapefile with location and provenance; 135 sites in the final dataset with necessary predictor data.

## Data extraction and processing
- Time frame: “Zero hour” is calving start or onset of a die-off; predictors aggregated over periods up to those dates.
- Biological basis: Disease progression from first signs to death occurs over hours; incubation ~12 hours to several days; variables generated for 3, 5, and 10 days before onset to capture potential environmental triggers.
- Aggregation and features:
  - Climate: totals, means, maxima, minima over 3/5/10 days before onset; precipitation metrics include number of wet days; two-month precipitation totals to onset (cum 0D).
  - Temperature variability: various metrics including average/maximum daily temperature variation, overall temperature variation, and daily minimum temperature oscillations over 3/5/10 days.
  - Snow: snow melt date from last three consecutive snow-cover days; snow cover length and days between end of snow melt and calving/onset.
  - NDVI and anomalies: daily-interpolated NDVI and anomaly metrics for multiple pre-onset windows (e.g., 40/30/15/5/and other periods; April/May weeks; SD units for anomalies).
- Data formats and integration:
  - Raster climate data and site shapefile metadata merged via site ID.
  - Daily rasters interpolated to daily values for anomaly and mean calculations.
  - Two date schemes for predictors: real onset dates (where known) and generalized dates (e.g., 9 May for calving start, 14 May for peak calving) to fill gaps.
- Dataset variations and naming conventions:
  - Core metrics vs. generalized onset metrics with suffixes:
    - Core field names (up to onset) and fields suffixed with _STGN (up to May 9) and _PKGN (up to May 14).
    - STGNONSET fields combine real onset dates with generalized estimates for modelling.
  - Dataset includes extensive metadata fields: Calving_ST, Calving_PK, CALVE_STGN, CALVE_PKGN, Onset, Obs_deaths, Last_death, Dieoff, Year, Population, etc.
- Data scope:
  - Final dataset: 135 sites with environmental predictors and Dieoff status; 214-site shapefile provides broader context and provenance.

## Dataset contents and structure
- Core variables cover site metadata, onset/die-off timing, and predictor groups:
  - Dieoff (0 = normal calving, 1 = die-off), Year, Population (Betpak-dala).
  - Calving and onset timing: Calving_ST, Calving_PK, CALVE_STGN, CALVE_PKGN, Onset, Obs_deaths, Last_death.
  - Totals and metrics for precipitation (e.g., TOTPRECIP_0D, 3D, 5D, 10D; with GPCC equivalents), soil moisture, temperatures (min, max, mean) across 0–10 days; dew point; humidity metrics; wind gusts.
  - Snow metrics: SNOWMELT_JD, snow depth, snow anomalies.
  - NDVI metrics: mean and min NDVI over 40/30/15/5 days to onset; NDVI anomaly metrics by period (April/May weeks and related aggregates) and related NDVI anomaly statistics.
  - NDVI and SNOW anomalies sourced from MODIS, SPOT/PROBA-V, and LifeWatch WB datasets; standardized as per data source conventions.
- Data access:
  - Shapefile with complete site metadata and provenance available at the EIDC, linked to the environmental predictor dataset.
  - The attached dataset provides the 135-site environmental predictors with the associated onset/die-off outcomes.

## How to use and integrate
- Primary use: modeling the probability of an MME at saiga calving aggregations, enabling exploratory analysis and predictive modelling.
- Integration steps:
  - Merge the environmental predictor data with site metadata using the common variable IDs (as in the shapefile attribute table).
  - Utilize real onset-based predictors when onset dates are known; otherwise use the generalized onset fields (STGN/STGNONSET) for model completeness.
  - Select predictor sets and suffix versions (e.g., _STGN vs _PKGN vs _STGNONSET) appropriate to the modelling approach and data completeness.
- Potential analyses:
  - Multivariate modelling to identify environmental triggers or combinations associated with MMEs (as explored in Kock et al. 2018).
  - Comparative assessment of predictor importance across 3/5/10-day windows before calving onset.
  - Spatial-temporal analyses across Betpak-dala site network to identify regional patterns.

## Limitations and caveats
- Missing/onset date uncertainties:
  - Calving dates are missing for many sites; two date schemes were implemented to mitigate this, but residual uncertainty remains.
- Data coverage and availability:
  - NDVI absolute values available only for a subset of sites (94–96) and only for certain datasets; GPCC precipitation data available from 1988 onward.
  - Some predictor fields have multiple versions (real vs generalized dates) and varying degrees of completeness.
- Data scale and resolution:
  - Large geographic scale with diverse data sources; discrepancies between ERA-Interim and GPCC precipitation and potential biases in anomalies due to differing temporal coverage.
- Modelling considerations:
  - The core dataset is designed for statistical analysis with mixed real/generalized dates; careful handling of missing values and date imputation is required for robust modelling.

## References
- Dee, D. P., et al. 2011. The ERA-Interim reanalysis: configuration and performance of the data assimilation system. Quarterly Journal of the Royal Meteorological Society.
- Kock, R., et al. 2018. Saigas on the brink: multi-disciplinary analysis of the factors influencing a mass die-off event. Science Advances.
- Pinzon, J. E., & Tucker, C. J. 2014. A Non-Stationary 1981-2012 AVHRR NDVI3g Time Series. Remote Sensing.
- Radoux, J., et al. 2015. Seasonal metrics and anomaly detection based on SPOT-VEGETATION archive in Europe. IGARSS 2015.
- Rousseau, C., et al. 2015. Snow cover anomalies from 2000 to 2014 and highlight of two exceptional years over Europe. IGARSS 2015.
- Schamm, K., et al. 2014. Global gridded precipitation over land: GPCC first guess daily product. Earth Systems Science Data.
- Vuolo, F., et al. 2012. Data service platform for MODIS Vegetation Indices time series processing at BOKU Vienna. SPIE Proceedings.