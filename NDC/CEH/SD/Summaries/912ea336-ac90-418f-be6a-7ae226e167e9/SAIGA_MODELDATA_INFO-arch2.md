# Environmental conditions at saiga calving and die-off sites in Kazakhstan, 1979 to 2016

## Overview
- Examines environmental conditions at saiga calving and die-off sites within the Betpak-dala population (central Kazakhstan) from 1979 to 2016.
- Focuses on mass mortality events (MMEs) linked to Pasteurella multocida, typically occurring in May during calving when saigas aggregate.
- Data support modelling of the probability of MMEs at calving aggregations; details align with Kock et al. (2018).

## Study context and aims
- Saiga MMEs (notably in 1981, 1988, 2015) investigated in the Betpak-dala population, the only Kazakh population with recorded massive die-offs.
- A set of environmental predictor variables was used to model MME probability at calving aggregations.
- A full shapefile (214 sites) and site metadata are available; a subset of 135 sites contains necessary predictor data for modelling.
- Modelling process and results described in Kock et al. (2018).

## Data scope and sites
- 214 calving/die-off sites represented in the accompanying shapefile; 135 sites with adequate predictor data available for analysis.
- Population focus: Betpak-dala, central Kazakhstan (one of three saiga populations in the country).
- Data include onset dates (calving or death), year, and a dependent variable Dieoff (1 = die-off, 0 = normal calving).

## Environmental data sources
- Climate data: ERA-Interim daily reanalysis (ECMWF) used for temperature, humidity, precipitation, soil moisture, snow depth, wind, etc.
  - Daily aggregates created from 3- or 6-hourly data (means, maxima, minima, totals).
  - Precipitation uncertainty addressed with GPCC gauge-based products (from 1988 onward).
- Vegetation and snow indicators:
  - NDVI: 7-day filtered MODIS NDVI (Vienna data) for absolute values (subset of 94 sites, 2001–2016); NDVI anomaly data from SPOT/PROBA-V LifeWatch WB (1998–2016; subset ~96 sites).
  - Snow: Snow depth data; snow anomalies derived by LifeWatch WB (2000–2016; subset ~95–96 sites).
- Data integration relies on linking environmental rasters to site locations via site shapefile attributes.

## Data extraction and processing
- Time reference: the “zero hour” is the start of calving or the index case for MMEs.
- Predictor aggregation windows:
  - Primary metrics computed over 3, 5, and 10 days before onset.
  - Additional metrics: precipitation in the two months leading to onset.
  - Temperature variability metrics include: daily temp variation, overall temp variation, and max/min temp differences over 3, 5, and 10 days before onset.
  - Snow melt timing: date of last three consecutive snow-covered days; metrics for length of snow cover and days between snow melt and calving/onset.
  - NDVI and snow/NDVI anomaly metrics calculated for various pre-onset periods and fixed calendar windows (e.g., last weeks of March/April).
- Data handling for incomplete dates:
  - When calving dates were missing, metrics were generated using fixed dates (May 9 for start, May 14 for peak calving) and when possible, real dates were used.
  - A mixed-onset dataset (STGNONSET) was created by combining real dates with generalised estimates for modelling purposes.
- Result: a database of 135 sites with diverse climate metrics aggregated to relevant pre-onset periods, plus site metadata and the Dieoff indicator.

## Predictor variables and dataset structure
- Core metric naming follows a structured convention, with variations such as:
  - Core field names (original metric values, some with missing data)
  - Suffix _STGN for metrics up to May 9
  - Suffix _PKGN for metrics up to May 14
  - Suffix _STGNONSET for estimates based on real plus generalized onset dates
- Dataset fields include:
  - Site metadata, ID, Dieoff, Year, Population, Calving_START and Calving_PK (start and peak calving dates), onset-related fields, and numerous precipitation, temperature, soil moisture, wind, humidity, and NDVI/SNOW metrics (e.g., TOTPRECIP_3D, GPCC_PRECIP_5D, MINTEMP_10D, MAXTEMP_10D, TEMPAV_5D, AVRHUMID_MEAN10D, WINDGUST_MNOFMAX5D, SNOWMELT_JD, NDVI_MEAN40D, SNOWANOM_MEAN_APRW4, etc.).
- The attached dataset lists 135 sites with predictor metrics aligned to onset dates, along with onset, death observations, and the Dieoff outcome.

## Modelling and outputs
- Predictor variables were developed to feed multivariate models assessing the probability of MME at calving aggregations.
- See Kock et al. (2018) for modelling approach, selection of variables, and results.
- The dataset supports analyses that examine environmental triggers and their relation to MME risk across sites and years.

## Data access and references
- Shapefile and site metadata with provenance are available via the provided data repository.
- Key sources and references include ERA-Interim (Dee et al. 2011), GPCC precipitation data (Schamm et al. 2014), MODIS NDVI (Vuolo et al. 2012), SPOT/PROBA-V NDVI anomalies (Radoux et al. 2015), and foundational modelling in Kock et al. (2018).
- The dataset and methods enable standardized monitoring and analysis of environmental conditions related to saiga MMEs, with an emphasis on enabling broader data use and sharing.