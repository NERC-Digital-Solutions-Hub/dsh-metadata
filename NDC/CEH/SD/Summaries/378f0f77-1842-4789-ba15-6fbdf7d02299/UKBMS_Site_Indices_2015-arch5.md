# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK.
- Data include butterfly counts from fixed transects (Pollard walks) and standardized methods such as timed counts or egg/larval web counts.
- All-species transects and reduced-effort Wider Countryside Butterfly Survey (WCBS) transects are used, with WCBS established in 2009 to sample wider habitats.
- Site indices provide a relative measure of population size, enabling year-to-year comparisons.

## Data collection methods
- All-species transects: fixed-route, 2–4 km, 45 minutes to 2 hours, 26 counts per year from April to September; counts recorded in a 5 m wide band along the transect.
- Transect timing and conditions: counts occur 10:45–15:45 and require suitable butterfly activity (weather criteria specified).
- Single-species transects: follow all-species methodology but recorded for a few weeks during the focal species’ flight period.
- Timed counts and egg/larval web counts: focus on specific species or life stages during defined time periods.
- WCBS: two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year (minimum two visits in July/August), sampling farmland and other wider habitats.
- Data are collected on standard field forms and entered online or via Transect Walker software.

## Data handling and processing
- Field data are entered by the recorder or regional transect coordinators and uploaded to an Oracle database.
- Each transect coordinator aggregates data for their region at season end.
- Site indices for transect sites are derived using a General Additive Model (GAM) to impute missing values and compute indices; WCBS sites are excluded from index calculations due to limited visits.
- Data are cross-validated against known distributions and flight periods, with automated and manual checks.

## Quality control
- Automatic checks within Transect Walker flag potential data entry errors (e.g., unusually high counts, records outside flight periods).
- Regional coordinators review data for questionable records; online submissions are subject to continuous validation throughout the season.
- Additional validation includes checks for records outside species’ known distribution, unusual abundance patterns, or first-time site records.

## Data storage and format
- Site indices are stored as text files (.txt) with columns including:
  - Species (scientific name, following Fauna Europaea)
  - Common name (following standard reference)
  - Year
  - Site Index (relative population size)
- If a site was not monitored sufficiently to calculate an accurate index for a given species in a year, the value is recorded as -2.
- Species vocabulary for data processing references established taxonomic and common-name sources (Fauna Europaea, Emmet & Heath).

## Data standards and governance notes
- Data are structured to support cross-site comparability and long-term trend analysis.
- Cross-referencing with external datasets (e.g., distribution records and flight period baselines) informs validation and quality checks.
- The workflow supports updates and ongoing data quality assurance, with explicit handling of incomplete monitoring (e.g., WCBS exclusion from indices).

## References and methodological notes
- Methodological details reference Pollard & Yates (1993) for transect concepts.
- GAM-based imputation methods described by Rothery & Roy (2001) underpin site-index calculations.