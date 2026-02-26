# The UK Butterfly Monitoring Scheme (UKBMS)

- The UKBMS collects butterfly data from over 2,000 sites across the UK annually, using standardized methods to enable year-to-year comparison and trend analysis.
- Data types include all-species transects, single-species transects (fewer weeks), timed counts, egg/larval web counts, and the Wider Countryside Butterfly Survey (WCBS).

## Data collection and sampling methods

- All-species transects: fixed-route line transects (2–4 km) walked weekly from April to September under specific weather conditions; 5 m wide belt counts entirely along the transect; transects fixed to ensure comparability across years.
- Transect timing and conditions: observations typically between 10:45 and 15:45, with weather thresholds (e.g., dry, Beaufort <5, temperature thresholds depending on sunshine).
- WCBS: reduced-effort sampling for wider countryside habitats, based on two parallel 1-km transects per randomly selected 1-km square; 2–4 visits per site per year.
- Data collection tools: standard field recording forms; online data entry via the UKBMS site or Transect Walker software; data uploaded into a central Oracle database.
- Data responsibility: each transect has a regional coordinator who collects and validates data for their region.

## Data processing and indices

- Site indices: calculated only for sites with sufficient monitoring visits; for timed observations, larval/egg counts, and similar, counts are timed to peak flight period. WCBS sites are excluded from index calculation due to insufficient visits.
- Modeling approach: a General Additive Model (GAM) is used to impute missing values and compute site indices for transect sites.
- Relative measure: site indices are a relative estimate of population size (not absolute counts) and correlate with more intensive measures like mark–release–recapture, though the proportion seen varies by species.

## Quality assurance and validation

- In-field automated checks (Transect Walker) flag potential data entry errors (e.g., abnormally high counts, records outside flight period).
- Regional coordinators review records for questionable values; continuous validation throughout the season.
- Additional automated and manual validation steps check for:
  - Records outside known distribution ranges
  - Records outside normal flight periods
  - First-time records at a site
  - Abundance anomalies or extreme values compared with typical site norms

## Data storage, formats and metadata

- Data storage: all records are stored in an Oracle database.
- Site indices are stored as text files with columns including Species, Common name, Year, and Site Index.
- Data flags: a value of -2 indicates that a site could not produce an accurate site index due to insufficient monitoring data for that year.
- Taxonomic and common-name references: scientific names follow Fauna Europaea; common names follow established references.

## Data governance, access and dissemination

- Data flow emphasizes centralized data management with regional oversight to ensure quality and consistency.
- Outputs are disseminated through reports, charts, and dashboards, enabling monitoring of trends over time and across sites.
- While data sharing in other contexts can be a barrier, UKBMS maintains centralized storage and standardized formats to support transparency and comparability.

## Key considerations for monitoring framework authors

- Longitudinal comparability: fixed transect routes and consistent sampling windows to enable year-to-year trend analysis.
- Standardization and metadata: clear definitions of methods, data formats, and validation procedures; explicit handling of missing data via GAM imputation.
- Data quality controls: layered validation—from in-field checks to regional reviews and automated procedures.
- Data accessibility and governance: centralized repositories, regionally managed data, and standardized outputs to support policy scrutiny and decision-making.
- Handling data gaps: explicit exclusions (e.g., WCBS for index calculation) and explicit flags for insufficient data to maintain the integrity of indices.