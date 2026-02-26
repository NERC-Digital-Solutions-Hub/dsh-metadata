# About the UK Butterfly Monitoring Scheme

- The UKBMS is a long-running UK-wide program (since 1976) that collects annual butterfly population data from site-based monitoring to support biodiversity status and policy questions.
- Data are gathered from multiple sampling frameworks: standard Pollard walks (2–4 km transects with 26 weekly counts), Wider Countryside Butterfly Survey (WCBS) in 1 km squares with 2–3 visits, and targeted single-species or alternative surveys.
- More than 2,500 active sites are monitored annually; all sampling methods are analyzed together to produce population indices.

- GIS-relevant data are location-focused, enabling spatial analyses of site distribution, survey coverage, and trends over time.

# Nature of data collected and trend analysis (GIS implications)

- Abundance indices are used (relative measures) to describe butterfly populations per site and per species.
- A Generalised Abundance Index (GAI) method (2016) combines site indices into species-level indices, weighting site data by the proportion of the species’ flight period surveyed that year.
- Counts across the season from all methods are used to model seasonal patterns and extrapolate for missing data, with weighting favoring observed data over extrapolated data.
- Data are suitable for trend analysis, comparative studies, and policy-oriented biodiversity assessments, with attention to detection variability among species and sites.

# Quality control

- Data are collected on standard forms and entered online or via Transect Walker; automated checks flag anomalies (e.g., unusually high counts, out-of-season records).
- Regional transect coordinators review records; multiple automated and manual validations follow (range checks, distribution checks, first-time site records, unusual abundances, etc.).
- Data corrections are performed through queries and communications with coordinators/recorders as needed.

# Details of this data download (GIS-centric)

- Time span: site location and attribute data for UK butterfly monitoring sites from 1976 to 2020 (sensitive sites excluded).
- Output format: comma-separated values (CSV).
- Spatial/geospatial fields per site:
  - Site number (unique)
  - Site name
  - Gridreference (OS grid reference, typically 6 figure)
  - Easting (x-coordinate)
  - Northing (y-coordinate)
  - Length (transect length in metres, if provided)
  - Country
  - No. Sections (transect divisions)
  - No. Yrs surveyed (up to 2021)
  - First year surveyed
  - Last year surveyed (up to 2021)
  - Survey type (standard UKBMS transect or WCBS)

# Licence and attribution

- Open Government Licence (OGL) for free use and reuse with conditions.
- Include citation details and the dataset’s Digital Object Identifier (DOI) in references.
- Attribution statement: Contains UK Butterfly Monitoring Scheme data © Butterfly Conservation, Centre for Ecology & Hydrology, British Trust for Ornithology, and Joint Nature Conservation Committee.
- Since 2017 data submitters have agreed to OGL availability; some historic data may have third-party IP restrictions.

# Collaboration and contact details

- The UKBMS partners offer advisory support on dataset interpretation and outputs.
- Co-authorship and intellectual input into publications arising from UKBMS data are welcomed.
- Contacts:
  - UK Centre for Ecology & Hydrology (Marc Botham): ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect Co-ordinator): transect@butterfly-conservation.org

# Key considerations for GIS Use

- Data provide precise site locations (grid references, Easting/Northing) suitable for mapping site distribution, transect coverage, and temporal analyses.
- Data are relational over time; users should account for changes in survey type (standard vs WCBS) and year coverage per site.
- Understand that indices are relative measures; spatial analyses should focus on trends and distributions rather than absolute abundance comparisons across species or sites.