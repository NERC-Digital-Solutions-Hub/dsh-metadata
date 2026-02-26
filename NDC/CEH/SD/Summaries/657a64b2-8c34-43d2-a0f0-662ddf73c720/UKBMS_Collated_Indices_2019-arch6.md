# About the UK Butterfly Monitoring Scheme

- Overview: The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with broad thanks to volunteers.
- Purpose: Provides annual data on butterfly population status across the UK to inform biodiversity policy questions; serves as a long-term, site-based monitoring resource.

- Data collection framework
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, weekly counts (ideally 26 per year) across almost 2000 sites; recorder-chosen routes with habitat units.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel 1 km transects; 2–3 visits per year (plus encouraged spring visits), ~750 squares per year.
  - Targeted surveys: single-species transects and other methods (e.g., timed counts, egg/larval web counts) focused on particular species.
- Data coverage and integration: Since 1976, >2500 active sites per year; data from all sampling methods are analyzed together to produce unified species indices.

- Data processing and analysis
  - Abundance indices: relative measures based on counts from transects; reflect proportion of butterflies observed rather than absolute population size.
  - Collated indices: produced per species using the Generalised Abundance Index (GAI) method (2016), with a site- and year-weighting adjustment based on the proportion of the species flight period surveyed.
  - Use of seasonal patterns and extrapolation: counts from all methods are used to estimate seasonal patterns and fill gaps, with greater weight given to observed data.

- Quality control
  - Data recording: field forms, online entry (UKBMS MyData) or Transect Walker, with automatic checks for anomalies.
  - Regional validation: regional transect coordinators review data; continuous checks during the season.
  - Automated/manual validation: checks for records outside known distributions, out-of-season records, first-time site records, and unusual counts; edits made as needed.

- Details of this data download
  - Scope: Annual collated indices for species with sufficient data from 1976–2019 (some early years excluded for certain species due to data gaps).
  - Format: Comma-separated values (.csv).
  - Key columns:
    - SPECIES CODE, SPECIES, COMMON NAME
    - YEAR, NO. SITES
    - COLLATED INDEX (log10 scale; standardized so the mean across the series equals 2)
    - YEAR RANK (1 = best year for that species)
    - TIME PERIOD, COUNTRY

- Licence and attribution
  - Open Government Licence (OGL); free use with few conditions.
  - Required citation details and Digital Object Identifier must be included in publications using the data.
  - Attribution statement: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

- Offer of collaboration and contact details
  - UKBMS partners offer advisory support and interpretation of outputs; opportunities for co-authorship and collaboration in publications and presentations.
  - Contacts:
    - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
    - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org

- Notes and considerations for data users (Data Support perspective)
  - Outputs are relative indices, not absolute population sizes; suitable for trend analysis and policy questions but not direct population counts.
  - Data quality is high due to multi-level validation but gaps exist in earlier years for some species; weighting and extrapolation help mitigate missing data.
  - Useful for building dashboards, reports, or self-serve analyses to compare species trends over time and space, with clear provenance and licensing.