# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
- Main methods:
  - All-species transects (Pollard walks): fixed-route, all butterflies recorded weekly under specified weather conditions.
  - Single-species transects: identical methodology but focused on one focal species for some weeks.
  - Timed counts and egg/larval web counts: species-specific counts over a set time/area and habitat.
- Transect design:
  - Routes are fixed to enable year-to-year comparison and to sample habitat types evenly.
  - Typical length: 2–4 km; divided into habitat/management sections.
  - Recording band: fixed width of about 5 m along the transect.
  - Counts: 26 per year (weekly from early April to late September).
  - Timing: 10:45–15:45; weather criteria required for butterfly activity.
  - Weather criteria: dry conditions, wind < Beaufort 5, temperature ≥13°C with at least 60% sunshine, or >17°C if overcast.
- Data collection contexts:
  - All-species: broad species list along transect.
  - Timed/egg-larval counts: targeted methods for specific life stages or species.

- Data collection methods
  - Field data recorded on standard forms.
  - Data entered into Transect Walker software (free download via UKBMS site).
  - Entry performed by the recorder or region transect coordinator.
  - End-of-season data assembled by each transect coordinator for their region.
  - Transect Walker files uploaded to an Oracle database containing all records.

- Analytical methods
  - After validation, missing values are imputed and site indices computed using General Additive Models (GAM).
  - Site indices from all methods are combined to produce a national annual index for each species (Collated Index).
  - Because not all sites are monitored every year, missing values are estimated with a loglinear regression model that accounts for year effects and site effects.
  - Collated Indices are updated annually as new data are incorporated; indices for species are calculated from data at five or more sites per year.

- Nature and units of recorded values
  - Site indices are relative measures of population size (not absolute counts) and relate to other population measures.
  - Collated Indices are presented as the log10 of the Collated Index (LCI) and are scaled so the average index across the series equals 2 for a given species.

- Quality control
  - Automatic checks in Transect Walker flag unusual counts or records outside flight periods.
  - Regional coordinators review records for questionable data.
  - Additional automated/manual validation includes checks for species outside known distribution ranges, unusual flight periods, first-time site records, and extreme or atypical abundances.

- Format and storage of data
  - Collated Indices are stored as CSV files.
  - Columns included:
    - Species (scientific name per Fauna Europaea v2.2)
    - Common name (per Emmet & Heath, 1990)
    - Year
    - No. Sites (sites contributing to the Collated Index that year)
    - Collated Index
    - Time period (data used to produce the Collated Indices)

- Data workflow relevance for GIS
  - Spatially explicit sampling via fixed transects and site-level indices supports map-based visualization of trends.
  - Data integration across sites, years, and methods enables landscape-scale analyses and GIS-based decision support.