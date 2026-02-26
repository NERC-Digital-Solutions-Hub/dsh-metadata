# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

- Data access and citation
  - Data and reuse/licensing details available at the provided DOI link.
  - If you use this data, you must cite Botham et al. (2017): United Kingdom Butterfly Monitoring Scheme: site indices data 2016, NERC Environmental Information Data Centre.

- Scope and purpose
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites per year across the UK.
  - Site indices provide a relative measure of butterfly abundance, used to monitor trends rather than exact population sizes.
  - Data support biodiversity monitoring, conservation assessment, and ecological research; intended for discovery and reuse by researchers, practitioners, and policy makers.

- Data collection methods
  - All-species transects (Pollard walks): fixed 2–4 km routes walked weekly (April–September) under suitable weather; transects fixed to enable year-to-year comparison.
  - Reduced-effort Wider Countryside Butterfly Survey (WCBS): 1-km squares with 2–4 visits per year, sampling wider habitats.
  - Single-species transects, timed counts, and egg/larval web counts used for specific species or contexts.
  - Field data recorded on standard forms; entered online via UKBMS MyData or into Transect Walker software; regional transect coordinators consolidate data.

- Data processing and quality assurance
  - Field data uploaded to an Oracle database; site indices computed using a General Additive Model (GAM) to impute missing values and derive indices for transect sites.
  - Data quality checks include automatic flags for out-of-range counts or unusual flight periods; regional coordinators perform validation; ongoing software-based and manual validation throughout the monitoring season.
  - Cross-checks against distribution extents (e.g., Butterflies for the New Millennium) and flight-period timing to identify anomalies.

- Data format and storage
  - Site indices stored as comma-separated values (CSV).
  - Columns include: Species (scientific name per Fauna Europaea), Common name, Year, SiteNo (site identifier), Site Index.
  - If a site-species combination lacks sufficient data to compute an index, the value is -2.

- Units, interpretation, and limitations
  - Site indices are relative measures of population size, not absolute counts; the index is proportional to the actual butterfly abundance at a site.
  - The index’s relative nature may vary by species (e.g., conspicuous species vs. cryptic ones).
  - WCBS sites are excluded from site-index calculations due to insufficient visits for reliable indices.

- Data governance and provenance
  - Data originate from UKBMS and are managed through the NERC Environmental Information Data Centre.
  - Clear criteria govern data inclusion (sufficient visits) and update procedures; ongoing governance ensures consistency across years and datasets.

- Related references and context
  - Methods and background linked to Pollard & Yates (1993), Emmet & Heath (1990), and Rothery & Roy (2001) on GAM-based modeling for butterfly transect data.

- Key challenges for data stewardship (from the broader context)
  - Incomplete understanding of user needs and priorities.
  - Timely acquisition of data from field contributors.
  - Ensuring data creators meet metadata and standardization requirements.
  - Handling multiple systems and formats, including legacy and bespoke solutions.
  - Managing and transferring large datasets (e.g., long time spans, many sites).
  - Integrating with outdated databases that require non-interoperable approaches.