# UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects and analyzes butterfly data from over 1,000 UK sites annually to monitor environmental health and policy performance over time.
- It uses standardized, repeatable methods to ensure comparability across years and sites.

## Experimental design and sampling regime

- All-species transects (Pollard walks) along fixed routes at each site; all butterflies recorded weekly under suitable weather.
- Transect length typically 2–4 km, divided into habitat/management sections; ~26 counts per year from April to September.
- Weather constraints for transects: 10:45–15:45, dry conditions, wind < Beaufort 5, temperature thresholds (≥13°C with ≥60% sunshine or >17°C if overcast).
- Single-species transects use the same methodology but are recorded only in some weeks.
- Timed counts involve a set effort over a defined area; egg/larval web counts record eggs or larval webs for species in suitable habitat.

## Data collection methods

- Data recorded on standard field forms and entered into Transect Walker software (free download from UKBMS).
- Data input either by the recorder or by a regional transect coordinator.
- Transect Walker files uploaded to an Oracle database housing all records.
- Each transect has a regional coordinator responsible for data collection and quality.

## Analytical methods

- After validation, a General Additive Model (GAM) imputes missing values and computes a site index.
- All-method site indices are combined to produce a national annual index for each species (Collated Index).
- Missing values and trends are estimated with a log-linear regression, accounting for year effects (weather) and site effects (population size differences).
- Collated Indices are updated annually as new data are added; indices may slightly alter as historical data are incorporated.
- Collated Indices are calculated for species recorded at five or more sites per year.
- Temporal scaling: Collated Indices are presented as Log10 Collated Index (LCI) with the average index over the series set to 2.

## Nature and units of recorded values

- Site indices are relative measures of population size (not absolute counts); they reflect a constant proportion of the true population.
- Collated Indices are log-transformed (Log10) and scaled so the average across the series equals 2, enabling temporal comparisons.

## Quality control

- In-field automatic checks within Transect Walker flag abnormal counts or records outside known flight periods.
- Regional coordinators review data for questionable entries and ensure consistency with known distributions.
- Additional automated and manual validation steps check for:
  - Records outside distribution ranges (using Butterfly Conservation data),
  - Records outside normal flight periods,
  - First-time records at a site,
  - Extreme or markedly different abundances for a site/time of year.

## Format of stored data

- Collated Indices are stored as CSV files with columns:
  - Species (scientific name per Fauna Europaea)
  - Common name
  - Year (year of the Collated Index)
  - No. Sites (sites contributing to the index that year)
  - Collated Index (the species index for that year)
  - Time period (data used to produce the index)