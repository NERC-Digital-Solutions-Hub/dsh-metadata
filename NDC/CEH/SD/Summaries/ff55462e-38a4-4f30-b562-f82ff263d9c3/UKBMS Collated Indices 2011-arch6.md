# Experimental design/sampling regime

- Experimental framework
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Primary method is all-species transects (Pollard walks): fixed-route line transects, 2–4 km long, 45 minutes to 2 hours to complete.
  - Counts are conducted weekly from early April to late September, weather permitting, with 26 counts per year.
  - Transects are fixed to allow year-to-year comparisons and are divided into habitat/management sections.

- Data collection methods
  - Field data recorded on standard forms and entered into Transect Walker software (free to download).
  - Data input by the recorder or the regional transect coordinator; a transect coordinator compiles all data for their region.
  - Transect Walker files are uploaded into an Oracle database that houses all records.

- Experimental variations
  - All-species transects: record all butterflies along the transect.
  - Single-species transects: same methodology but focused on one focal species for one or more weeks.
  - Timed counts and egg/larval web counts: targeted abundance measures for specific species in suitable habitat areas; follow same time window as transects.

- Analytical methods
  - After validation, a General Additive Model (GAM) imputes missing values and computes a site index.
  - Site indices from all methods are combined to derive a national annual index per species (Collated Index).
  - Because not all sites are monitored every year, a log-linear regression estimates missing values and yields indices/trends, incorporating year effects (weather-driven) and site effects.
  - Collated Indices are updated annually with new data; past years’ indices may be revised as data accrues.
  - Collated Indices are calculated for species recorded at five or more sites per year.

- Nature and units of recorded values
  - Site indices are relative measures, correlating with more intensive population size measures (e.g., mark–release–recapture).
  - Collated Indices are expressed as Log10 of the Collated Index (LCI) and are scaled so that the species’ average index over the series equals 2.
  - The proportion of butterflies seen varies by species (e.g., more conspicuous species vs. harder-to-see species).

- Quality control
  - Automatic checks in Transect Walker flag data entry anomalies (e.g., abnormally high counts, records outside known flight periods).
  - Regional coordinators review data for each region to catch questionable records.
  - Additional automated/manual validation checks for out-of-range distributions, records outside flight periods, new-site records, and unusually extreme values.

- Format and storage of data
  - Collated Indices stored as CSV files.
  - Columns include:
    - Species (scientific name following Fauna Europaea v2.2)
    - Common name (following Emmet & Heath)
    - Year
    - No. Sites (number of contributing sites)
    - Collated Index (the species’ index for that year)
    - Time period (data used to produce the Collated Indices)