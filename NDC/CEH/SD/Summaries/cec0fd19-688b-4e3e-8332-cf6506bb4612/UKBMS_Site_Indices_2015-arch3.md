# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
- Data are primarily gathered through fixed-route transects known as Pollard walks, with additional methods for some species and sites.

## Monitoring Methods and Data Types
- All-species transects
  - Fixed-route 2–4 km transects recording all butterfly species within a ~5 m wide band.
  - Typically 26 counts per year from April to September; weekly surveys under suitable weather.
  - Transects are fixed to enable year-to-year comparisons and are divided into habitat/management sections.
  - Weather criteria: observations between 10:45 and 15:45, dry conditions, wind Beaufort ≤ 5, temperature thresholds depending on sunshine/overcast.
- Single-species transects
  - Follow the all-species methodology but record for a reduced number of weeks during the focal species’ flight period.
- Timed counts and egg/larval web counts
  - Timed counts: counts of a focal species over a set period/area within weather constraints.
  - Egg/larval web counts: counting eggs or larval webs in suitable habitat.
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey started in 2009 to sample farmland and wider habitats.
  - Based on two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits (minimum two in July/August), spring visits encouraged.

## Data Collection and Processing
- Field data are recorded on standard forms and entered online or via Transect Walker software.
- Data entry is performed by recorders or regional transect coordinators; coordinators compile data for their region.
- Online data and Transect Walker files are uploaded to an Oracle database.
- Site indices are calculated for sites with sufficient monitoring visits; GAM (General Additive Model) imputes missing values for transect sites.
- WCBS sites are excluded from site index calculations due to insufficient visits for accurate indices.

## Nature and Units of Recorded Values
- Site indices are relative measures of population size, not absolute counts.
- Indices correlate with more intensive population size measures (e.g., mark-release-recapture) and represent a constant proportion of actual abundance, varying by species.

## Quality Control and Validation
- Automated checks in Transect Walker flag potential data entry errors (e.g., unusually high counts, records outside flight periods).
- Regional transect coordinators review records for plausibility and consistency.
- Additional automated and manual validation processes include checks against known distributions, flight periods, first-time site records, and atypical abundances.

## Data Storage and Format
- Site indices are stored as a text file (.txt) with columns:
  - Species (scientific name, following Fauna Europaea)
  - Common name (vernacular, following standard references)
  - Year (year of the site index)
  - Site Index (relative index value)
- If a site was not monitored sufficiently to calculate an index for a given year, the value is -2.

## Notes and References
- Key methodological basis includes Pollard, E. & Yates, T.J. (1993) Monitoring Butterflies for Ecology and Conservation.
- GAM methodology for imputation described by Rothery, P. & Roy, D.B. (2001) in Journal of Applied Statistics.