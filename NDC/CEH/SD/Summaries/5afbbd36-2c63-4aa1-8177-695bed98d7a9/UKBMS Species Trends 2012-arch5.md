# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK.
  - Data types include all-species transects, single-species transects, timed counts, and egg/larval web counts.
  - Transects are fixed routes designed to sample habitat types and management activities; consistency over years enables year-to-year comparisons.

- Data collection methods
  - All-species transects: fixed-route line transect; weekly recording under suitable weather; transects 2–4 km long, divided into habitat/management sections; typical 26 counts per year from April to September.
  - Weather and activity constraints: observations occur between 10:45 and 15:45 under defined weather (e.g., wind, temperature, sunshine conditions).
  - Data recording: field forms; entered into Transect Walker software; input by recorder or regional transect coordinators; data uploaded to an Oracle database.

- Data processing and analytics
  - Post-collection quality checks and validation precede analysis.
  - Statistical modeling:
    - General Additive Models (GAMs) to impute missing values and derive site indices.
    - A linear regression framework to estimate trends in collated indices across sites.
  - Outputs:
    - Collated Indices (log10-scaled, relative measures) for each species.
    - National annual indices derived from site data.
    - Species-specific trends over different timescales: all-time (1976–2012), last 20 years (1993–2012), and last 10 years (2003–2012).

- Data formats and storage
  - Stored species trend data are in CSV format with columns including:
    - Species, Common name, No.years, Series slope, Series Std.Err, Series P-value, Series trend, Series % change.
    - 20-yr, 10-yr slope, Std.Err, P-value, Trend, and % change fields.
  - Species names follow Fauna Europaea taxonomy; common names follow standard references.
  - Site indices are relative measures scaled so the series average equals 2; trends are the slope of the Collated Index.

- Data quality control and governance
  - In-field automated checks (Transect Walker) flag anomalies (e.g., unusually high counts, out-of-flight-period records); recorders may adjust or confirm.
  - Regional coordinators perform additional checks with local site knowledge.
  - Automated/manual validation screens for:
    - Records outside known distribution (cross-checked with BN M and existing UKBMS data),
    - Records outside normal flight periods,
    - First-time records at a site,
    - Extreme or atypical abundances.
  - Data provenance and update policy:
    - Collated Indices are updated annually as new monitoring data are incorporated.
    - Past year values may be revised as data are added, reflecting ongoing data assimilation.

- Practical implications for data governance (Data Stewards view)
  - Standardized data collection and recording processes enable comparability across years and sites.
  - Clear data lineage from field forms to Transect Walker to Oracle storage to published CSVs.
  - Metadata considerations include species taxonomy, common names, number of years analyzed, and clearly defined statistical metrics.
  - Data sharing and accessibility:
    - Transect Walker is freely available; data outputs and indices are published and downloadable (e.g., CSVs) via UKBMS resources.
  - Handling incomplete data:
    - Not all sites monitored every year; missing data are addressed via GAM-based imputation and a collated index approach, with explicit notes on the number of contributing years per species.