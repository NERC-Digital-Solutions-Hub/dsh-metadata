# About the UK Butterfly Monitoring Scheme

- Purpose and scope
  - UKBMS provides annual data on butterfly population status from a nationwide, site-based monitoring program.
  - Data support understanding biodiversity trends and policy questions; active since 1976 with over 3,000 sites recorded annually.
  - Multiple sampling methods included: standard transects (Pollard walks), Wider Countryside Butterfly Survey (WCBS), and targeted surveys.

- Data collection methods
  - Standard transects (Pollard walks): fixed-route 2–4 km transects; record all butterflies within a 5 m band; ~26 counts per year; weekly monitoring during suitable weather from April to September.
  - WCBS: stratified-random 1 km squares with two parallel transects; 2–3 visits per year (plus spring visits encouraged).
  - Targeted surveys: single-species transects, timed counts, egg/larval web counts, etc.
  - Data integration: all sampling methods combined for analysis.

- GIS-relevant data and attributes
  - Data download includes location and attribute data for UK sites (1976–2023), with sensitive sites excluded.
  - CSV format; key columns include:
    - Site_number, Site_name
    - Gridreference (6-figure accuracy, central transect), Easting, Northing
    - Length (transect length in metres, if provided)
    - Country, N_Sections, N_Yrs_surveyed
    - First_year_surveyed, Last_year_surveyed
    - Survey_type (UKBMS standard transect or WCBS)
  - Spatial coverage uses UK Ordnance Survey grid references and associated coordinates for mapping and analysis.

- Data quality control and processing
  - Field data recorded on standard forms; entered online or via Transect Walker; uploaded to central database.
  - Automated checks flag: abnormally high counts, records outside flight periods, records outside known ranges.
  - Regional transect coordinators validate data; continuous season checks and iterative data cleaning.
  - Additional validation targets: consistency with known distributions, flight periods, and site-specific baselines.

- Data structure and analysis notes
  - Abundance indices (relative measures) derived from counts; site indices reflect a proportion of butterflies present.
  - Generalised Abundance Index (GAI) method used to compute species indices; weights per site-year reflect the proportion of the flight period surveyed.
  - All counts across Pollard walks, reduced surveys, and WCBS contribute to seasonal pattern estimates and extrapolation.

- Data access, licensing, and attribution
  - Data download provided under the Open Government Licence (OGL) for free use and reuse.
  - Attribution: “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.”
  - Since 2017, submitters consented to data reuse under OGL; historical data may have IP or third-party restrictions in rare cases.

- Collaboration and contact
  - UKBMS partners offer guidance on dataset interpretation and potential co-authorship in publications arising from data use.
  - Contacts: UKBMS at ukbms@ceh.ac.uk; Butterfly Conservation transect coordinators at transect@butterfly-conservation.org.