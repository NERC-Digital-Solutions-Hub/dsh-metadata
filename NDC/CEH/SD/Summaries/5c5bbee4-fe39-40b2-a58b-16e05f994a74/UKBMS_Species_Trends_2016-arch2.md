# UK Butterfly Monitoring Scheme (UKBMS) methodology

## Overview
- The UKBMS aggregates data from over 2,000 sites annually across the UK to monitor butterfly populations.
- Data collection uses standardized transect-based methods with variations for coverage and effort.
- The goal is to produce comparable, long-term indicators of environmental health and policy-relevant trends.

## Experimental design / sampling regime
- All-species transects (Pollard walks): fixed routes, weekly counts April–Sept, 2–4 km routes, ~26 visits/year, 5 m wide recording band, weather-conditional sampling.
- Transect routes fixed to allow year-to-year comparisons; routes cover habitat/management variation within sites.
- Weather constraints for transects: 10:45–15:45, dry conditions, wind ≤ Beaufort 5, 13°C+ with ≥60% sunshine or >17°C if overcast.
- Single-species transects: follow all-species methodology but only in selected weeks for focal species.
- Timed counts: species-specific counts over a set time/area, weather-conditional like transects.
- Egg/larval web counts: record eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).
- Wider Countryside Butterfly Survey (WCBS, established 2009): reduced-effort sampling in farmland and wider countryside; two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits/year (minimum 2 visits in July/August; spring visits encouraged).

## Data collection and entry
- Field data recorded on standard forms; entered online via UKBMS data entry site or Transect Walker software.
- Data entry can be by recorders or regional transect coordinators; coordinators compile data for their region.
- Online data and Transect Walker files are uploaded to an Oracle database housing all records.

## Analytical methods
- Two main approaches, depending on species group:
  - Wider countryside species (mobile, wide habitat range):
    - Two-stage model using all counts from all survey types.
    - Stage 1: Generalized Additive Model (GAM) to estimate annual seasonal flight pattern; derive daily values and standardize to a year-specific pattern.
    - Stage 2: Full annual counts model with seasonal values as an offset; estimates annual abundance changes accounting for varying seasonality.
    - Method described in Dennis et al. 2013.
  - Habitat specialists and regular migrants (less WCBS data; use reduced-effort data like timed counts/larval counts):
    - GAM to impute missing values and compute site indices.
    - Site indices combined to produce a national annual Collated Index; missing values and year/site effects handled via log-linear regression.
    - Collated Indices updated annually as new data arrive; trends calculated on the Collated Indices.
- Trends calculated by linear regression on species trends:
  - Whole time series (1976–2016)
  - Last 20 years (1997–2016)
  - Last 10 years (2007–2016)
- Key definitions:
  - Collated Indices are log10-transformed; scaled so the average index over the series equals 2.
  - Site indices are relative (not absolute) population measures.
  - Trends expressed as slope of the Collated Index over time; include p-values to indicate significance.

## Population groups and definitions
- Wider countryside species: mobile species across a range of habitats.
- Habitat specialists: low-mobility, primarily semi-natural habitats.
- Regular migrants: species overwintering outside the UK or migrating in yearly from continental Europe.
- Note: Red Admiral exhibits resident populations in parts of the UK but is generally considered migratory.

## Quality control
- Automatic checks in Transect Walker flag potential data entry errors (e.g., anomalous counts, records outside flight periods).
- Regional transect coordinators verify data; continuous validation throughout the season.
- Post-entry validation includes checks for records outside known distribution, anomalous timing, first-time site records, extreme abundances, and unusual site-year variation.

## Data structures and storage
- Outputs stored as CSV files with fields including:
  - Sci_Name, Common_name, No_years, Series_slope, Series_Std_Err, Series_P_value, Series_trend, Series_%_change
  - 20_yr_Slope, 20_yr_Std_Err, 20_yr_P_value, 20_yr_Trend, 20_yr_%_change
  - 10_yr_Slope, 10_yr_Std_Err, 10_yr_P_value, 10_yr_Trend, 10_yr_%_change
- Series and trend descriptions reflect statistical significance (e.g., Rapid decline/increase vs Stable).
- Dataset references and background methods cited (e.g., Moss & Pollard 1993; Rothery & Roy 2001; Dennis et al. 2013; Journal of Applied Statistics; Methods in Ecology and Evolution).

## Nature and units of recorded values
- Site indices: relative population size, proportional to actual abundance; not an absolute count.
- Collated Indices: expressed as Log10 values; standardized so mean equals 2 for comparability.
- Trends: reported as slopes (change per year) with associated standard errors and p-values.