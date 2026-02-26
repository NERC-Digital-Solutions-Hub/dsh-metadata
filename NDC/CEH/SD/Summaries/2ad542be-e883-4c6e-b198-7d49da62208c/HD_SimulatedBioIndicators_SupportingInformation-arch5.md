# Simulated Monthly Biological Indicators for England and Wales 1964-2012

## Context and Aim
- Part of the Historic Droughts project (2014-2018) aimed at interdisciplinary understanding of UK droughts to improve future drought management.
- Project involved eight UK institutions and linked hydrometeorological, environmental, agricultural, regulatory, social, and cultural perspectives.
- This dataset investigates the response of three biological indicators to discharge: ASPT (Average Score Per Taxon), LIFE at Family level (LIFE_F), and LIFE at Species level (LIFE_S).
- Indicators are derived from BIOSYS bio-monitoring data provided by the Environment Agency (EA) for drought-surveillance sites in England and Wales.
- Discharge is characterized by the Standardised Streamflow Index (SSI), specifically SSI6 (6-month accumulation), with predictors including lagged SSI6 values.

## Data Provenance and Scope
- Data come from BIOSYS (Environment Agency) circa 2011-2012 subset used for drought surveillance.
- Study uses 86 biological sites matched to 76 EA gauging stations, with about 1950 data-points spanning roughly 1984-2011 for inputs; the final simulated dataset covers 1964-2012.
- Biological indicators provide snapshots of invertebrate communities as proxies for river ecological health at sampling time.
- Output files present simulated (modelled) de-trended and de-seasonalised indicator series across 1964-2012.

## Indicators and Data Sources
- Indicators:
  - ASPT = Observed Average Score Per Taxon
  - LIFE_F = LIFE at the Family level
  - LIFE_S = LIFE at the Species level
- Data sources:
  - BIOSYS bio-monitoring records (EA), subset from EA freshwater invertebrates England dataset (circa 2011-2012)
  - SSI6 as the drought-related predictor, with 6-month accumulation and six lagged values (6–36 months prior)

## Methods and Processing
- Data preparation:
  - Twice-yearly bio-indicator series (autumn and spring) extracted from BIOSYS for the 86 sites and 76 gauging stations (approx. 1950 data-points; period ~1984-2011).
  - Trends and seasonality removed: linear regression per site with season and year as predictors; fitted values subtracted to create de-trended/deseasonalised indicators.
- SSI6 calculation:
  - 6-month accumulation period; SSI6 used as predictor alongside six lagged SSI6 values (6, 12, 18, 24, 30, 36 months prior).
- Modelling approach:
  - Three separate Multi-Level (ML) models (one per indicator) with two levels: data (level 1) and site (level 2).
  - Multi-Model Inference (MMI) used to select sets of good models; the final model is an average across the good-model set.
  - Models run on the full SSI dataset to produce final simulated de-trended/de-seasonalised series for 1964-2012.
- Outputs:
  - Final dataset includes simulated indicators for ASPT, LIFE_F, and LIFE_S with corresponding predictor variables.

## Data Formats and Variable Details
- Files (CSV) and their purpose:
  - HD_Bio_Indicators_Site_Location: Biological sampling site location and matching gauging station
  - HD_Input_ASPT_ENG_WLS_1985-2011: Observed and de-trended/de-seasonalised ASPT
  - HD_Output_ASPT_ENG_WLS_1964-2012: Modelled de-trended/de-seasonalised ASPT
  - HD_Input_LIFE_FAMILY_ENG_WLS_1985-2011: Observed and de-trended/de-seasonalised LIFE Family-level
  - HD_Output_LIFE_FAMILY_ENG_WLS_1964-2012: Modelled de-trended/de-seasonalised LIFE Family-level
  - HD_Input_LIFE_SPECIES_ENG_WLS_1985-2011: Observed and de-trended/de-seasonalised LIFE Species-level
  - HD_Output_LIFE_SPECIES_ENG_WLS_1964-2012: Modelled de-trended/de-seasonalised LIFE Species-level
- Common headers (example):
  - SITE_ID, STATION_ID, SAMPLE_ID
  - DATE_OBS, DATE_MOD
  - YEAR_0, SEASON
  - ASPT, LIFE_F, LIFE_S (observed)
  - DTDS_ASPT, DTDS_LIFE_F, DTDS_LIFE_S (de-trended/de-seasonalised dependent variables)
  - SSI6, SSI6_6M_LAG, SSI6_12M_LAG, SSI6_18M_LAG, SSI6_24M_LAG, SSI6_30M_LAG, SSI6_36M_LAG
  - MOD_ASPT, MOD_LIFE_F, MOD_LIFE_S (modelled outputs)
- Coordinates and identifiers:
  - EASTING, NORTHING (British National Grid)
  - DESCRIPTIONS for site and station associations
- Versioning and period:
  - Observed inputs cover circa 1985-2011; outputs cover 1964-2012

## Data Quality, Limitations, and Governance
- Data are subject to features typical of ecological time series: year-to-year variability and seasonal patterns; detrending and deseasonalising applied to improve comparability.
- Methods and data are described as part of a manuscript in preparation, with full methodological detail to follow.
- Data rights and references:
  - Acknowledgement to Historic Droughts Project (grant NE/L01016X/1)
  - Related methodological references for SSI and biological indicators
  - BIOSYS data rights are held by the Environment Agency

## Access, Reuse, and Stewardship Considerations
- Data are provided as CSV files with explicit input and modelled output components for transparency and reproducibility.
- Clear documentation of data lineage (BIOSYS to EA, site-station mappings, detrending/deseasonalising steps) supports data governance and reuse.
- For ongoing stewardship, consider:
  - Maintaining metadata on data provenance, transformation steps, and model configurations (ML/MMI setups, site-level effects)
  - Versioning and updates if BIOSYS or SSI methodologies change
  - Licensing and usage rights, given EA copyright and BIOSYS data rights
  - Potential future releases or updates aligned with the referenced forthcoming paper and related publications