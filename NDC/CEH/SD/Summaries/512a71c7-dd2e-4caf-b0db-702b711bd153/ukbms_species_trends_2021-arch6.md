# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, relying on volunteer data from over 2,500 sites annually.
- Purpose and scope: to provide annual data on butterfly population status across the UK for understanding biodiversity trends and informing policy; data collection has operated since 1976.
- Sampling components:
  - Standard butterfly transects (Pollard walks): fixed-route counts 2–4 km long, weekly counts (up to 26 per year) across ~2,000 sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified random 1 km squares with two parallel transects (2–3 visits per year) across ~800 squares.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species.
- Data integration: counts from all sampling methods are combined to produce site indices, which are then aggregated into species-level collated indices using a Generalised Abundance Index (GAI) with weighting that accounts for the proportion of the flight period surveyed each year.
- Data use: the indices are relative measures of population size and are used to assess trends and inform conservation and policy decisions.

## Nature of data collected and trend analysis

- Data are used to create abundance indices (relative population size) from counts across sites and methods.
- Trend computation:
  - Long-term trends use data from 1976 onward (where sufficient data exist).
  - Collated indices are produced by applying the GAI method with site-year weighting.
  - Seasonal pattern estimation and extrapolation account for sampling gaps; observed data have greater influence than extrapolated data.
- Output focuses on trends and changes in abundance for each species, including:
  - Long-term slope (per year), standard error, and p-value.
  - Descriptions of overall trend (rapid decline, rapid increase, stable) based on slope and significance.
  - Percent change over the full series and over latest 10 and 20-year windows (with slopes, SEs, p-values, and trend descriptions).

## Quality control

- Field data are collected on standard forms and entered into the UKBMS system or Transect Walker software before upload.
- Automated checks flag anomalies (e.g., abnormally high counts, records outside flight periods); regional transect coordinators perform ongoing validation.
- Data undergo multiple validation steps, including checks against known distributions and flight periods, first-record at sites, and comparisons to typical site patterns.
- Where issues are found, edits are made through queries and coordinated validation with coordinators or recorders.

## Details of this data download

- Provides long- and short-term trends in collated indices for species with sufficient data, exported as a CSV file.
- Time span: from 1976 to the year indicated in the filename (start year may vary by species due to data availability).
- Key columns (examples):
  - COMMON_NAME, SCI_NAME
  - NYEARS (years included in the series)
  - F_LIN_B, F_LIN_SE, F_LIN_P (linear trend per year, SE, P-value)
  - F_TRENDETAIL (text description of overall trend)
  - F_FULL_R (percentage change over the full series)
  - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R (20-year trend metrics)
  - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R (10-year trend metrics)
- Outputs allow users to assess species-specific trends and recent changes across multiple timeframes.

## Licence and attribution statement

- The dataset is provided under the Open Government Licence (OGL), allowing free use with few conditions.
- Publications or reports using the data must include the specified citation (with DOI) as given in the metadata.
- Attribution statement to be included with any derived information or images: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer assistance in interpreting outputs and are open to collaboration.
- Potential co-authorship and input for scientific publications, conference presentations, or posters resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)