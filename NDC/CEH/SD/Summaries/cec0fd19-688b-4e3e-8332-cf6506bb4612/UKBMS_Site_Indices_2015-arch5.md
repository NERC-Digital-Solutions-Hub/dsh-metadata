# The UK Butterfly Monitoring Scheme (UKBMS)

- A national effort collecting butterfly observation data from over 2,000 sites annually across the UK.
- Primarily relies on fixed-route Pollard walk transects to estimate butterfly abundance, with additional methods for certain species or contexts (timed counts and egg/larval web counts).
- Includes two main transect types: all-species transects (standard) and Wider Countryside Butterfly Survey (WCBS) transects (reduced effort).

## Data collection methods

- All-species transects
  - Fixed-route line transect at each site; all butterflies counted along a 2–4 km route.
  - Counts are conducted weekly (April to September) under specific weather conditions.
  - Transects are fixed to enable year-to-year comparison; counts are taken in a 5 m wide band.
  - Typical effort: 26 counts per site per year; transects take 45 minutes to 2 hours.
- Single-species transects
  - Follow the same methodology as all-species transects but restricted to a few weeks for the focal species.
- Timed counts and egg/larval web counts
  - Timed counts record a focal species over a set period and area, under defined weather conditions.
  - Egg/larval web counts record eggs or larval webs in suitable habitat.
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey for broader habitats (farmland, countryside).
  - Based on two parallel 1-km transects within randomly chosen 1-km squares; 2–4 visits per year (minimum two in July/August), fewer in spring.
- Data capture
  - Field data recorded on standard forms; entered online via the UKBMS data site or Transect Walker software.
  - Data input by recorder or regional transect coordinators; coordinators aggregate region data.
  - Online data and Transect Walker files uploaded to an Oracle database storing all records.

## Data management and processing

- Site indices
  - Calculated only for sites with sufficient monitoring; for timed observations and egg/larval counts, indices are adjusted to align with the flight period and site size.
  - WCBS sites are excluded from index calculations due to insufficient visits for accurate indices.
  - For transect sites, indices are computed using a General Additive Model (GAM) to impute missing values and estimate site indices.
- Data flow and stewardship
  - Data move from field recorders to regional coordinators, then into the centralized Oracle database.
  - Regional coordinators validate data and perform ongoing quality checks.

## Nature, units, and interpretation of recorded values

- Site indices are relative measures of population size, not absolute counts.
- They are designed to correlate with more intensive population measures (e.g., mark–release–recapture) and represent a constant proportion of the actual population for a given species.
- Species-specific visibility varies; some species are more or less conspicuous, affecting index magnitude.

## Quality control and data validation

- In-field automatic checks within Transect Walker flag potential errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review records for questionable entries.
- Additional automated and manual validation steps post-entry, including checks for:
  - Records outside known distribution ranges (using external datasets).
  - Records outside normal flight periods.
  - First-time records at a site.
  - Abnormal abundances or drastic deviations from typical site patterns.

## Data format and metadata

- Stored data format: Site Indices stored as plain text files (.txt).
- Columns include:
  - Species (scientific name per Fauna Europaea v2.2)
  - Common name (per Emmet & Heath, 1990)
  - Year (year of the site index)
  - Site Index (relative abundance value)
- Handling of gaps: if a site was not monitored sufficiently to calculate an index in a given year, the Site Index value is set to -2.

## Relevance to data stewardship and governance

- Standardization
  - Uses consistent species naming, metadata conventions, and data formats to enable interoperability and long-term usability.
- Provenance and lineage
  - Clear data flow from field collection to regional coordination to centralized storage, with validation at multiple stages.
- Accessibility and sharing
  - Data are deposited in a central Oracle database and made available through online entry portals and software tools (Transect Walker), supporting discoverability and reuse.
- Data quality and integrity
  - Multi-layered QC approaches (automatic checks, regional validation, and global validation rules) to ensure high data quality and reliability.
- Limitations and disclosures
  - Explicit notes on when data (e.g., WCBS indices) cannot be used for certain analyses due to insufficient visits; indices are relative rather than absolute measures.
- Potential use and impact
  - Relative population indices facilitate temporal trend analyses and comparisons across sites, aiding conservation decisions and butterfly population monitoring.

## Key challenges

- Incomplete understanding of user needs and priorities.
- Timeliness of data acquisition from field sites.
- Ensuring data creators meet metadata and standardization requirements.
- Managing data across multiple systems and formats, including older bespoke solutions.
- Handling large datasets and transferring data from remote or remote-sensing points.
- Dealing with outdated databases that require bespoke, non-interoperable solutions.