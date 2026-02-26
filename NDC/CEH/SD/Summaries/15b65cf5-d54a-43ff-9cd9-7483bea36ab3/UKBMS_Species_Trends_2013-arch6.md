# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites per year across the UK.
  - Data collection includes all-species transects (fixed routes), single-species transects, timed counts, and egg/larval web counts.
  - Transects are fixed to enable year-to-year comparison, typically 2–4 km long and divided into habitat/management sections.
  - Data collection occurs weekly from April to September under suitable weather; counts are conducted within defined weather and time windows.

- Data collection methods
  - Field data are recorded on standard forms.
  - Data are entered into the Transect Walker software; recorded directly by the recorder or by a regional transect coordinator.
  - Transect Walker files are uploaded to an Oracle database.

- Analytical methods
  - After validation, missing values are imputed using General Additive Models (GAM) to create site indices.
  - Site indices are combined to form a national annual index for each species (Collated Index) via a log-linear model to handle incomplete annual monitoring.
  - Indices are updated annually as new data are received; past values may be revised.
  - Species trends are derived by linear regression on the Collated Indices:
    - Across the full series (1976–2013)
    - Over the last 20 years (1993–2013)
    - Over the last 10 years (2003–2013)

- Nature and units of recorded values
  - Site indices are relative measures of population size, not absolute counts.
  - Collated Indices are presented as Log10 of the Collated Index (LCI), scaled so the series average is 2.
  - Trends are reported as the slope of the Collated Index per year; interpretations include rapid decline, rapid increase, or stable depending on slope and p-value.

- Quality control
  - Automatic checks in Transect Walker flag unusual counts or out-of-season records.
  - Regional coordinators review data for questionable records.
  - Additional automated and manual validation checks ensure consistency with known distribution ranges, flight periods, and site history.

- Format of stored data
  - Data stored as a CSV with per-species entries, including:
    - Scientific and common names, number of years in the series, series slope, standard error, p-value, and trend description for the full series.
    - Percentage change over the full series.
    - 20-year and 10-year slope, standard error, p-value, trend descriptions, and percentage changes.
  - Columns reflect: species taxonomy, years contributing, slopes, uncertainties, statistical significance, and descriptive trend labels (e.g., rapid decline, stable).

- Temporal coverage and data usability
  - The dataset covers long-term trends since 1976, with recent years providing shorter, more precise insights.
  - Some species have incomplete early-year data, resulting in shorter trend series or updated historical values as more data are incorporated.
  - The structured data format enables end-user analysis and monitoring of butterfly population changes over time.