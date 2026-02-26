# About the UK Butterfly Monitoring Scheme

- Organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee; relies on volunteers.
- Annual data track butterfly population status across the UK since 1976; currently involves over 2,500 actively recorded sites each year.
- Data come from a multi-component sampling framework and are analyzed together to support understanding of insect population changes and biodiversity policy questions.
- Core components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide band, weekly counts (up to 26 per year), typically ~2,000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel 1 km transects, 2–3 visits per year, sampling ~750 squares.
  - Targeted surveys: single-species transects and other methods (timed counts, egg/larval web counts) focused on specific species.
- Foundational references: Pollard & Yates (1993); ongoing methodology noted.

# Nature of data collected and trend analysis

- Data are abundance indices (relative measures) derived from counts along transects and sites; not absolute population sizes.
- Site indices reflect a constant proportion of local populations, with detectability varying by species.
- Collated indices for species produced using the Generalised Abundance Index (GAI) method (2016) with a weighting adjustment:
  - Data from each site/year weighted by the proportion of the species’ flight period observed at that site/year.
  - Uses all counts across survey methods to model seasonal patterns and extrapolate gaps, giving more weight to observed data.
- Methodology integrates multiple data sources and years to produce species-level trends.

# Quality control

- Field data recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker; then uploaded to a central database.
- Automatic checks flag potential errors (e.g., abnormally high counts, records outside known flight periods); recorders can adjust or proceed.
- Regional transect coordinators validate data for their regions; continuous checks during the season.
- Further automated/manual validation includes queries for records outside distribution, out-of-season records, first-time site records, and anomalous abundances; corrections involve coordinators and interview-based data adjustments.

# Details of this data download

- Provides annual collated indices of abundance for species with sufficient data from 1976–2019 (earlier years may lack collated indices due to insufficient data).
- File format: CSV (comma-separated values).
- Columns described:
  - SPECIES CODE: unique species number
  - SPECIES: scientific name (Fauna Europaea, version 2.2)
  - COMMON NAME: vernacular name (Emmet & Heath)
  - YEAR: year of the collated index
  - NO. SITES: number of sites contributing to the collated index for that year
  - COLLATED INDEX: log10 of the Collated Index, scaled so average across the series equals 2
  - YEAR RANK: rank of the CI value for that year for the species (1 = best year)
  - TIME PERIOD: time period used to produce the indices
  - COUNTRY: country from which data were used for the regional index

# Licence and attribution statement

- Data download is provided under the Open Government Licence (OGL); allows free use with few conditions.
- Citation: include the metadata DOI in references when describing research using the data.
- Attribution: include the statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC” with any information or images derived from the data.

# Offer of collaboration and contact details

- Partners offer advisory support on dataset details and interpretation of outputs.
- Potential for co-authorship and intellectual input on scientific publications, conference presentations, or posters resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
  - Butterfly Conservation, Transect Co-ordinator: transect@butterfly-conservation.org