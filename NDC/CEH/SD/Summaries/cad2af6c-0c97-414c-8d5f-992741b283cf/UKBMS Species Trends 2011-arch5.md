# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Butterfly abundance is estimated using standardized methods (all-species transects, timed counts, egg/larval web counts) to enable year-to-year comparison.
- Data are organized to reflect habitat/management units and sampling effort across sites and years.

## Data collection methods
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free), either by the recorder or regional transect coordinators.
- Transect Walker files uploaded into an Oracle database containing all records.
- Each transect coordinator is responsible for compiling data for all sites within their region after each monitoring season.

## Experimental design details
- All-species transects: fixed-route lines (2–4 km) with 5 m recording bands; weekly counts from April to September; routes fixed to allow year-to-year comparisons.
- Single-species transects: follow all-species methodology but target one focal species for a few weeks during the flight period.
- Timed counts: fixed area and time period within suitable weather; counts focus on a specific species.
- Egg/larval web counts: count eggs or larval webs in suitable habitat areas.
- Weather and activity constraints: observations occur between 10:45 and 15:45 under conditions favorable to butterfly activity (specific temperature, sunshine, wind limits).

## Analytical methods
- After validation, a General Additive Model (GAM) imputes missing values and computes site indices.
- Collated Index: national annual index per species, derived by combining site indices and adjusting for varying site participation (uses log10 of indices).
- Missing values and trends: log-linear regression estimates missing indices and provides overall trends for each species since 1976.
- Timeframe for trends:
  - Whole series (1976–2011)
  - Last 20 years (1992–2011)
  - Last 10 years (2002–2011)
- Notes on data: Collated Indices can change as new data are added; not all species have complete early-year data.

## Nature and units of recorded values
- Site indices are relative measures of population size, proportional to actual abundance, and linked to other population measures.
- Indices are transformed to Log10 for Collated Indices, with the series standardized so the average is 2.
- Trends are expressed as the slope of the index over time; detailed outputs include years, standard errors, p-values, and qualitative trend descriptions (rapid decline, rapid increase, or stable).

## Quality control
- Automatic validation in Transect Walker flags anomalous records (e.g., unusually high counts, out-of-season records); recorders can adjust or confirm.
- Regional coordinators review site data for questionable entries, followed by automated/manual validations against known distributions and flight periods.
- Additional checks ensure data consistency with distribution ranges and typical seasonal activity.

## Format of stored data
- Species Trends stored as CSV with columns including:
  - Species, Common name
  - No.years (years contributing to the trend)
  - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
  - 20-yr/10-yr slopes, Std.Err, P-values, Trends, and % changes
- Descriptions detail the meaning of each column (e.g., trend classifications like Rapid decline, Rapid increase, Stable).