# UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects and analyzes butterfly data from over 1,000 sites annually across the UK, using standardized methods to enable year-to-year comparisons and national trend estimates.

## Experimental design and data collection regime
- All-species transects (Pollard walk): fixed-route transects (2–4 km) walked weekly under suitable weather, subdivided into habitat/management units; 5 m wide strip records all species.
- Transects are fixed to enable comparability across years; typically 26 counts per year from early April to late September.
- Weather constraints for transects: dry, wind < Beaufort 5; temperature thresholds (≥13°C with ≥60% sunshine or >17°C if overcast).
- Data capture includes:
  - All-species transects
  - Single-species transects (recorded only during focal species’ flight period, a subset of weeks)
  - Timed counts (abundance of a species over a set time/area)
  - Egg/larval web counts (e.g., Marsh Fritillary) in suitable habitat areas

## Data collection methods
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free download via UKBMS website) by the recorder or regional transect coordinator.
- Transect Walker data uploaded to an Oracle database housing all records.

## Analytical methods
- Data validation followed by a General Additive Model (GAM) to impute missing values and compute a site index.
- Site indices are combined to produce a national annual Collated Index (for each species); because not all sites are monitored every year, a log10 transformation (LCI) is used for reporting.
- Missing values and trends are estimated with a log-linear regression model, accounting for year effects (weather-related variability) and site effects (differences among sites).
- Collated Indices are updated annually as new monitoring data are added; earlier years’ indices may be revised.
- Species trends are derived by linear regression on the Collated Indices:
  - Whole time series (1976–2011 in the report)
  - Last 20 years (1992–2011)
  - Last 10 years (2002–2011)
- Some species have shorter trend series due to insufficient data in earlier years.

## Nature and units of recorded values
- Site index: a relative measure of population size (not absolute), proportional to actual population, with detectability varying by species.
- Collated Indices are reported as Log10 Collated Index (LCI), scaled so the series average equals 2.
- Trends reported as slope values with associated p-values, standard errors, and qualitative trend descriptions (rapid decline/increase or stable) for the overall series, 20-year, and 10-year intervals.
- Outputs include percentage change over the full series, 20-year, and 10-year windows.

## Quality control
- In-field automatic checks in Transect Walker flag abnormal counts or flights outside expected periods; recorders can accept or adjust flagged data.
- Regional transect coordinators review data for questionable entries.
- Additional automated and manual validation steps check:
  - Records of species outside known distribution ranges
  - Records outside normal flight periods
  - First-time records at a site
  - Extreme or abnormal abundances

## Format of stored data
- Stored as CSV with columns including:
  - Species (scientific name per Fauna Europaea)
  - Common name
  - No.years (years included in the series)
  - Series slope, Series Std.Err, Series P-value, Series trend, Series % change
  - 20-yr Slope/Std.Err/P-value/Trend/% change
  - 10-yr Slope/Std.Err/P-value/Trend/% change
- Additional metadata includes the 20-year and 10-year trend descriptors and statistical significance indicators.