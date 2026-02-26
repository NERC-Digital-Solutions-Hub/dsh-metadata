# UK Butterfly Monitoring Scheme data download

- Overview
  - The UKBMS provides annual, site-based butterfly population data across the UK since 1976, used to understand trends and support biodiversity policy questions.
  - Data are gathered via multiple sampling methods and analyzed together to produce seasonal abundance indices.

- Data scope and sampling methods
  - Standard butterfly transects (Pollard walks): fixed routes (~2–4 km) with weekly counts across the main flight season; ~2000 sites sampled annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects; 2–3 visits per year to sample common habitats.
  - Targeted surveys: single-species transects or alternative methods (timed counts, egg/larval web counts) for particular species.
  - Data years: since 1976; current download includes site data up to 2020, with last survey year field indicating up to 2021 in some cases.

- Data content and structure (for GIS use)
  - Location and attribute data for each monitored site.
  - CSV format; excludes sensitive sites.
  - Key fields:
    - Site number
    - Site name
    - Gridreference (OS grid reference; typically 6-figure accuracy; central gridreference of transect)
    - Easting
    - Northing
    - Length (transect length in metres, where provided)
    - Country
    - No. Sections (transect subdivisions)
    - No. Yrs surveyed
    - First year surveyed
    - Last year surveyed
    - Survey type (UKBMS standard transect or WCBS)

- Spatial features relevant to GIS
  - Precise location data enabling mapping of transect routes, site distribution, and spatial coverage over time.
  - Grid references and projected coordinates (Easting/Northing) support GIS integration and spatial analyses.
  - Transect length and segmentation information facilitate visualization of sampling effort.

- Data quality, validation, and processing
  - Field data collected on standard forms; entered online or via Transect Walker; uploaded to a central database.
  - Automated checks for data entry errors (e.g., unusually high counts, out-of-season records).
  - Regional transect coordinators perform ongoing validation; additional automated and manual validation checks against known distributions and flight periods.
  - Data used to generate abundance indices (GAI) by combining counts from all methods; indices are relative measures, not absolute population sizes.
  - Weights applied so site-level observations influence final indices more when survey coverage is higher.

- Licensing, attribution, and reuse
  - Open Government Licence (OGL) for the data download.
  - Must include a full citation with the dataset’s DOI in publications using the data.
  - Attribution statement required: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.
  - Since 2017, submitters have agreed to OGL; historical data may have third-party IP considerations; contact provided for concerns.

- Collaboration and contact
  - UKBMS partners offer guidance on dataset use and interpretation.
  - Opportunities for co-authorship and intellectual contribution to scientific outputs.
  - Contacts:
    - Marc Botham, UKBMS (ukbms@ceh.ac.uk)
    - Butterfly Conservation Transect Co-ordinator (transect@butterfly-conservation.org)

- Relevance for GIS specialists
  - Provides a robust, multi-method spatial dataset suitable for map-based biodiversity analysis and policy reporting.
  - Enables creation of species-specific distribution maps, transect coverage maps, and time-series visualizations of site-level data.
  - Supports integration with other spatial datasets (habitat, land use, climate) due to standardized location fields and clear data provenance.