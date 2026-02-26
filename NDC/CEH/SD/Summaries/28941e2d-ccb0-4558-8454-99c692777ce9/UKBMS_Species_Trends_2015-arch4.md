# UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects butterfly data from over 2,000 sites annually across the UK, using standardized field methods to estimate population abundance for various species.
- Data types include all-species transects, reduced-effort Wider Countryside Butterfly Survey (WCBS) transects, and occasional single-species transects, timed counts, or egg/larval web counts depending on the species and site.

## Experimental design and sampling regime

- All-species transects: fixed-route line transects (2–4 km) sampled weekly during suitable weather (April–September). Routes are fixed to enable year-to-year comparisons and are divided into habitat/management sections. Counts cover a 5 m width along the transect.
- Transect timing and conditions: observations are conducted between 10:45 and 15:45, under conditions of dry weather, Beaufort wind < 5, and temperature thresholds (≥13°C with at least 60% sunshine, or ≥17°C if overcast).
- WCBS (Wider Countryside Butterfly Survey): reduced-effort sampling along two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per year (minimum 2 visits in July/August; spring visits encouraged).
- Single-species transects, timed counts, and larval webs follow the standard transect methodology but are focused on particular species or life stages during specific flight periods.

## Data collection and processing

- Field data are recorded on standard forms and entered online via the UKBMS data entry site or into Transect Walker (a free software tool). Data entry can be done by the recorder or a regional transect coordinator.
- End-of-season data submission is centralized: each transect coordinator gathers data for all sites in their region, with online and Transect Walker files uploaded to an Oracle database housing all records.

## Analytical methods

- Two primary approaches are used to derive national indices, depending on data density and sampling method:
  - Wider Countryside species: a two-stage model using all counts from all survey types. Stage 1 applies a generalized additive model (GAM) to estimate the annual seasonal flight pattern; stage 2 fits a model to the full annual counts with seasonal values as an offset to estimate annual abundance changes and trends. This method accounts for varying seasonality across years.
  - Habitat specialists and regular migrants (with sparser WCBS data): a GAM imputes missing values to create a site index, which is then aggregated to a national Collated Index. A log-linear regression model estimates missing values and trends, accommodating year effects (weather) and site effects (population size variation). Collated Indices are updated annually as new data are received.
- Trend calculation:
  - Linear regression on collated indices to produce overall trends since 1976.
  - Additional trends computed for recent periods: last 20 years (1996–2015) and last 10 years (2006–2015).
- Data interpretation involves distinguishing wider countryside species (mobile, broad habitat use), habitat specialists (low mobility, semi-natural habitats), and regular migrants (overwintering outside the UK).

## Data quality and validation

- Automated checks in Transect Walker flag unusual counts or records outside known flight periods; recorders can adjust or confirm entries.
- Regional transect coordinators review records for reliability and consistency, with continuous validation throughout the season.
- Additional validation steps include checks for records outside known distribution, first-time site records, extreme values, and substantial deviations from typical counts, using Butterfly Conservation data and existing UKBMS records.

## Data storage and format

- Species Trends are stored as CSV files with structured columns describing:
  - Species details (scientific name, common name)
  - Data coverage (number of years, series slope, standard error, p-value, trend description, percent change)
  - 20-year and 10-year trends (slopes, standard errors, p-values, trend descriptions, percent changes)
- Indices are presented as relative measures (Site Indices) and log10 Collated Indices (LCI) to standardize comparisons across species and time.
- The trend outputs include categories such as Rapid decline, Rapid increase, or Stable based on slope direction and statistical significance.

## Outputs and interpretation

- Key outputs: Site Indices, Collated Indices (LCI), and species-specific trends over multiple timeframes (overall, 20-year, and 10-year).
- The indices provide a relative measure of population change over time and are designed to reflect changes in abundance across monitored sites, supporting long-term monitoring and policy-relevant insights.