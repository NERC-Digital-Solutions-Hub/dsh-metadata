# About the UK Butterfly Monitoring Scheme

- Purpose and governance
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It relies on volunteer contributions and provides annual data on butterfly population status to understand biodiversity trends and inform policy.

- Sampling framework and data scope
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 45 minutes to 2 hours, 5 m wide, weekly counts (up to 26 per year) from April to September; over 2000 sites monitored annually by 2022.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (minimum 2 visits in July/August); around 800 squares sampled per year.
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) focused on specific species or flight periods.
  - Data integration: all sampling methods contribute to a unified UKBMS dataset analyzed collectively.

- Nature of data and trend analysis
  - Data are abundance indices (relative measures) rather than absolute population counts; indices reflect a consistent proportion of butterflies present, varying by species.
  - National species indices are produced using the Generalised Abundance Index (GAI) with a weighting adjustment so site-year data are weighted by the proportion of the species flight period surveyed.
  - Seasonal patterns across counts are modeled to account for gaps in recording and to extrapolate counts.

- Quality control and data integrity
  - Field data are recorded on standard forms and entered online via the UKBMS system or Transect Walker; uploaded to a central database.
  - Automatic checks flag potential errors (e.g., unusually high counts, records outside known flight periods); regional transect coordinators perform ongoing validation.
  - Additional automated/manual validation checks screen for out-of-range distributions, out-of-season records, new-site records, and anomalous abundances; corrections are made through queries and coordination when needed.

- Data download details
  - The download provides long- and short-term trends in collated indices for all species with sufficient data; provided as CSV (.csv).
  - Long-term trends cover 1976–2022 (start year may be later for some species due to data limitations).
  - Key columns include:
    - COMMON_NAME, SCI_NAME, NYEARS
    - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL
    - F_FULL_R (percent change over the series)
    - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
    - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
  - Documentation notes that start years may vary due to data availability; trends are based on collated counts across survey methods.

- Licence and attribution
  - Data are provided under the Open Government Licence (OGL) with freedom to use and reuse, subject to licence conditions.
  - Any reports or publications referencing the data must include the citation (including DOI) from the metadata record.
  - Attribution statement required: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact details
  - UKBMS Partners offer assistance with dataset details and interpretation of outputs.
  - Opportunities for co-authorship and intellectual input in publications resulting from UKBMS data.
  - Contact information:
    - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
    - Butterfly Conservation, Transect coordinator: transect@butterfly-conservation.org

- Practical considerations for data users (Data Support focus)
  - Outputs are typically relative indices rather than absolute abundances; consider detection variability across species.
  - Weighting and modeling (GAI) are used to create robust annual indices across sites with differing survey effort.
  - Data quality processes are rigorous, with multiple validation layers to ensure reliability for policy questions and biodiversity trend analysis.