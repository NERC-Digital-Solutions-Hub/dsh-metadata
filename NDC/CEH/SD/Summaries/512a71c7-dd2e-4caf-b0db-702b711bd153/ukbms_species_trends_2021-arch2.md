# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data, and the scheme has monitored butterfly population changes across the UK since 1976, currently with over 2500 active sites annually.
- Data derive from a mix of site-based monitoring using three main components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide band, recorded weekly from April to September (ideally 26 counts/year; ~2000 sites).
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (20–30 visits total are typical across the year), sampling around 800 squares/year.
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focusing on particular species or life stages.
- Data are used to understand changes in insect populations and inform biodiversity policy, with an integrated dataset from all sampling methods analyzed together.

## Data collection and sampling framework

- The sampling framework combines multiple data streams:
  - Pollard walks (standard transects)
  - WCBS transects (stratified random 1 km squares)
  - Targeted surveys (single-species transects and other methods)
- Surveillance is ongoing across a wide geographic area, enabling long-term trend analysis and policy-relevant biodiversity monitoring.

## Data structure and trend analysis

- UKBMS relies on abundance indices (relative measures of population size) derived from counts along transects and sites.
- A Generalised Abundance Index (GAI) method (2016) combines site-level indices into species-wide collated indices, with a modification to weight data from each site by the proportion of the species’ flight period surveyed in that year. This helps account for gaps in recording.
- All counting data (Pollard walks, reduced surveys, WCBS) are used to model the seasonal pattern for each year, which informs extrapolation to missing data. Observed data are given more weight than extrapolated data.

## Quality control

- Data are collected on standard forms in the field, entered online (via UKBMS MyData or Transect Walker), and uploaded to a central database.
- Automated checks flag potential data entry errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators validate records and monitor for questionable data.
- A series of automated and manual validation steps follow, including checks for:
  - Records outside known distribution ranges
  - Flights outside normal periods
  - First records at a site
  - Extreme or anomalous abundances
- Corrections are made through queries and, if needed, edits to the main UKBMS dataset through coordination with transect recorders/coordinators.

## Details of this data download

- The download provides long- and short-term trends in collated indices for all species with sufficient data, in a CSV (.csv) format.
- Time frames:
  - Long-term trends: from 1976 to the year indicated in the file name (start year may be later for some species due to insufficient early data).
- Columns and key metrics included:
  - COMMON_NAME: common names (per Emmet & Heath, 1990)
  - SCI_NAME: scientific names (per Agassiz et al., 2013, with later updates)
  - NYEARS: number of years the trend is calculated
  - F_LIN_B, F_LIN_SE, F_LIN_P: slope, standard error, and p-value for the long-term trend
  - F_TRENDETAIL: textual interpretation of the long-term trend (Rapid decline, Rapid increase, Stable)
  - F_FULL_R: percentage change over the full series
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R: 20-year trend metrics
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R: 10-year trend metrics
- These fields provide a structured view of how species populations have changed over time and in recent periods.

## Licence and attribution

- The data download is provided under an Open Government Licence (OGL), enabling free use with few conditions.
- Users must include the citation (including DOI) as provided in the metadata when describing research based on the data.
- Attribution to use with any information or images derived from the data: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS partners offer assistance with dataset details and interpretation of outputs.
- Collaboration is welcome, including co-authorship and intellectual input for scientific outputs (papers, conferences, posters).
- Contact:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation: Transect co-ordinator, transect@butterfly-conservation.org