# About the UK Butterfly Monitoring Scheme

- The UKBMS is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers. It has monitored butterfly abundance in the UK since 1976 across over 2,500 sites annually.
- Purpose: provide annual data on butterfly population status to understand trends and inform biodiversity policy questions.

## Nature of data collection and structure

- Three main components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide belt, recording all species weekly from April to September (~26 counts per year); ~2,000 sites sampled yearly.
  - Reduced effort surveys: single-species transects, timed counts, and egg/larval web counts focusing on specific species or life stages.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares with two parallel 1-km transects; 2–4 visits per year (2 in July/August); ~750 squares sampled yearly.
- Data integration: results from all components are combined to produce species-level indices (abundance indices are relative, not absolute counts). The Generalised Abundance Index (GAI) method (2016) is used to derive collated indices, with site-year weighting based on the proportion of the species flight period surveyed.

## Data quality control and governance

- Field recording uses standard forms; data entered online or via Transect Walker before upload to a central database.
- Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators validate data; ongoing checks during the season.
- Additional automated and manual validation ensures records are within distribution ranges, proper flight periods, and reasonable compared to typical site counts. Any data entry errors are corrected through targeted queries and, if needed, edits to the UKBMS dataset.

## Details of this data download

- Provides long- and short-term trends in collated indices for species with sufficient data, delivered as a CSV.
- Key columns include:
  - COMMON_NAME, SCI_NAME, NYEARS (years in the series)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL (long-term trend slope, its SE, P-value, and qualitative detail)
  - F_FULL_R (overall percentage change)
  - T20_LIN_B/SE/P, T20_TRENDDETAIL, T20_20_R (20-year trend metrics)
  - T10_LIN_B/SE/P, T10_TRENDDETAIL, T10_10_R (10-year trend metrics)

## Licence and attribution

- Data are provided under the Open Government Licence (OGL), enabling free use with minimal conditions.
- Citation requirements (including DOI) must be included in publications using the data.
- Attribution statement to be included: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset use and interpretation, and welcome collaboration and co-authorship opportunities.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology and Hydrology: Marc Botham (ukbms@ceh.ac.uk)