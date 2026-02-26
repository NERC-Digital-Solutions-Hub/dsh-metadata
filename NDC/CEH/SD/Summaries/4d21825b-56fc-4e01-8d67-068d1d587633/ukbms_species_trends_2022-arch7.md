# About the UK Butterfly Monitoring Scheme

- The UKBMS is organized and funded by Butterfly Conservation, CEH, BTO, and JNCC; relies on volunteer data collection; ongoing since 1976 with over 3000 active sites annually.
- Purpose: track population status of butterflies to support biodiversity status and policy questions; data cover multiple sampling frameworks and methods.

## Data collection and spatial scope

- Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, ~5 m wide, weekly counts (up to 26 visits) from April to September; 2000+ sites monitored annually by 2022.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, two parallel transects per square, 2–3 visits per year (July/August prioritized; spring visits encouraged); ~800 squares sampled per year.
- Targeted surveys: single-species transects, timed counts, and egg/larval web counts; methods adapted for specific species.
- Data are spatially explicit at multiple scales (sites and 1 km squares) and integrate across methods for broad trend analysis.

## Data types and trend metrics

- Abundance indices: relative measures of butterfly abundance rather than absolute counts.
- Data synthesis: Generalised Abundance Index (GAI) to produce species-level collated indices; weights site-year data by the proportion of the species flight period observed to balance observed vs. extrapolated counts.
- Trend outputs: long-term (from 1976 or start year to 2022) and shorter-term trends (e.g., last 20 and last 10 years) with slopes, standard errors, and p-values.
- Trend descriptors include textual classifications (e.g., rapid decline, rapid increase, stable) based on slope direction and significance.
- Columns provided in downloads describe species names (common and scientific), years, slope measures, errors, p-values, trend details, and percent changes over various intervals.

## Quality control and data validation

- Field data recorded on standard forms; entered online via UKBMS portal or Transect Walker; uploaded to a central database.
- Automated checks flag implausible counts or out-of-season records; regional transect coordinators perform ongoing validation.
- Further automated/manual validation ensures consistency with known distributions, flight periods, and site history; data edits are made as needed.

## Data download specifics (for GIS use)

- Format: CSV file containing long- and short-term trends for species with adequate data.
- Time coverage: long-term series from 1976 to 2022 (start year may vary by species due to data availability).
- Key columns include:
  - COMMON_NAME, SCI_NAME
  - NYEARS (years covered)
  - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL, F_FULL_R
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
- Data suitable for GIS analysts to plot species trends over time and across spatial units (sites and 1 km squares).

## Licence and attribution

- Data released under Open Government Licence (OGL); free use with few conditions.
- Must cite the dataset with its DOI in any publications or reports describing research using the data.
- Attribution statement required: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact

- UKBMS partners offer guidance on using and interpreting the dataset; co-authorship and intellectual input for publications possible.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)