# The UK Butterfly Monitoring Scheme (UKBMS)

- A national effort collecting butterfly data from over 2,000 sites annually across the UK to monitor environmental health and policy performance over time.
- Data are gathered using standardized, fixed-route transects and standardized counting methods to enable year-to-year comparability and broader environmental assessments.

## What is monitored and how

- All-species transects (Pollard walks)
  - Fixed-route line transect at each site, typically 2–4 km, divided into habitat/management units.
  - All butterfly species counted in a fixed 5 m wide band along the transect each week from early April to late September (ideally 26 counts per year).
  - Walks occur only under suitable butterfly activity weather (roughly 10:45–15:45; dry; wind < Beaufort 5; temperature thresholds with sunshine or overcast conditions).
  - Transects are kept fixed to allow year-on-year comparisons; dominant method across > half of sites (over 1,000 sites recently).
- Single-species transects
  - Follow the same methodology as all-species transects but recorded only for several weeks during the focal species’ flight period.
- Timed counts and egg/larval web counts
  - Timed counts record the abundance of a particular species over a set period and area (within the standard weather window).
  - Egg and larval web counts record eggs or larval webs for species in suitable habitats.
- Wider countryside butterfly survey (WCBS)
  - Reduced-effort survey imitating the BTO Breeding Bird Survey approach.
  - Two parallel 1-km transects within randomly selected 1-km squares; subdivided into 10 sections.
  - 2–4 visits per site (minimum of 2 visits in July/August; spring visits encouraged).

## Data collection and entry

- Field data recorded on standard forms, then entered online (UKBMS data entry site) or via Transect Walker software.
- Data entry by recorders or regional transect coordinators; end-of-season data collection consolidated by regional coordinators.
- Online data and Transect Walker files uploaded to an Oracle database containing all records.
- Site indices calculated for sites with sufficient monitoring; WCBS indices excluded due to limited visits.

## Data processing and analysis

- Site indices
  - Relative measures of population size (not absolute counts), representing a proportion of butterflies present at a site.
  - Correlate with more intensive population size measures (e.g., mark-release-recapture) for validation.
- Handling missing data
  - General Additive Models (GAMs) used to impute missing values and compute site indices for transect sites.
- WCBS
  - Not used for site indices because WCBS data are based on a limited number of visits and do not yet support robust index estimation.

## Quality control and validation

- In-field automated checks in Transect Walker flag potential data entry errors (e.g., abnormally high counts, records outside flight periods).
- Regional transect coordinators review records for questionable data; continuous validation during the season.
- Additional automated/manual validation checks post-entry to identify records outside known distribution, unusual flight periods, first-time site records, and extreme or atypical abundances.

## Data formats and storage

- Site indices stored as text files (.txt) with columns:
  - Species (scientific name per Fauna Europaea)
  - Common name (per Emmet & Heath)
  - Year
  - Site Index (relative abundance)
- If a species at a site in a year cannot have an accurate index due to insufficient monitoring, the value is recorded as -2.
- Taxonomic references used: Fauna Europaea (version 2.2) and standard butterfly references.

## Temporal and environmental constraints

- Transect timing and weather criteria are essential to ensure comparability across years and sites.
- Weather-related thresholds and fixed sampling periods are designed to maximize detectability and consistency of counts.

## Outputs, usage, and data access

- Outputs include site indices, which form the basis for assessing environmental health and policy performance over time.
- Outputs are presented as reports, maps, and charts to support monitoring and decision-making.
- The data infrastructure (standardized formats, QA processes, and portal storage) is designed to increase dataset value and enable access to underlying data for broader analysis and integration with other environmental data sources.

## Key references

- Pollard, E. & Yates, T.J. (1993). Monitoring Butterflies for Ecology and Conservation.
- Rothery, P. & Roy, D.B. (2001). Application of generalized additive models to butterfly transect count data. Journal of Applied Statistics.
- Butterfly Conservation resources (Butterflies for the New Millennium, BN M) and related UKBMS data management practices.