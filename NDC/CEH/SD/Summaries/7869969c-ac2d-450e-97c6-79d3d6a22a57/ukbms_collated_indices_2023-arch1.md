# About the UK Butterfly Monitoring Scheme

- Purpose and coordination
  - A long-running program (since 1976) to monitor butterfly population status across the UK.
  - Funded and organized by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - Relies on volunteer data contributors; aims to inform biodiversity status and policy questions.

- Sampling framework and data sources
  - Standard butterfly transects (Pollard walks): fixed-route, typically 2–4 km, 5 m wide band, weekly counts (up to 26 per year) from April to September; 2,000+ sites by 2022.
  - Wider Countryside Butterfly Survey (WCBS): 1 km squares with two parallel transects; 2–3 visits per year (plus optional spring); around 800 squares sampled annually.
  - Targeted surveys: single-species transects, alternative methods (e.g., timed counts, egg/larval web counts) for specific species.
  - Data collection methods yield counts of all butterfly species along transects or via targeted surveys.

- Nature of the data and trend analysis
  - Outputs are abundance indices (relative measures) rather than absolute population sizes.
  - Site indices reflect a constant proportion of butterflies present; detection varies by species.
  - Indices combined using the Generalised Abundance Index (GAI) with a weighting adjustment for the proportion of the flight period surveyed each year per site.
  - GAI uses all counts in a season to estimate a yearly seasonal pattern and extrapolate gaps, with observed data weighted more heavily than extrapolated data.

- Quality control and data hygiene
  - Field data recorded on standard forms, entered online via UKBMS MyData or Transect Walker, then uploaded to central databases.
  - Automatic checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
  - Regional transect coordinators validate data; ongoing checks throughout the season.
  - Additional automated and manual validation to flag records outside known distributions, out-of-period observations, first-time site records, or aberrant abundances; edits applied through queries in coordination with data recorders.

- Details of this data download
  - Contains annual collated indices of abundance for species with sufficient data from 1976–2023 (some early years exclude certain species due to limited data).
  - Provided as a CSV with columns:
    - SPECIES_CODE, SPECIES, COMMON_NAME
    - YEAR, N_SITES
    - COLLATED_INDEX (log10 of the Collated Index, scaled so average across the series equals 2)
    - YEAR_RANK (yearly rank among years for that species)
    - TIME_PERIOD, COUNTRY
  - The Collated Index uses the full season’s counts (Pollard walks, reduced surveys, WCBS) to estimate the seasonal pattern and account for sampling gaps.

- Licence and attribution
  - Open Government Licence (OGL) enables wide use with few conditions.
  - Must include citation with DOI in any reports/publications; attribution statement required: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.

- Offer of collaboration and contact details
  - UKBMS Partners offer guidance on dataset use and interpretation; potential for co-authorship and intellectual input in publications, conferences, or posters.
  - Contacts:
    - Marc Botham, UK CEH: ukbms@ceh.ac.uk
    - Butterfly Conservation Transect Co-ordinator: transect@butterfly-conservation.org