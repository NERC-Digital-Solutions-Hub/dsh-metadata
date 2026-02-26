# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collates data from over 2,000 sites annually across the UK.
- Population abundance is estimated using standardized methods, primarily fixed-route transects, with some species-specific methods (timed counts, egg/larval web counts).
- Data are used to monitor environmental health and policy performance over time, enabling consistent longitudinal comparisons.

## Monitoring methods

- All-species transects
  - Fixed-route line transect at a site; 2–4 km long, divided into habitat/management sections.
  - All butterfly species recorded in a 5 m wide belt along the transect.
  - Weekly counts from early April to late September; aim for 26 counts per year.
  - Transect routes are fixed to allow year-to-year comparisons.
  - Weather constraints: counts conducted when butterfly activity is likely (dry; wind < Beaufort 5; temperature thresholds depending on sunshine or cloud cover).

- Single-species transects
  - Follow the all-species transect methodology but recorded only for weeks during the focal species’ flight period.

- Timed counts and egg/larval web counts
  - Timed counts: abundance of a focal species recorded over a set time in a defined area (weather constraints as above).
  - Egg/larval web counts: count eggs or larval webs of a species in suitable habitat areas.

- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort sampling in wider countryside habitats (farmland, etc.).
  - Based on the BTO Breeding Bird Survey (BBS) design: two parallel 1-km transects within randomly selected 1-km squares.
  - 2–4 visits per site, minimum 2 visits in July/August (spring visits encouraged).
  - Uses the fixed-route transect methodology of UKBMS all-species transects.

## Data collection, entry and quality control

- Field data recorded on standard forms; online data entry via UKBMS site or Transect Walker software.
- Data are entered by recorders or regional transect coordinators; coordinators compile data for their region.
- Data uploaded to an Oracle database hosting all records.
- Site indices are calculated only for sites with sufficient monitoring; WCBS indices excluded due to insufficient visits for accurate indices.
- For transect sites, a General Additive Model (GAM) imputes missing values and computes the site index.

## Data format, units and interpretation

- Site indices are relative measures of population size (not absolute counts) and correlate with more intensive methods like mark–release–recapture.
- The relative index reflects a constant proportion of the true population, varying by species visibility.
- Data validation and quality checks:
  - Automatic checks in Transect Walker flag potential data entry errors (e.g., abnormally high counts, records outside flight periods).
  - Regional coordinators review records; online data also validated continuously.
  - Further automated/manual validation targets records outside known distribution, outside normal flight periods, first-time site records, and anomalous counts.

- Stored data format for site indices:
  - Columns include: Species (scientific name per Fauna Europaea v2.2), Common name, Year, Site Index.
  - If a species is recorded at a site in a year but the site was not monitored sufficiently to calculate an index, the value is -2.

## Outputs and implications

- Site indices provide standardized, comparable measures of butterfly population status across sites and years.
- Outputs support environmental health assessments and policy performance monitoring over time.
- Data management enables ongoing storage, aggregation, and potential sharing with portals for broader access.

## Key notes for analysts

- The fixed transect approach and GAM-based imputation are central to producing comparable site indices.
- Quality control is multi-layered (in-field checks, regional review, and automated validation) to maintain data reliability.
- WCBS offers broader countryside coverage but currently does not yield site indices due to limited visits at some sites.