# UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects annual butterfly data from over 1,000 sites across the UK using standardized field methods to support ecological monitoring and policy evaluation.

- Experimental design and sampling
  - All-species transects (Pollard walks): fixed-route line transects at sites, sampling evenly across habitat types and management, typically 2–4 km, with about 26 weekly counts from April to September under suitable weather.
  - All-species transects use a fixed route to enable year-to-year comparisons.
  - Transects are conducted during specific daily hours and only under favorable butterfly activity conditions (weather thresholds).
  - Single-species transects replicate the all-species approach but record only one focal species for selected weeks.
  - Additional methods include timed counts and egg/larval web counts for specific species in suitable habitats.

- Data collection and entry
  - Field data are recorded on standard forms and entered into Transect Walker (free software) by recorders or regional transect coordinators.
  - Regional coordinators compile data for all sites in their region, with Transect Walker files uploaded to an Oracle database.

- Analytical methods and indicators
  - After validation, a General Additive Model (GAM) imputes missing values and derives a site index for each method.
  - Individual site indices are combined to produce a national Collated Index for each species, using a log-linear regression to estimate missing values when not all sites are monitored each year.
  - The Collated Index is updated annually as new data are incorporated; indices are computed for species recorded at five or more sites per year.
  - Site indices are relative measures of population size (not absolute counts) and are treated as proportional to actual population size; Collated Indices are presented as log10 values with the average scaled to 2.

- Data interpretation and units
  - Site indices reflect relative population size and can be compared across years and sites, acknowledging species detectability differences.
  - Collated Indices (log10) provide a standardized, relative measure of population trends over time.

- Quality control and validation
  - Automated checks in Transect Walker flag anomalous counts or records outside known flight periods; recorders can amend data accordingly.
  - Regional coordinators apply further validation checks; automated and manual procedures assess out-of-range distributions, unusual flight periods, first-time site records, extreme abundances, or large year-to-year differences.
  - Data undergo ongoing validation to ensure consistency with known distributions and temporal patterns.

- Data storage and format
  - Collated Indices are stored as CSV files.
  - Columns include: Species (scientific name per Fauna Europaea), Common name (per Emmet & Heath), Year, No. Sites (sites contributing to the index), Collated Index (value for the year and species), Time period (data used to compute the index).