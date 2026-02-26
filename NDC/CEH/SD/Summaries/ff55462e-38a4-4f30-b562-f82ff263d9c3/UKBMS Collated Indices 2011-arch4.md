# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Majority of data come from fixed linear transects called Pollard walks; other methods include timed counts and egg/larval web counts for some species and sites.
- Transect design aims to sample habitat types and management activities evenly; transects are fixed to enable year-to-year comparisons.
- All-species transects cover 2–4 km per site, with a 5 m wide observation band; typical protocol yields about 26 counts per year from early April to late September.
- Weather and activity windows: observations occur 10:45–15:45 under suitable butterfly activity conditions, with specific thresholds for wind, temperature, and sunshine.

# Data collection methods

- Field data recorded on standard forms and entered into Transect Walker software (free download from UKBMS site).
- Data entry can be by the recorder or by the regional transect coordinator; each transect region has a coordinator responsible for season-end data compilation.
- Transect Walker files are uploaded to an Oracle database that stores all records.

# Analytical methods

- After validation, missing values are imputed using General Additive Models (GAM) to produce site indices.
- A Collated Index for each species is derived by combining data across all sampling methods; a log-linear regression model estimates missing values and trends due to year and site effects.
- Collated indices are updated annually as new monitoring data are incorporated; past indices may adjust slightly with new data.
- Collated Indices are calculated for species recorded at five or more sites per year.

# Nature and units of recorded values

- Site indices are relative measures of population size, proportional to actual counts (not absolute numbers).
- Relative indices are scaled so that the average index across the time series equals 2 for each species.
- Collated Indices are presented as the Log10 of the Collated Index (LCI).
- The index reliability varies by species (e.g., conspicuous species vs. less visible ones).

# Quality control

- Automatic checks in Transect Walker flag unusual counts or records outside known flight periods.
- Regional coordinators review records for questionable entries; subsequent automated and manual validations search for out-of-range ranges, unusual site introductions, first-time site records, and anomalous counts.

# Format of stored data

- Collated Indices stored as CSV files.
- Columns include: Species (scientific name per Fauna Europaea), Common name, Year, No. Sites, Collated Index, Time period (data used to produce the index).