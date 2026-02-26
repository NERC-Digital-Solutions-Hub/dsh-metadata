# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
- It relies on volunteer data collection to provide annual population status data for butterflies across the UK.
- Sampling frameworks include:
  - Standard butterfly transects (Pollard walks): ~2–4 km routes, 5 m wide, weekly counts (up to 26 per year) at ~2000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year at ~800 squares.
  - Targeted surveys: single-species transects, timed counts, egg/larval web counts.
- Data span since 1976, with over 2500 actively recorded sites each year.
- The dataset supports understanding population changes and informing biodiversity and policy questions.

## Nature of data collection and trend analysis

- Data are abundance indices (relative measures) rather than absolute population sizes.
- Indices reflect a constant proportion of butterflies present, with detectability varying by species.
- Trends are combined across sites using the Generalised Abundance Index (GAI, developed 2016) with site-year weighting by the proportion of the species’ flight period surveyed.
- All counts from Pollard walks, WCBS, and other surveys are used to estimate seasonal patterns and to extrapolate gaps; weighting gives observed data greater influence than extrapolated data.

## Quality control

- Field data recorded on standard forms and entered online or via Transect Walker, then uploaded to a central database.
- Automatic checks flag potential data entry errors (e.g., unusually high counts, out-of-flight-period records).
- Regional transect coordinators review data; validation continues throughout the season.
- Additional automated/manual validation checks screen for out-of-range records, distributions, first-time site records, and unusual abundances; edits are made as needed.

## Details of this data download

- Provides long- and short-term trends in collated indices for species with sufficient data, in a CSV file.
- Long-term trends run from 1976 to the year indicated in the file name (some species start later due to data limits).
- Columns include:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years of series)
  - F_LIN_B, F_LIN_SE, F_LIN_P (linear change per year, its SE, and P-value)
  - F_TRENDETAIL (trend description: Rapid decline, Rapid increase, or Stable)
  - F_FULL_R (percentage change over the full series)
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year metrics)
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year metrics)

## Licence and attribution statement

- Data are provided under the Open Government Licence (OGL) with broad use rights.
- Required: cite the dataset with its DOI in any reporting/publication that uses the data.
- Attribution to include with outputs: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer guidance on dataset interpretation and are open to collaboration, including co-authorship on publications or presentations.
- Contact:
  - UKBMS: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org