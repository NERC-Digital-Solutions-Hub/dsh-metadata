# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, primarily using fixed-line transects called Pollard walks to estimate butterfly abundance.
- Data types include site indices (relative population measures) for multiple species, derived from standard methods (all-species transects, reduced-effort WCBS; timed counts and egg/larval web counts for some species).

- Data collection methods and coverage
  - All-species transects: fixed routes, weekly records along a 2–4 km transect in a 5 m wide band, typically 26 counts per year from April to September.
  - WCBS (Wider Countryside Butterfly Survey): reduced-effort sampling along two parallel 1-km transects within randomly selected 1-km squares, 2–4 visits per year.
  - Single-species transects: subset of weeks within the flight period for a focal species.
  - Timed counts and egg/larval web counts: species-specific measures during restricted time frames and areas.
  - Data collection window: counts conducted under specified weather conditions and time windows (10:45–15:45; specific temperature, wind, and sunshine criteria).

- Data workflow and storage
  - Field recording on standard forms; data entered online via the UKBMS data entry site or Transect Walker software.
  - Data entry can be done by the recorder or a regional transect coordinator; regions have coordinators who aggregate data.
  - Data uploaded to an Oracle database; site indices calculated using statistical methods.
  - WCBS data are excluded from site-index calculations due to insufficient visit counts.

- Data processing and quality control
  - Automatic checks in Transect Walker flag anomalous counts or records outside known flight periods.
  - Regional coordinators review records; continuous checks during the season.
  - Additional automated/manual validation checks for out-of-range distributions, first records at a site, unusually high or unusual counts.
  - Imputation and site-index calculation use a General Additive Model (GAM) to handle missing values (for transect sites).

- Data characteristics and units
  - Site indices are relative measures of population size, not absolute counts; proportion of actual population that is observed varies by species.
  - Indices are time- and site-specific; where data are insufficient, the index value is set to -2.
  - Species naming follows Fauna Europaea; common names follow Emmet & Heath.

- Data formats and accessibility
  - Site indices stored as CSV files with columns: Species, Common name, Year, Site number, Site Index.
  - Access and licensing information available via DOI and data access URL; data must be cited appropriately if reused.

- Key citations and provenance
  - Data and reuse/licensing details: https://doi.org/10.5285/0f64d554b36f-484a-a231-b6526796877a
  - Site index data reference: Botham et al. 2017, United Kingdom Butterfly Monitoring Scheme: site indices data 2016, NERC Environmental Information Data Centre.
  - Methodological references for transect methods and GAM-based index calculation (Pollard & Yates 1993; Rothery & Roy 2001).

- Reuse considerations for data leaders
  - Strengths: standardized, long-running, centralized data management; clear data lineage from field collection to index computation; robust QC and validation processes; explicit metadata and provenance.
  - Opportunities for improvement: maintaining data discoverability across networks; handling data gaps and variability in species detectability; ongoing coordination to harmonize metadata and formats; potential expansion of data products beyond site indices (e.g., temporal trends, species-specific insights).