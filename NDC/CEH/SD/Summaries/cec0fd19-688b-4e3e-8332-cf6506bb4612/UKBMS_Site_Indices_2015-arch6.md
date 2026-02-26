# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 2,000 sites annually across the UK.
- Data include all-species transects, single-species transects, timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).
- Site indices are relative measures of population size, used to track trends over time rather than providing absolute counts.

## Data collection methods
- All-species transects
  - Fixed-route, 2–4 km long, divided into habitat/management sections.
  - Record all butterfly species within a fixed 5 m wide band.
  - Approximately 26 counts per year (weekly) from April to September.
  - Walks occur between 10:45 and 15:45 under suitable butterfly activity conditions.
  - Weather criteria: dry, wind < Beaufort 5, temperatures of ≥13°C (sunny) or ≥17°C (overcast).
- Single-species transects
  - Follows the all-species method but records only during a few weeks for the focal species.
- Timed counts and egg/larval web counts
  - Timed counts: abundance of a species over a set period/area, following same time/weather rules.
  - Egg/larval counts: number of eggs or larval webs in suitable habitat areas.
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort sampling in wider countryside habitats (farmland, etc.).
  - Two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year, minimum 2 visits in July/August.
  - Based on the Breeding Bird Survey (BBS) methodology.

## Data collection and entry
- Field data recorded on standard forms.
- Online data entry via the UKBMS data entry site or Transect Walker software (free download).
- Data may be entered by the recorder or by a regional transect coordinator.
- Transect coordinators compile data for their region; online data and Transect Walker files are uploaded into an Oracle database.

## Data processing and site indexing
- Site indices are computed only for sites with sufficient monitoring visits.
- For timed/egg/larval counts, indices are typically derived from counts near the peak of the flight period and adjusted for time of year and site area.
- For transect data, missing values are imputed using a General Additive Model (GAM).

## Quality control and validation
- Automatic checks in Transect Walker flag potential errors (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators perform ongoing validation throughout the season.
- Additional automated/manual validation includes cross-checks for records outside known distribution ranges, unusual first-time site records, and extreme or abnormal abundances.
- Distribution range checks reference Butterfly Conservation data and existing UKBMS data.

## Data format and units
- Site indices are relative measures, not absolute population sizes; correlations exist with more intensive methods (e.g., mark–release–recapture).
- Data stored as a text file with columns:
  - Species (scientific name, Fauna Europaea)
  - Common name
  - Year
  - Site Index
- If a species at a site/year cannot yield an accurate index due to insufficient monitoring, the value is -2.

## Key references
- Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation.
- Rothery, P. & Roy, D.B. (2001). Application of generalized additive models to butterfly transect count data.
- BNMs (Butterflies for the New Millennium) data used for distribution checks.