# About the UK Butterfly Monitoring Scheme

- Organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee; volunteers contribute data.
- Purpose: annual, site-based monitoring of butterfly population status since 1976; currently over 3,000 active sites each year; data from all sampling methods are analyzed together to inform biodiversity status and policy questions.

## Data collected and sampling framework

- Three main components:
  - Standard butterfly transects (Pollard walks): fixed-route, weekly counts (typically 2–4 km, 5 m recording band) with up to 26 counts per year; many sites (over 2,000 by 2022).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, 2–3 visits per site per year (including July/August), sampling around 800 squares annually.
  - Targeted surveys: single-species transects, alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species.
- All methods contribute to a unified UKBMS dataset.

## Data products and analysis

- Outputs are abundance indices (relative measures of population size) rather than absolute counts.
- Site indices are combined into species-level indices using the Generalised Abundance Index (GAI) with site-by-year weighting based on how much of the species’ flight period is surveyed.
- Counts from all methods are used to model seasonal patterns and estimate population indices, accounting for gaps in recording.

## Quality control and data validation

- Field data recorded on standard forms, entered online (or via Transect Walker) and uploaded to a central database.
- Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods); regional coordinators review data.
- Additional automated/manual validation screens for:
  - Records outside known distribution
  - Out-of-season records
  - First-time site records
  - Abnormal abundances or atypical site-year comparisons
- Corrections are applied through queries and coordination with transect recorders when needed.

## This data download: scope and format

- Provides location and attribute data for UK sites monitored under UKBMS from 1976 to 2022; sensitive sites excluded.
- Delivered as a CSV file.
- Key columns include:
  - Site_number, Site_name, Gridreference, Easting, Northing, Length
  - Country, N_Sections, N_Yrs_surveyed, First_year_surveyed, Last_year_surveyed
  - Survey_type (standard UKBMS vs WCBS)

## Licence and attribution

- Open Government Licence (OGL) for free use and reuse with minimal conditions.
- Must include full citation (including DOI) in reports/publications using the data.
- Attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.
- Since 2017, submitters have agreed to OGL terms; some historic data may carry third-party IP restrictions; notify if concerns arise.

## Collaboration and contact details

- UKBMS partners offer guidance on dataset interpretation and potential collaboration.
- Opportunity for co-authorship and intellectual input in publications resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
  - Butterfly Conservation Transect Co-ordinator: transect@butterfly-conservation.org

## Key implications for Data Leaders

- This dataset exemplifies a multi-source, long-running data asset with integrated governance, quality controls, and derived indicators (GAI-based indices).
- Highlights the importance of clear licensing, attribution, and user guidance for reuse in policy and research.
- Demonstrates scalable data quality processes (field validation, regional oversight, automated checks) suitable for broader data ecosystems.
- Emphasizes the value of collaboration, open data access (OGL), and opportunities for co-authored outputs while balancing data sensitivity and IP considerations.
- Provides a model for documenting data provenance, scope, and methodological details to support discoverability and trust in data products.