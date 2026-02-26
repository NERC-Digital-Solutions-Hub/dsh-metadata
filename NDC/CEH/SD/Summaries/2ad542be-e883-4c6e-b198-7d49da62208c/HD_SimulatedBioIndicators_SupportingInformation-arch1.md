# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Context
- Part of the Historic Droughts project (2014-2018, £1.5m) involving eight UK institutions to understand past UK droughts and improve future management tools.
- Droughts and water scarcity (DWS) threaten livelihoods; need to understand links between hydrometeorological and social systems.
- Aim: develop interdisciplinary understanding of drought through hydrometeorological, environmental, agricultural, regulatory, social, and cultural perspectives; characterize UK drought/water-scarcity history since the late 19th century.

## Motivation
- Investigate how three biological indicators respond to discharge: ASPT (Average Score Per Taxon), LIFE Family (LIFE at family level), and LIFE Species (LIFE at species level).
- Data sourced from Environment Agency BIOSYS long-term bio-monitoring in England; indicators serve as proxies for ecological health of river reaches.
- Discharge characterized by Standardised Streamflow Index (SSI), specifically SSI6 (6-month accumulation) tailored for drought studies.

## Methods
- Raw data: twice-yearly indicators (autumn and spring) from BIOSYS for 86 sites matched to 76 EA gauging stations (≈1950 data-points; period roughly 1984-2011).
- Pre-processing: detrend and deseasonalise indicators via site-specific linear regressions with season and year as predictors; use residuals as DTDS (de-trended/de-seasonalised) indicators.
- SSI6: computed for 76 paired stations for 1964-2012; uses six-month accumulation with Tweedie distribution.
- Predictors: SSI6 for sampling month plus six lagged SSI6 values at 6–36 months prior.
- Modeling: three Multi-Level (ML) models (one per bio-indicator) with two levels (data and site) and Multi-Model Inference (MMI) to average across a set of good models.
- Output: final dataset of simulated de-trended/de-seasonalised ASPT, LIFE Family, and LIFE Species for 1964-2012.
- Note: a paper detailing methods and data is in preparation.

## Data Format and Contents
- CSV files organized as inputs and outputs for each indicator:
  - HD_Bio_Indicators_Site_Location: site location and matching gauging station
  - HD_Input_ASPT_ENG_WLS_1985-2011: observed and de-trended/de-seasonalised ASPT
  - HD_Output_ASPT_ENG_WLS_1964-2012: modelled ASPT (DTDS and final)
  - HD_Input_LIFE_FAMILY_ENG_WLS_1985-2011: observed/de-trended LIFE Family
  - HD_Output_LIFE_FAMILY_ENG_WLS_1964-2012: modelled LIFE Family
  - HD_Input_LIFE_SPECIES_ENG_WLS_1985-2011: observed/de-trended LIFE Species
  - HD_Output_LIFE_SPECIES_ENG_WLS_1964-2012: modelled LIFE Species
- Key headers across files (depending on file):
  - SITE_ID, EASTING, NORTHING (British National Grid)
  - STATION_ID (matched National River Flow Archive gauging station)
  - SAMPLE_ID, DATE_OBS, DATE_MOD
  - YEAR_0 (centered year around 1998), SEASON (Au/Sp)
  - ASPT, LIFE_F, LIFE_S (observed)
  - DTDS_ASPT, DTDS_LIFE_F, DTDS_LIFE_S (de-trended/de-seasonalised dependent variables)
  - SSI6 (6-month SSI), SSI6_6M_LAG, SSI6_12M_LAG, SSI6_18M_LAG, SSI6_24M_LAG, SSI6_30M_LAG, SSI6_36M_LAG (predictors)
  - MOD_ASPT, MOD_LIFE_F, MOD_LIFE_S (modelled outputs)
- Temporal coverage:
  - Observed inputs: roughly 1985-2011
  - Model outputs: 1964-2012
  - Spanning drought-relevant periods and longer historical context

## Data Provenance and Access
- Acknowledgement: Historic Droughts Project, grant NE/L01016X/1
- Foundational references:
  - Standardised Streamflow Index development (Barker et al. 2016; Svensson et al. 2017)
  - BIOSYS bio-monitoring data from Environment Agency England (c. 2011-2012 version; currently downloadable from data.gov.uk)
- Project scope: drought-surveillance subset of EA network; spring samples tend to have higher indicator scores than autumn.

## Notes and Considerations
- Biological indicators show an overall positive long-term trend in UK records, partially due to improving water quality, with notable seasonal variation.
- The combination of hydrological predictors (SSI6 and lags) with multi-level modelling allows estimation of ecological responses across sites with differing baselines.
- Data handling includes methodological steps to ensure comparability across sites with differing sampling histories.