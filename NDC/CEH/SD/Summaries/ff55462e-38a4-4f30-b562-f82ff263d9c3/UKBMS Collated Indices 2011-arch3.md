# UK Butterfly Monitoring Scheme (UKBMS)

## Experimental design/sampling regime
- Data collected annually from over 1,000 sites across the UK.
- Uses multiple transect-based methods:
  - All-species transects (Pollard walks): fixed routes 2–4 km long, weekly counts from early April to late September, ~26 counts/year.
  - Single-species transects: follow all-species protocol but focused on one focal species.
  - Timed counts and egg/larval web counts for specific species.
- Transect routes are fixed to sample habitat types and management activities; weather constraints (suitable butterfly activity) govern when counts occur.
- Observational windows typically between 10:45 and 15:45, with specific weather criteria (dry, wind < Beaufort 5, temperature thresholds).

## Data collection methods
- Field data recorded on standard forms.
- Data entered into Transect Walker software (free download) by recorders or regional coordinators.
- Regional transect coordinators compile data for their region; Transect Walker files are uploaded to an Oracle database.

## Analytical methods
- After validation, a General Additive Model (GAM) imputes missing values and computes site indices.
- Indices from all methods are combined to produce a national annual Collated Index for each species using a log-linear regression to handle missing years/sites and year/site effects.
- Yearly updates incorporate new data; past years’ indices may shift as data are re-included.
- Collated Indices are calculated for species recorded at five or more sites per year.

## Nature and units of recorded values
- Site indices are relative measures of population size, proportional to actual abundance.
- Collated Indices are expressed as the logarithm (base 10) of the Collated Index (LCI); values are scaled so that the average index over the series equals 2, providing a relative measure over time.

## Quality control
- Automatic checks within Transect Walker flag anomalous records (e.g., unusually high counts, records outside known flight periods).
- Regional coordinators review records, followed by automated and manual validation steps.
- Additional queries check for species outside known distribution, atypical flight periods, first-time site records, and unusual abundances.

## Format of stored data
- Collated Indices stored as CSV files.
- Columns include:
  - Species (scientific name per Fauna Europaea)
  - Common name (per standard references)
  - Year (index calculation)
  - No. Sites (sites contributing in that year)
  - Collated Index (the index value for that year)
  - Time period (data used to produce the indices)