# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Uses standardized methods to monitor butterfly populations and derive indices and trends for environmental health assessments.

## Sampling design
- All-species transects:
  - Fixed-route line transect at a site; all butterflies recorded weekly from April to September.
  - Transects 2–4 km long, divided into habitat/management units, typically 5 m wide, yielding about 26 counts per year.
  - Transects are fixed to allow year-to-year comparison; counts occur under suitable butterfly-weather conditions.
  - Walking window: 10:45 am to 3:45 pm; weather criteria: dry, Beaufort wind ≤5, temperature thresholds (≥13°C with ≥60% sunshine or ≥17°C if overcast).
- Single-species transects:
  - Similar to all-species but focused on one focal species during select weeks.
- Timed counts:
  - Abundance of a target species recorded over a set time and area, under the same daily time window and weather criteria.
- Egg/larval web counts:
  - Recording eggs or larval webs in suitable habitats (e.g., Marsh Fritillary).

## Data collection and storage
- Field data on standard recording forms.
- Entered into Transect Walker software (free, UKBMS website).
- Data entered by recorders or regional transect coordinators; coordinators compile data for their region.
- Transect Walker files uploaded to an Oracle database housing all records.

## Analytical methods
- Data validation and cleaning precede analysis.
- Statistical modeling:
  - General Additive Model (GAM) to impute missing values and compute site indices.
  - Site indices aggregated into national Collated Indices per species.
  - Log-linear regression to estimate missing values and produce indices/trends, accounting for year and site effects.
- Time-series outputs:
  - Trends calculated for whole series (1976–2012), last 20 years (1993–2012), and last 10 years (2003–2012).
  - Some species have shorter trend series due to insufficient historical data in early years.

## Data format and interpretation
- Site indices are relative population measures (not absolute counts), related to other abundance measures.
- Collated Indices are presented as Log10 values; scaled so the average index over the series equals 2.
- Trends are reported as slopes (change per year) with associated p-values to indicate statistical significance.
- Dataset notes:
  - Collated Indices updated annually as new data are added; past values may shift slightly.
  - Some species’ trends have fewer contributing years; the dataset records the number of years contributing.

## Quality control
- Automatic data-entry checks in Transect Walker flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional coordinators validate records; additional automated and manual checks validate distribution, flight period, first-time site records, and extreme values.

## Outputs and underlying data
- Stored data format:
  - CSV with columns: Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change, 20-yr Slope, 20-yr Std.Err, 20-yr P-value, 20-yr Trend, 20-yr % change, 10-yr Slope, 10-yr Std.Err, 10-yr P-value, 10-yr Trend, 10-yr % change.
- Outputs include:
  - Per-species Collated Indices and trends over multiple timeframes.
  - Documentation of the number of contributing years per species.

## Access and software
- Transect Walker software available for download on the UKBMS site.
- Data stored in an Oracle database; ongoing updates ensure timely trend reporting.

## Challenges and opportunities
- Increasing the value of datasets by combining UKBMS data with other relevant environmental data (moving beyond single-use applications).
- Enabling broader access to the underlying data used to generate final outputs.