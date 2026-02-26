# Experimental design/sampling regime

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites across the UK annually.
  - Data collection methods include all-species transects (Pollard walks), single-species transects, timed counts, and egg/larval web counts.
  - Transects are fixed-route to enable year-to-year comparability and are sampled across habitat types and management units; observations occur in a defined weekly window during the butterfly season.

- Data collection and management
  - Field data are recorded on standard forms and entered into the Transect Walker software (free download from UKBMS website).
  - Data entry can be by the recorder or a regional transect coordinator; each transect coordinator aggregates data for their region.
  - Transect Walker files are uploaded into an Oracle database that stores all records.
  - Data flow is organized by regional coordinators who verify and compile site data.

- Analytical methods
  - After validation, a General Additive Model (GAM) imputes missing values and computes a site index.
  - Site indices from all sampling methods are combined to produce a national annual Collated Index for each species.
  - Missing values are estimated with a loglinear regression model that accounts for year effects and site effects.
  - Collated Indices are updated annually as new data are incorporated; past indices may adjust slightly as data are added.
  - Indices are calculated for species recorded at five or more sites per year.
  - Collated Indices are presented as the logarithm (base 10) of the index (LCI) and scaled so the average index over the series equals 2.

- Nature and units of recorded values
  - Site indices are relative measures of population size, not absolute counts.
  - They reflect a constant proportion of the true population, varying by species (visibility differences among species).

- Quality control and validation
  - Transect Walker performs automatic checks for data-entry errors (e.g., abnormally high counts, records outside known flight periods).
  - Regional coordinators review data for questionable records.
  - Automated and manual validation steps follow, including checks for records outside known distribution, outside typical flight periods, first-time site records, and extreme or unusual abundances.

- Format and structure of stored data
  - Collated Indices are stored as CSV files.
  - Columns include:
    - Species: scientific name (per Fauna Europaea, v2.2)
    - Common name: vernacular name (per Emmet & Heath, 1990)
    - Year: year for which the Collated Index is calculated
    - No. Sites: number of sites contributing to the Collated Index for that year
    - Collated Index: the calculated index value for that year
    - Time period: the data period used to produce the Collated Indices
  - Validation references include Butterflies for the New Millennium (BNM) and existing UKBMS data.