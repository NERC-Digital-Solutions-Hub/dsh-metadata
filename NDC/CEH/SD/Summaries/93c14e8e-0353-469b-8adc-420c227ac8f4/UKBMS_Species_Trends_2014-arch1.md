# UK Butterfly Monitoring Scheme (UKBMS) Methods

- The UKBMS collects data from over 2,000 sites annually across the UK, using standardized transect-based methods to estimate butterfly abundance and trends.
- Multiple survey types are used to cover different habitat contexts: all-species transects, single-species transects, timed counts/egg-larval web counts, and the Wider Countryside Butterfly Survey (WCBS).

## Experimental design and sampling regime
- All-species transects (Pollard walks) involve fixed-route line transects at each site, typically 2–4 km long, with 26 weekly counts from early April to end September in suitable weather.
- Transects are fixed to enable year-to-year comparisons and are divided into habitat/management sections.
- Weekly transect conditions: 10:45–15:45, dry weather, wind < Beaufort 5, temperature thresholds (≥13°C with sunshine or >17°C if overcast).
- Single-species transects follow the same methodology but are recorded only during focal species’ flight periods.
- Timed counts record a focal species over a set time/area; egg/larval webs counts record eggs or larval webs in suitable habitat.
- WCBS (established in 2009) uses two parallel 1-km transects within randomly selected 1-km squares, with 2–4 visits (minimum two in July/August; spring visits encouraged) to sample wider countryside habitats more efficiently.

## Data collection and entry
- Data are recorded on standard forms in the field.
- Online entry via the UKBMS data portal (MyData) or via Transect Walker software.
- Real-time or end-of-season uploading to an Oracle database.
- Data flow: field recorder or regional transect coordinator collect data; regional coordinators validate and compile data for their region; data are stored centrally.

## Analytical methods and indices
- Two national index approaches, depending on species group:
  - Wider countryside species: two-stage model using all counts across survey types.
    - Stage 1: generalized additive model estimates the annual seasonal flight pattern per species.
    - Stage 2: uses full annual counts with seasonal values as an offset to estimate annual changes in abundance.
    - Details described in Dennis et al. (2013).
  - Habitat specialists and regular migrants: GAM-based imputation for missing values to produce a site index; then a log-linear regression is applied to derive a Collated Index (LCI) across monitored sites.
- Collated Indices are updated annually as new data are incorporated; not all years are available for all species.
- A linear regression is then applied to the Collated Indices to produce simple trends for:
  - Whole time series (1976–2013),
  - Last 20 years (1993–2013),
  - Last 10 years (2003–2013).
- Species groups:
  - Wider countryside species: mobile, occur across broad habitats.
  - Habitat specialists: low mobility, restricted to semi-natural habitats.
  - Regular migrants: overwinter outside the UK, but arrive seasonally.
- Values are presented as relative measures; site indices relate to population size but are not absolute counts.

## Nature and units of recorded values
- Site indices are relative population size measures, proportional to actual abundance.
- Collated Indices are presented as log10 Collated Index (LCI), normalized so the average index over the series equals 2 for each species.
- Trends are the slope of the Collated Index over the specified time periods.
- Additional fields include: annual % change, 10- and 20-year slopes, standard errors, and p-values, plus narrative trend details (e.g., rapid decline, rapid increase, stable).

## Quality control and validation
- In-field automated checks (Transect Walker) flag anomalous counts or records outside known flight periods; recorders may adjust or confirm.
- Regional transect coordinators review records for their regions; online data are subject to ongoing validation.
- Post-entry validation includes checks for out-of-range distributions, records outside normal flight periods, first-time site records, extreme abundances, and discrepancies relative to normal site-level patterns.
- Validation steps rely on existing distribution data and reference datasets (e.g., BNMs) to ensure records align with known ranges.

## Data storage format and key fields
- Species Trends are stored as CSV files with columns including:
  - SCI_NAME (scientific name), COMMON_NAME, NYEARS (years used for series), F_LIN_B (linear slope), F_LIN_SE (standard error), F_LIN_P (p-value), F_TRENDDETAIL (text trend description), F_FULL_R (percentage change over the series),
  - T20_LIN_B / SE / P / TRENDDETAIL / R (20-year metrics),
  - T10_LIN_B / SE / P / TRENDDETAIL / R (10-year metrics).
- Additional fields cover descriptive trend details and multiple time-scale metrics to support interpretation and reporting.

## References and methodological notes
- Key methodological references underpinning the analytical approaches include:
  - Dennis et al. 2013 (two-stage index method for wider countryside species),
  - Moss & Pollard 1993; Pollard & Yates 1993 (early index calculation and monitoring framework),
  - Rothery & Roy 2001 (application of GAMs to transect data).