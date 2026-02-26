# United Kingdom Butterfly Monitoring Scheme: site indices data 2016

- Overview
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites per year across the UK.
  - Data primarily gathered via fixed linear transects (Pollard walks) to estimate butterfly abundance; includes both standard all-species transects and reduced-effort Wider Countryside Butterfly Survey (WCBS) transects.
  - Site indices provide a relative measure of population size, useful for tracking trends and comparing across years and sites.

- Data collection methods
  - All-species transects: fixed routes (2–4 km), recording all butterflies within a ~5 m band weekly from April to September (roughly 26 counts per year); transects are habitat- and management-specific and fixed to enable year-to-year comparisons.
  - Single-species transects: follow the all-species methodology but concentrate on a focal species during selected weeks.
  - Timed counts and egg/larval web counts: alternative methods for specific species or life stages.
  - WCBS: reduced-effort sampling in wider countryside habitats, using two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per season.
  - Data recording: field forms; online entry via UKBMS data site or Transect Walker software; data uploaded to an Oracle database. Each transect region has a coordinator responsible for data submission.

- Data processing and indices
  - Site indices are computed only for sites with sufficient monitoring visits; WCBS sites are excluded from site index calculations due to limited visits.
  - For transect sites, a General Additive Model (GAM) is used to impute missing values and calculate the site index.
  - Indices are relative to the actual population size and are linked to other measures (e.g., mark-release-recapture) but are not absolute counts.

- Data formats and units
  - Stored as CSV files with columns including:
    - Species (scientific name)
    - Common name
    - Year
    - SiteNo (site identifier)
    - Site Index (value for that species at that site and year)
  - A value of -2 indicates that a site-year combination could not produce an accurate index due to insufficient data.

- Quality control
  - In-field automatic checks in Transect Walker flag unusual counts or flight-period outliers; recorders can correct.
  - Regional transect coordinators validate records; ongoing checks during the season.
  - Post-entry validation includes checks for misaligned distribution (based on Butterfly Conservation data), flight period anomalies, new site records, extreme or unusual abundances.

- Data access and citation
  - Data and reuse/licensing details available at the provided DOI link.
  - Use requires citation: Botham, M.; Roy, D.; Brereton, T.; Middlebrook, I.; Randle, Z. (2017). United Kingdom Butterfly Monitoring Scheme: site indices data 2016. NERC Environmental Information Data Centre. DOI.
  - References for methodology include key statistical and monitoring sources (e.g., Pollard & Yates 1993; Rothery & Roy 2001; Emmet & Heath 1990).

- Key references
  - Pollard E. & Yates T.J. (1993). Monitoring Butterflies for Ecology and Conservation.
  - Rothery P. & Roy D.B. (2001). Application of generalized additive models to butterfly transect count data.
  - Emmet A.M. & Heath J. (1990). The Moths and Butterflies of Great Britain and Ireland.