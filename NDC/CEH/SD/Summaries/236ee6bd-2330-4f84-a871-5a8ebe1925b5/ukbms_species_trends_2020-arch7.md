# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, CEH, BTO, and JNCC, with significant volunteer contributions.
- It provides annual data on butterfly population status from a wide-scale, site-based monitoring program across the UK since 1976.
- Spatial coverage includes over 2,500 active sites each year, with data collected through multiple sampling methods that are analyzed together to understand biodiversity status and trends.
- This dataset is intended to support map-based visuals and spatial analyses for policy, clients, and public audiences.

## What is collected and how data are generated

- Standard butterfly transects (Pollard walks): fixed routes (2–4 km) with weekly counts (about 26 counts/year) across a 5 m width, covering early April to late September; ~2,000 sites sampled annually.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (plus encouraged spring visits); ~800 squares sampled annually.
- Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on specific species or life stages.
- Data are collected across multiple methods and combined for analysis.

## How trends are calculated and presented

- Indices are abundance-based, relative measures derived from counts on transects and sites.
- Collated species indices are produced using the Generalised Abundance Index (GAI) with a weighting adjustment that accounts for the proportion of the flight period surveyed at each site/year.
- Seasonal patterns are estimated from all counts to handle gaps in recording and extrapolate data, with greater weight given to observed data.
- Outputs include long-term trends (start year varies by species) and short-term trends (last 20 and last 10 years), with detailed statistics per species:
  - Overall and recent yearly change (slope) with standard errors and P-values
  - Descriptions of trend direction (rapid decline, rapid increase, stable)
  - Percent change measures over the full series and the last 20/10 years

## Quality control

- Field data are recorded on standard forms and entered online via UKBMS tools or Transect Walker, then uploaded to a central database.
- Automated checks flag potential data-entry errors; regional transect coordinators perform ongoing validation.
- Additional automated/manual validation screens for out-of-range distributions, abnormal abundances, atypical flight periods, and first-at-site records.
- Corrections are implemented through queries and coordination with coordinators/recorders.

## Details of this data download

- Provides long- and short-term trends in collated indices for species with sufficient data, delivered as a CSV file.
- Columns include:
  - COMMON_NAME, SCI_NAME, NYEARS (years of series)
  - F_LIN_B, F_LIN_SE, F_LIN_P (overall trend slope, SE, P)
  - F_TRENDETAIL (trend description)
  - F_FULL_R (percent change over the full series)
  - T20_LIN_B/SE/P, T20_TRENDDETAIL, T20_20_R (20-year trend metrics)
  - T10_LIN_B/SE/P, T10_TRENDDETAIL, T10_10_R (10-year trend metrics)
- Start years can vary by species due to data availability.

## Licence and attribution

- This data download is provided under the Open Government Licence (OGL) for flexible use and reuse.
- Citations/DOI must be included in publications using the data.
- Attribution statement to include: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.
- Open access license details and attribution requirements are provided in the accompanying metadata.

## Collaboration and contact information

- UKBMS partners offer guidance on dataset details and result interpretation.
- Opportunities for co-authorship and intellectual input in scientific outputs are available.
- Contacts:
  - UK Centre for Ecology & Hydrology – Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation – Transect co-ordinator (transect@butterfly-conservation.org)