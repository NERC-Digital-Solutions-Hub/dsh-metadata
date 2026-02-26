# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Context and Aims
- Part of the Historic Droughts project (2014-2018; £1.5m) to develop cross-disciplinary understanding of past UK droughts and improve drought management tools.
- Involves eight UK institutions and aimed to integrate hydrometeorological, environmental, regulatory, social and cultural perspectives.
- This dataset investigates how three biological indicators respond to river discharge: ASPT, LIFE at the family level (LIFE-F), and LIFE at the species level (LIFE-S).

## Data Sources and Scope
- Biological indicators sourced from Environment Agency BIOSYS data (circa 2011-2012 snapshot).
- Observed indicators derived from a subset of EA’s Freshwater and Marine Biological Surveys for Invertebrates England (BIOSYS); current BIOSYS is accessible via data portals.
- Discharge represented by Standardised Streamflow Index (SSI), specifically SSI6 (6-month accumulation) tailored for drought studies.
- Spatial/temporal coverage: 86 biological sites matched to 76 EA gauging stations; roughly 1,950 data points across 1964-2012 (with observed data primarily 1985-2011 for inputs).

## Methods and Modelling Approach
- Data processing:
  - Biological records show a general annual positive trend with seasonal variation (spring higher than autumn).
  - Detrending and de-seasonalising performed per site using linear regression with season and year as predictors; residuals used as input for analysis.
- SSI6 construction:
  - SSI6 calculated for 76 paired stations with a 6-month accumulation, using a Tweedie distribution.
  - Seven predictors composed of SSI6 for the sampling month and six lagged SSI6 values (6 to 36 months prior).
- Modelling framework:
  - Three separate multi-level models (one per bio-indicator) with two levels: observations (level 1) and site (level 2).
  - Multi-Model Inference (MMI) used to select sets of good models; final estimates are model-averaged.
  - Final output consists of simulated de-trended/de-seasonalised indicator series for 1964-2012.
- Documentation note: a detailed methods paper is in preparation.

## Data Format and Outputs
- Provided as CSV files, including:
  - HD_Bio_Indicators_Site_Location: site locations and matched gauging stations.
  - HD_Input_ASPT_ENG_WLS_1985-2011 and HD_Output_ASPT_ENG_WLS_1964-2012: observed and modelled AS PT (de-trended/de-seasonalised).
  - HD_Input_LIFE_F_ENG_WLS_1985-2011 and HD_Output_LIFE_F_ENG_WLS_1964-2012: observed and modelled LIFE at family level.
  - HD_Input_LIFE_S_ENG_WLS_1985-2011 and HD_Output_LIFE_S_ENG_WLS_1964-2012: observed and modelled LIFE at species level.
- Key headers include SITE_ID, STATION_ID, coordinates, SAMPLE_ID, dates, SEASON, ASPT/LIFE metrics, de-trended/de-seasonalised values, SSI6 and lag predictors, and MOD_ indicators for modelled outputs.

## Data Quality, Provenance, and Governance
- Data lineage roots in the Historic Droughts project; acknowledges EC grants and EA data rights.
- Raw data derived from BIOSYS with adjustments to remove trends/seasonality before modelling.
- Outputs are model-based estimates (not direct observations) intended to support drought-related ecological analyses.
- References provided for the SSI methodology and for BIOSYS data source.

## Potential Uses and Considerations for Data Leaders
- Governance: clear data provenance, transformation steps, and modelling approach support reproducibility and auditability.
- Data integration: links biological indicators to hydrological context (SSI6) enable cross-domain drought analytics and ecosystem health assessments.
- Accessibility: multiple CSV files with standardized headers facilitate discoverability and reuse; attention to data rights (Environment Agency) and updated BIOSYS access needed for future use.
- Limitations: inputs largely cover 1985-2011; outputs span 1964-2012; model-based estimates depend on MMI assumptions and the quality of BIOSYS and SSI6 data.
- Collaboration potential: dataset aligns with cross-institutional drought research and could support broader data-community efforts in ecological response to hydrological extremes.