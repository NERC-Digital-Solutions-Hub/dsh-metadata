# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Context and Aim
- Part of the Historic Droughts project (2014–2018, £1.5m) to develop cross-disciplinary understanding of UK droughts and improve management tools.
- Aims to investigate how three bio-indicators respond to discharge: ASPT (Average Score Per Taxon), LIFE at the family level (LIFE F), and LIFE at the species level (LIFE S).
- Data sourced from Environment Agency BIOSYS biobanking; discharge represented by the Standardised Streamflow Index (SSI), specifically SSI6 for drought-focused analysis.

## Data and Scope
- Biological data from 86 sites matched to 76 EA gauging stations; ~2,000 data-points across 1984–2011 for raw indicators; outputs cover 1964–2012.
- Twice-yearly sampling (autumn and spring); observed indicators show an overall positive trend with seasonal variation (spring higher than autumn).
- The dataset provides a simulated, de-trended, and de-seasonalised series for the three indicators.

## Methods and Modelling
- Pre-processing: detrend and de-seasonalise bio-indicator time series by fitting site-specific linear models with season and year as predictors.
- Hydrological predictor: SSI6 (6-month accumulation) with seven predictors: SSI6 in the sampling month plus six lagged SSI6 values (6–36 months prior).
- Modelling approach: Three multi-level (two-level: data and site) models using Multi-Model Inference (MMI) to select a set of good models rather than a single best model.
- Outputs: final simulated, de-trended, de-seasonalised ASPT, LIFE F, and LIFE S series for 1964–2012.
- Documentation: a related methods paper is in preparation.

## Data Format and Contents
- CSV files include:
  - HD_Bio_Indicators_Site_Location: site locations and matching gauging stations.
  - HD_Input_ASPT_ENG_WLS_1985-2011: observed and de-trended/de-seasonalised ASPT (input).
  - HD_Output_ASPT_ENG_WLS_1964-2012: modelled DTDS ASPT (output).
  - HD_Input_LIFE_FAMILY_ENG_WLS_1985-2011: observed and de-trended/de-seasonalised LIFE F (input).
  - HD_Output_LIFE_FAMILY_ENG_WLS_1964-2012: modelled DTDS LIFE F (output).
  - HD_Input_LIFE_SPECIES_ENG_WLS_1985-2011: observed and de-trended/de-seasonalised LIFE S (input).
  - HD_Output_LIFE_SPECIES_ENG_WLS_1964-2012: modelled DTDS LIFE S (output).
- Key headers include SITE_ID, EASTING/NORTHING, STATION_ID, SAMPLE_ID, DATE_OBS, DATE_MOD, SEASON, ASPT, LIFE_F, LIFE_S, DTDS_ASPT, DTDS_LIFE_F, DTDS_LIFE_S, SSI6 and SSI6Lag indicators, and MOD_* modelled outputs.

## Data Quality and Context
- Observed time-series trends likely reflect improvements in river water quality alongside natural and seasonal variability.
- Sampling period and data availability vary by indicator and site (inputs: ~1985–2011; outputs: 1964–2012).
- The dataset is designed for reuse in monitoring and policy evaluation, with a focus on integrating hydrological drought signals and biological responses.

## Access, Acknowledgements, and References
- Acknowledges the Historic Droughts Project (grant NE/L01016X/1) and Environment Agency BIOSYS data.
- References related to the SSI methodology and biological indicators are provided for methodological context.