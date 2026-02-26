# UK Butterfly Monitoring Scheme (UKBMS) Methodology

- Overview
  - UKBMS collects data from over 1,000 sites yearly across the UK to monitor butterfly abundance and trends.
  - Uses standardized, fixed-route transects and alternative methods (timed counts, egg/larval web counts) for certain species or sites.
  - Data are processed, quality-controlled, analyzed, and stored in centralized databases; outputs include site-level indices, national collated indices, and species trends over multiple time periods.

- Experimental design / sampling regime
  - All-species transects: fixed-route line transect at each site; all butterflies recorded weekly under predefined weather conditions; routes are 2–4 km, divided into habitat/management sections; counts occur in a 5 m wide band, typically 26 counts per year from April to September.
  - Transects are conducted 10:45–15:45 and only when butterfly activity conditions are met (dry, wind < Beaufort 5, temperature thresholds with sunshine or overcast as specified).
  - Single-species transects follow the all-species method but target only specific species during a few weeks of their flight period.
  - Timed counts and egg/larval web counts: happen for focal species over set time/area; weather and time constraints similar to transects.

- Data collection methods
  - Field data recorded on standard forms; entered into Transect Walker software (free) by recorders or regional transect coordinators.
  - Regional coordinators compile data for their region; Transect Walker files uploaded to an Oracle database housing all records.

- Analytical methods
  - After validation, Generalized Additive Models (GAM) impute missing values and compute site indices.
  - Site indices are combined into a national Collated Index for each species; as not all sites are monitored every year, a log-linear regression estimates missing values to produce indices and trends.
  - Collated Indices are updated annually with new data; previous years’ indices may shift as data are incorporated.
  - Species are included in Collated Indices if recorded at five or more sites per year.
  - Trends are derived from linear regression on collated indices:
    - Time series: 1976–2011, 1992–2011, and 2002–2011.
  - Methodology references: GAM approach (Rothery & Roy, 2001) and collated index calculation (Moss & Pollard, 1993).

- Nature and units of recorded values
  - Site indices are relative measures, proportional to actual population size; they align with other abundance measures (e.g., mark–release–recapture).
  - Collated Indices are presented as log10 values, scaled so the series average equals 2, providing a relative population size over time.
  - Recorded trends are the slope (change per year) of the Collated Index.
  - Dataset fields (examples): Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change; 20-yr and 10-yr equivalents (slope, std.err, P-value, trend, % change).

- Quality control
  - Automatic data-entry checks in Transect Walker flag anomalies (e.g., out-of-season records, abnormally high counts).
  - Regional coordinators review records for plausibility and regional consistency.
  - Additional automated/manual validation to flag records outside known distributions, unusual flight periods, first-time site records, and extreme values.

- Format of stored data
  - Species Trends stored as CSV files; columns include species identifiers, years, slopes, p-values, trends, and percentage changes for series, 20-year, and 10-year periods.
  - Data documentation specifies species authority (scientific name), common name, and statistical metadata (years, slope, standard error, P-values, trend descriptions, and percentage changes).