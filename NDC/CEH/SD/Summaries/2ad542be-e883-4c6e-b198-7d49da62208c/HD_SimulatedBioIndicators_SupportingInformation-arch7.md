# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Overview
- A dataset from the Historic Droughts project (2014-2018) linking hydrometeorological drought indicators to aquatic biotic health proxies.
- Focuses on three biological indicators as proxies for river ecological health: ASPT (Average Score Per Taxon), LIFE at the Family level (LIFE_F), and LIFE at the Species level (LIFE_S).
- Data derived from BIOSYS biorecords (Environment Agency) for England, with context across drought surveillance sites.

## Spatial and Temporal Scope
- Spatial: 86 bio-monitoring sites matched to 76 EA gauging stations; includes SITE_ID, STATION_ID, and British National Grid coordinates (EASTING, NORTHING).
- Temporal: 1964–2012 (biological data largely 1984–2011 for inputs; outputs cover 1964–2012).
- Observations are twice-yearly (autumn and spring) with seasonality and potential long-term trends.

## Data Structure and Formats
- Outputs provided as CSV files, including:
  - HD_Bio_Indicators_Site_Location: site and matching gauging station details.
  - For each indicator (ASPT, LIFE_F, LIFE_S):
    - HD_Input_<Indicator>_ENG_WLS_1985-2011: observed, de-trended and de-seasonalised input data.
    - HD_Output_<Indicator>_ENG_WLS_1964-2012: modeled, de-trended and de-seasonalised output data.
- Key headers may include: SITE_ID, EASTING, NORTHING, STATION_ID, SAMPLE_ID, DATE_OBS, DATE_MOD, YEAR_0, SEASON, ASPT/LIFE_F/LIFE_S, DTDS_ASPT/DTDS_LIFE_F/DTDS_LIFE_S (de-trended/de-seasonalised values), SSI6 and SSI6 lagged predictors, MOD_ASPT/MOD_LIFE_F/MOD_LIFE_S (model outputs).

## Indicators and Predictors
- Biological indicators:
  - ASPT: Observed and modeled de-trended/de-seasonalised values.
  - LIFE_F: LIFE index at the family level (observed and modeled).
  - LIFE_S: LIFE index at the species level (observed and modeled).
- Hydrological predictor:
  - SSI6: Standardised Streamflow Index over a 6-month accumulation, with six lagged values (6–36 months prior) used as predictors.
- Modelling approach:
  - Three ML models (one per indicator) using a two-level structure (data level and site level).
  - Multi-Model Inference (MMI) to derive a set of good models and combine them for final predictions.
  - Outputs represent detrended and deseasonalised series across 1964–2012, based on the SSI6 framework.

## Methods and Processing
- Data preparation:
  - Biorecords from BIOSYS with seasonal sampling (Autumn and Spring) were detrended and deseasonalised via linear regression per site.
  - SSI6 calculated for 76 paired gauging stations; included current month and six lag terms as predictors.
- Analytical approach:
  - Separate ML models per indicator; two levels: site and data.
  - MMI to avoid over-reliance on a single best model; uses the weighted average of a good-model set.
- Considerations:
  - Biological indicators typically show an annual positive trend, likely due to improving water quality in recent decades, with seasonal variation (Spring higher than Autumn).
  - Some sites have shorter records; variability in sample counts and periods across sites.

## GIS-Relevant Considerations
- Enables spatial mapping of ecological health indicators across the UK river network.
- Coordinates (Easting/Northing) and site-to-station linkages facilitate spatial joins, buffering, and habitat relationship analyses.
- Outputs support mapping of modeled ecological health against hydrological drought stress (SSI6) to identify hotspots and temporal trends (1964–2012).

## Data Quality and Accessibility
- Data derived from a reputable national monitoring program (Environment Agency BIOSYS); rights held by EA.
- Periodicity and coverage vary by site; some data limited to specific sub-periods.
- Acknowledges ongoing work with detailed methodology described in a related paper (in preparation).

## Dataset Use and Citations
- Data files and outputs are intended for environmental and hydrological analyses, particularly examining the response of biotic indicators to drought-related hydrological stress.
- Key references include foundational works on the Standardised Streamflow Index (Barker et al., 2016; Svensson et al., 2017) and the BIOSYS data source from the Environment Agency.