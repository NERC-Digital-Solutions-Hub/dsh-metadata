# About the UK Butterfly Monitoring Scheme

- Purpose and scope
  - Annual data on butterfly population status in the UK, sourced from a large volunteer-based monitoring program.
  - Managed and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - Over 3,000 actively recorded sites annually; data from all sampling methods are analyzed together.
  - Provides data to understand biodiversity trends and inform policy questions.

- Data collection framework
  - Standard butterfly transects (Pollard walks): fixed-route transects 2–4 km, 26 counts/year (April–September), 5 m wide band, weekly counts under suitable weather.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel transects, 2–3 visits/year (July/August plus optional spring), ~800 squares/year.
  - Targeted surveys: single-species transects and other methods (timed counts, egg/larval web counts) focusing on specific species.
  - Methods are combined to form a comprehensive UKBMS dataset.

- Data structure and nature
  - Uses abundance indices (relative measures) rather than absolute population sizes.
  - Site indices are combined into species-level collated indices using the Generalised Abundance Index (GAI) with year- and site-weighting based on flight period coverage.
  - Counts from all methods are utilized to estimate seasonal patterns and extrapolate for gaps in recording.

- Quality control and governance
  - Field data recorded on standard forms; entered online or via Transect Walker; uploaded to a central database.
  - Automatic checks during data entry to flag anomalies (e.g., unusually high counts, records outside flight periods).
  - Regional transect coordinators validate and review data; ongoing checks throughout the season.
  - Further automated and manual validation to catch records outside distribution ranges, atypical flight periods, first-time site records, or extreme abundances; data corrections made as needed.

- Data download details
  - Dataset: annual indices of abundance for each species at each UK site with sufficient data, covering 1976–2022.
  - File format: CSV (comma-separated values).
  - Key columns and meanings:
    - SITE_CODE: unique site identifier
    - COUNTRY: country used to compute regional collated index
    - SPECIES_CODE: unique species identifier
    - SPECIES: scientific name (per Agassiz et al. updates)
    - COMMON_NAME: vernacular name (per Emmet & Heath)
    - YEAR: year of the collated index
    - SITE_INDEX: abundance index for species at a site and year (−2 indicates insufficient data)
  - Taxonomy references provided for species naming consistency.

- licence and attribution
  - Open Government Licence (OGL) for free use and reuse with few conditions.
  - Required citation details (including DOI) must be included in publications using the data.
  - Attribution statement to be used: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration offers and contact details
  - UKBMS partners offer guidance on dataset interpretation and opportunities for co-authorship or intellectual input in publications, presentations, or posters.
  - Contact: UKBMS at ukbms@ceh.ac.uk (CEH) or transect@butterfly-conservation.org (Butterfly Conservation).