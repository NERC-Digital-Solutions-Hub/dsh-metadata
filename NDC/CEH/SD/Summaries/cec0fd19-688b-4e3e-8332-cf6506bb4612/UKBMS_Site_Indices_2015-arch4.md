# The UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS collects data from over 2,000 sites annually across the UK, using multiple standardized data collection methods.
- Primary method: fixed-route Pollard walks (all-species transects) plus Wider Countryside Butterfly Survey (WCBS) as a reduced-effort alternative.
- Additional measures include timed counts and egg/larval web counts for certain species.

## Data collection methods
- All-species transects: fixed routes sampled weekly during April–September under suitable weather; routes chosen to reflect habitat variation and management; 2–4 km long, divided into habitat units; counts occur in a 5 m wide belt, yielding ideally 26 counts/year.
- Transect timing and conditions: walks between 10:45 and 15:45; weather criteria include dry conditions, wind below Beaufort 5, and temperature thresholds (≥13°C with sun or ≥17°C if overcast).
- Single-species transects: follow all-species methodology but recorded only during specific weeks for focal species.
- Timed counts and egg/larval web counts: species-specific counts over set periods or areas, aligned with flight periods.
- WCBS: established in 2009 to sample wider countryside habitats; uses two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits per site (minimum two in July/August; spring visits encouraged).

## Data capture and storage
- Field data recorded on standard forms; entered online via the UKBMS data entry site or via Transect Walker software.
- Data submission: transect coordinators compile regional data; online data and Transect Walker files are uploaded to an Oracle database holding all records.

## Data processing and indices
- Site indices: calculated only at sites with adequate monitoring; for timed/egg/larval counts, indices are based on peak flight period data adjusted for time of year and site area.
- WCBS indices: excluded due to insufficient visits for reliable population indices.
- Imputation and modeling: for transect sites, a General Additive Model (GAM) is used to impute missing values and calculate site indices.

## Quality control
- In-field checks: Transect Walker automatically flags potential data entry errors (e.g., unusually high counts or records outside flight periods); recorders may revise entries.
- Regional validation: regional transect coordinators review records and perform ongoing checks.
- Post-entry validation: automated and manual procedures detect records outside distribution ranges, outside flight periods, first-time site records, extreme or atypical values.

## Data format and metadata
- Site indices are stored in a text file (.txt) with columns:
  - Species (scientific name per Fauna Europaea)
  - Common name (per Emmet and Heath)
  - Year
  - Site Index (relative measure; proportional to actual population size)
- If a species was recorded at a site in a year but insufficient data exist to compute a reliable index, the value is recorded as -2.

## Data governance and accessibility (implications for Data Leaders)
- Centralized data platform: online entry, specialized software (Transect Walker), and a central Oracle database ensure standardization, discoverability, and updates.
- Clear documentation and metadata: taxonomy, naming conventions, and index definitions are explicitly defined, supporting reproducibility.
- Integrated quality framework: automated and manual QC processes at multiple stages maintain data integrity and reliability for analysis and dissemination.
- Longitudinal design: fixed transects and standardized procedures enable year-to-year comparisons and robust trend analysis across a large network of sites.