# The UK Butterfly Monitoring Scheme (UKBMS)

- Overview
  - UKBMS collects data from over 2,000 sites annually across the UK to monitor butterfly populations.
  - Population abundance is estimated through standardized counting methods, with site-level indices serving as a relative measure of population size and used to track trends and correlate with other ecological indicators.

- Data collection methods
  - All-species transects
    - Fixed-route line transects (2–4 km) sampled weekly from April to September, in a 5 m wide band.
    - Weather- and time-of-day criteria: counts between 10:45 and 15:45 under suitable conditions (dry, Beaufort wind ≤5, temperature ≥13°C with ≥60% sunshine or >17°C if overcast).
    - Transects are habitat- and management-specific and remain fixed year to year for comparability; typical weekly counts yield about 26 counts per year.
  - Single-species transects
    - Follow the all-species methodology but recorded only on a few weeks during the focal species’ flight period.
  - Timed counts and egg/larval web counts
    - Timed counts: fixed area and time, conducted under the same weather rules.
    - Egg/larval web counts: count eggs or larval webs in suitable habitats for designated species.
  - Wider Countryside Butterfly Survey (WCBS)
    - Reduced-effort survey designed to sample broader countryside habitats (farm landscapes).
    - Based on two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year, with a minimum of 2 visits in July/August.

- Data collection workflow
  - Field data recorded on standard forms; uploaded online via the UKBMS data entry site or Transect Walker software.
  - Data entered by recorders or regional transect coordinators; coordinators consolidate data within their region.
  - Online data and Transect Walker files are uploaded to an Oracle database containing all records.

- Site indices and modeling
  - Site indices are relative measures tied to counts and adjusted for time of year and site area.
  - For transect sites, a General Additive Model (GAM) imputs missing values to compute the site index.
  - WCBS sites are excluded from site-index calculations due to insufficient visits for reliable indices.
  - Indices relate closely to more intensive population measures (e.g., mark-release-recapture).

- Quality control and validation
  - In-field automatic checks in Transect Walker flag unusual counts or species outside known flight periods.
  - Regional transect coordinators validate records and monitor for questionable data throughout the season.
  - Automated and manual validation steps follow, including checks for records outside distribution ranges, out-of-period sightings, first-time records at a site, and extreme or atypical abundances.

- Data format and metadata
  - Site indices stored as text files with columns: Species (scientific name per Fauna Europaea), Common name, Year, Site Index.
  - If a species at a site/year cannot yield an accurate index due to insufficient monitoring, the value is marked as -2.
  - Species naming follows standardized references; common names follow established butterfly nomenclature.

- Practical considerations for analysts
  - Indices are relative, not absolute population sizes, and are suitable for trend analysis and cross-year comparisons.
  - Data gaps and WCBS limitations are acknowledged; GAM-based imputation helps address missing observations in transect data.
  - Data provenance is tracked through field forms, Transect Walker records, and the central Oracle database, with standardized validation for reliability.