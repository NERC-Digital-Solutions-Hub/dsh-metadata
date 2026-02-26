# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects butterfly data from over 2,000 sites annually across the UK.
- Data collection uses standardized methods, primarily fixed-line transects (Pollard walks) for all-species counts, plus reduced-effort Wider Countryside Butterfly Survey (WCBS) transects and other methods (timed counts, egg/larval web counts) for specific species or contexts.
- Data are used to estimate population abundance through site-specific indices rather than absolute counts, enabling year-to-year comparisons.

## Data Collection Methods
- All-species transects:
  - Fixed-route 2–4 km lines sampled weekly during favorable butterfly activity (weather-dependent).
  - Route sections map to habitat/management units; counts occur in a 5 m band along the transect from April to September (ideally 26 counts/year).
  - Transects typically 45 minutes to 2 hours; sampling times 10:45–15:45.
- Single-species transects:
  - Follows the all-species methodology but only during focal species flight periods.
- Timed counts and egg/larval web counts:
  - Timed counts: fixed area and time period, weather-appropriate.
  - Egg/larval web counts: count eggs or larval webs in suitable habitat areas.
- WCBS (Wider Countryside Butterfly Survey):
  - Reduced-effort, sampling wider countryside habitats (farmland, etc.), using two parallel 1-km transects in randomly selected 1-km squares; 2–4 visits per site, minimum 2 July/August visits, spring visits encouraged.

## Data Processing and Storage
- Field data recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker software.
- Data entry can be performed by the recorder or a regional transect coordinator.
- Regional coordinators compile data for all sites in their region; online data and Transect Walker files are uploaded to an Oracle database.
- For transect sites, a Generalized Additive Model (GAM) is used to impute missing values and calculate a site index.
- WCBS sites are excluded from site index calculations due to limited visits.

## Data Quality and Validation
- Automatic checks in Transect Walker flag potential data entry errors (e.g., unusually high counts, records outside known flight periods); recorders may revise or confirm entries.
- Regional coordinators review data for plausibility and consistency; ongoing validation throughout the season.
- Additional automated/manual validation targets out-of-range distributions (e.g., records outside known species ranges, unusual timing, first-time site records, extreme abundances).

## Data Formats and Metadata
- Site indices are stored as a text file with columns:
  - Species (scientific name, Fauna Europaea v2.2)
  - Common name
  - Year
  - Site Index (relative population size estimate)
- If a species was recorded at a site in a year but the monitoring did not meet criteria to calculate an index, the value is -2.
- Data reference standards:
  - Species nomenclature aligns with Fauna Europaea; common names follow Emmet & Heath.
  - Flight period and site-specific adjustments are embedded in the processing (e.g., time-of-year and site size adjustments).

## Limitations, Gaps, and Considerations for Data Leaders
- Site indices are relative and depend on detectability; some species are easier to observe than others.
- WCBS indices are not calculated due to insufficient visit counts, leading to gaps in wider-area representativeness.
- Data quality relies on consistent transect routes and weather constraints; deviations can affect comparability.
- Data are subject to imputation (GAM) for missing values, which has implications for interpretation and uncertainty.
- Data management practices include centralized storage (Oracle) and regional stewardship (transect coordinators) to maintain data quality and discoverability.

## Implications for Data Strategy and Community
- Emphasizes end-to-end data governance: standardized collection, centralized storage, rigorous validation, and transparent metadata.
- Supports cross-year comparability and collaboration through fixed transects and clearly defined data products (site indices).
- Highlights the importance of documenting data provenance, processing steps (GAM imputation), and quality checks to ensure trust and reuse.
- Indicates potential areas for enhancement in coverage and data completeness, particularly for WCBS and in ensuring consistent data collection amidst variable field conditions.