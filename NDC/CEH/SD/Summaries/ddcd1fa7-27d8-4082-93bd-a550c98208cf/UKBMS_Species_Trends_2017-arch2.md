# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data, with the scheme tracking butterfly population status annually since 1976.
- It supports policy-relevant understanding of biodiversity changes by providing long-term, site-based data augmented with random 1-km square sampling.

## Data collection and monitoring framework

- Components:
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m recording band, weekly counts from April to September (aim ~26 counts/year), ~2000 sites annually.
  - Reduced effort surveys: single-species transects or alternative methods (e.g., timed counts, egg/larval web counts) focusing on specific species or periods.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1-km squares with two parallel 1-km transects; 2–4 visits per year (typically July/August), ~750 squares sampled annually.
- Sampling intensity and effort are tailored to habitat types (farmland, etc.), building a comprehensive UK-wide picture of butterfly abundance.

## Nature of data and trend analysis

- Data are expressed as abundance indices (relative, not absolute counts) derived from transect counts, reflecting proportional population changes at sites.
- Trend aggregation uses the Generalised Abundance Index (GAI) method (2016) with weighting by the proportion of the species’ flight period surveyed at each site/year, combining data from all components to generate species-level collated indices.
- The approach accounts for gaps in recording and aims to weight observed data more than extrapolated values.

## Quality control

- Field data are collected on standard forms and entered online via the UKBMS data portal or Transect Walker software, then uploaded to a central database.
- Automated checks flag improbable values (e.g., abnormally high counts, records outside flight periods). Regional transect coordinators validate data, and continuous quality checks run throughout the season.
- Further automated/manual validation screens for out-of-range distributions, unusual timing, new-site records, or extreme/unexpected abundances; corrections are made through data queries and coordination with recorders as needed.

## Details of this data download

- Provides long- and short-term trend data in collated indices for species with sufficient data, in CSV format.
- Columns include:
  - COMMON_NAME, SCI_NAME, NYEARS
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL, F_FULL_R
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R

- Interpretations:
  - F_* fields describe annual growth rates, uncertainty, and qualitative trend descriptions over the full series.
  - T20_* fields describe trends and change over the last 20 years; T10_* over the last 10 years.
  - Trend detail fields (“Rapid decline”, “Rapid increase”, “Stable”) indicate direction and statistical significance (P-values).

## Licence and attribution

- Data are published under the Open Government Licence (OGL), permitting free use with minimal conditions.
- Must include the citation/DOI in references for publications using the data, and include the attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS Partners offer guidance on dataset use and interpretation, and welcome collaboration and co-authorship on publications arising from UKBMS data.
- Contacts:
  - Tom Brereton, Butterfly Conservation: tbrereton@butterfly-conservation.org
  - Marc Botham, CEH: ukbms@ceh.ac.uk