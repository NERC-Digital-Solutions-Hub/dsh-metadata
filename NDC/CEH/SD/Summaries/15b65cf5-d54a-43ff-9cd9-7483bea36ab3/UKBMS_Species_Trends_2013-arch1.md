# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, employing multiple recording methods to estimate butterfly abundance.
- All-species transects (Pollard walks) form the core method: fixed-route line transects, 2–4 km long, with a fixed width (about 5 m) and weekly counts from early April to late September, yielding up to 26 counts per year.
- Transect routes are selected to represent habitat types and management on sites and remain fixed to allow year-to-year comparability.
- Alternative methods used at some sites include single-species transects, timed counts, and egg/larval web counts during the focal species’ flight period.

## Data collection and transect types

- All-species transects: record all butterflies along the fixed route each week under specified weather conditions.
- Single-species transects: follow the all-species methodology but focus on one focal species during a subset of weeks.
- Timed counts: quantify a focal species over a set period and area.
- Egg/larval web counts: record eggs or larval webs in suitable habitat areas for particular species.

## Field procedures and scheduling

- Recording is conducted in the field on standard forms and later entered into Transect Walker software.
- Data entry can be done directly by the recorder or by a regional transect coordinator.
- Transect data are uploaded to an Oracle database; regional coordinators compile site data for their regions.

## Data capture and storage

- After collection, data pass validation and are stored in a central database, with ongoing updates as new monitoring data are received.

## Analytical methods

- Validation: automated checks in Transect Walker flag potential errors (e.g., unusually high counts, records outside flight periods); coordinators perform regional reviews.
- Data imputation and indexing:
  - General Additive Models (GAM) are used to impute missing values and derive site indices.
  - Collated Index (across sites) is produced by combining site indices; a log-linear regression models missing values and yields indices and trends.
  - Year effects and site effects are accounted for in the modeling framework.
- Trend analysis:
  - Linear regression on collated indices to produce a simple measure of abundance change over time since 1976.
  - Trends are provided for the full series, the last 20 years (1993–2013), and the last 10 years (2003–2013).
  - Some species have shorter trend series due to insufficient early data; gaps are indicated in the dataset.

## Nature and units of recorded values

- Site indices are relative measures of population size, proportional to actual abundance; they are not absolute counts.
- Collated Indices are presented as Log10(Collated Index) (LCI); indices are scaled so the average over the series equals 2.
- Trends are reported as slopes (change in the Collated Index per year) and accompanied by standard errors and P-values to indicate significance.
- Descriptions of trends (e.g., rapid decline, rapid increase, stable) are determined by the slope direction and statistical significance.

## Quality control and validation

- Automated checks identify anomalies (e.g., records outside known distributions or flight periods, first-time site records, extreme or unexpected abundances).
- Regional coordinators with local site knowledge verify records; follow-up validation ensures data quality before analysis.

## Data format and storage

- Species Trends are stored as CSV files with the following columns:
  - Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change
  - 20-yr Slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change
  - 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change

## Scale, timing and references

- Timeframe and scope:
  - Flight period: April to September; field recordings typically conducted 10:45–15:45 under suitable butterfly activity conditions.
  - Trends cover from 1976 onward, with annual updates as more data are incorporated.
- Foundational references include Pollard & Yates (1993), Rothery & Roy (2001), and Moss & Pollard (1993).