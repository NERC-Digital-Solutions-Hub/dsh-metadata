# 1. About the UK Butterfly Monitoring Scheme

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - It relies on volunteers and has monitored butterfly abundance across the UK since 1976.
  - The dataset supports understanding insect population changes and informs biodiversity status and policy questions.
  - Each year, the scheme tracks data from over 2,500 actively recorded sites.

- Sampling framework
  - Standard butterfly transects (Pollard walks): fixed routes, 2–4 km, monitored weekly (ideally 26 counts/year) across habitats; about 1,900 sites annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares with two parallel 1-km transects, 2–3 visits per year (plus optional spring visits); ~800 squares annually.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species or situations.

- Data and trend analysis
  - Outputs are abundance indices (relative measures) rather than absolute counts.
  - Indices are combined using the Generalised Abundance Index (GAI, 2016) with site- and year-weighting to reflect sampling effort and flight period coverage.
  - All sampling methods are integrated to estimate seasonal counts, enabling extrapolation for gaps; observed data are weighted more heavily than extrapolated data.
  - Data from Pollard walks, WCBS, and reduced surveys are used to derive species-specific collated indices.

- Quality control
  - Field data are collected on standard forms and entered online via the UKBMS data entry site or Transect Walker.
  - Automatic checks flag anomalies (e.g., unusually high counts, out-of-period records) and regional coordinators review data.
  - Additional automated and manual validation checks ensure records fall within known distribution ranges and expected flight periods; corrections are made through data queries and coordination with recorders.

- Details of this data download (format and content)
  - Provides annual collated indices of abundance for UK species with sufficient data, covering 1976–2020 (some early years excluded for insufficient data).
  - Delivered as a CSV file with columns:
    - SPECIES CODE: unique species number
    - SPECIES: scientific name (Fauna Europaea)
    - COMMON NAME: vernacular name
    - YEAR: year of the collated index
    - NO. SITES: number of contributing sites
    - COLLATED INDEX: log10 of the collated index; scaled so the series average equals 2
    - YEAR RANK: year-specific rank for the species across years
    - TIME PERIOD: time period used to compute indices
    - COUNTRY: country/region data source for regional indices

- Licence and attribution
  - Open Government Licence (OGL): free use with few conditions.
  - Must include citation details (DOI) as provided in metadata records.
  - Attribution statement: Contains UKBMS data © Butterfly Conservation, UKCEH, BTO, JNCC.

- Offer of collaboration and contact details
  - The UKBMS partners welcome collaboration, interpretation support, and co-authorship opportunities for publications derived from UKBMS data.
  - Contacts:
    - UKCEH: Marc Botham (ukbms@ceh.ac.uk)
    - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)