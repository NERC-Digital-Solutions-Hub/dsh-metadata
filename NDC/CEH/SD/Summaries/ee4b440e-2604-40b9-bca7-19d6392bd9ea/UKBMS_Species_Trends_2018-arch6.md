# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the Centre for Ecology and Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee. Volunteers contribute data; the scheme has monitored butterfly abundance since 1976 and now involves over 2,500 actively recorded sites annually.
- The dataset supports understanding changes in insect populations and informs biodiversity policy questions.

## Data collection components

- Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects; record all butterfly species in a 5 m band each week from April to September; about 1,900 sites are sampled each year.
- Reduced effort surveys: single-species transects (same methodology but for selected species and fewer weeks), timed counts (abundance over a set period/area), egg and larval web counts (eggs/larval webs in suitable habitat).
- Wider Countryside Butterfly Survey (WCBS): similar transect method but in stratified-random 1 km squares; 2–4 visits per site per year (minimum two visits in July/August); ~750 squares sampled annually since 2009, focusing on common habitats like farmland.

- All components are analyzed together to produce integrated species-level indices.

## Data processing and trend analysis

- UKBMS uses abundance indices (relative measures, not absolute counts) derived from counts along transects and sites.
- Collated species indices are generated using the Generalised Abundance Index (GAI, 2016) with weighting that accounts for the proportion of the flight period surveyed each year at each site; this combines all seasonal counts to estimate the year’s seasonal pattern and extrapolate gaps.
- Weighting gives observed data greater influence over extrapolated data, supporting robust trend estimation across methods and years.

## Quality control

- Field data are collected on standard forms and entered online (UKBMS mydata) or via Transect Walker; records are uploaded to a central database.
- Automated checks flag anomalies (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators review data; ongoing validation includes checks for out-of-range distributions, unusual flight times, first-time site records, and extreme values.
- Corrections are made through queries and discussions with coordinators/recorders; edits update the master UKBMS dataset.

## Details of this data download

- Provides long- and short-term trends in collated indices for all species with sufficient data; format: CSV.
- Columns include:
  - COMMON_NAME: vernacular species names (Emmet & Heath, 1990)
  - SCI_NAME: scientific names (Fauna Europaea v2.2)
  - NYEARS: number of years the series trend covers
  - F_LIN_B, F_LIN_SE, F_LIN_P: annual slope, standard error, and p-value for the overall (long-term) trend
  - F_TRENDETAIL: narrative trend category (Rapid decline, Rapid increase, Stable) for the long-term trend
  - F_FULL_R: percent change over the full series
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R: 20-year trend metrics and description
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R: 10-year trend metrics and description

## Licence and attribution

- Data are provided under the Open Government Licence (OGL) with flexible use; citation requirements apply, including the DOI in any publications using the data.
- Attributions must include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, the Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.

## Collaboration and contact details

- UKBMS partners offer advisory support and interpretation of outputs; collaboration and co-authorship on publications and presentations are welcome.
- Contacts:
  - Butterfly Conservation: Tom Brereton (tbrereton@butterfly-conservation.org)
  - Centre for Ecology and Hydrology: Marc Botham (ukbms@ceh.ac.uk)