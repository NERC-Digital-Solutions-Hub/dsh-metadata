# UK Butterfly Monitoring Scheme

- Overview: The UKBMS is a long-running, volunteer-based program that tracks butterfly population status across the UK since 1976. It is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.

- Data collection components:
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects walked weekly (up to 26 visits/year) with a 5 m wide recording band; ~2000 sites sampled annually.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits/year.
  - Targeted surveys: single-species transects and alternative methods (e.g., timed counts, egg/larval web counts).

- Nature of data and trend analysis:
  - Data are used to create abundance indices (relative measures) rather than absolute counts.
  - Indices are combined into species-wide collated indices using the Generalised Abundance Index (GAI) with weighting by the proportion of the flight period observed each year per site.
  - All sampling methods contribute to seasonal pattern estimation and extrapolation to account for recording gaps.

- Data quality control:
  - Field data are recorded on standard forms and entered online via the UKBMS data entry site or Transect Walker.
  - Automated checks flag potential errors; regional transect coordinators validate data throughout the season.
  - Additional automated/manual validation screens for: out-of-range distributions, flights outside known periods, first-time site records, and unusual abundances. Corrections are made through queries in collaboration with coordinators or recorders.

- Details of this data download:
  - Provides long- and short-term trends in collated indices for all species with sufficient data.
  - Format: CSV (.csv) with columns including:
    - COMMON_NAME, SCI_NAME, NYEARS
    - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDETAIL, F_FULL_R
    - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
    - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
  - Start years for some species may be later due to data sufficiency.

- licence and attribution:
  - Open Government Licence (OGL) for use and reuse with few conditions.
  - Must include full citation with DOI in publications describing research using the data.
  - Attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right from Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact details:
  - UKBMS Partners offer guidance on data interpretation and are open to co-authorship and input for publications, conferences, or posters.
  - Contacts:
    - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
    - Butterfly Conservation: Transect coordinator (transect@butterfly-conservation.org)

- GIS-focused notes for map-based use:
  - Spatial coverage includes site-level Pollard transects and 1 km WCBS squares, enabling map-based visualization of spatial distribution and trends.
  - Data are suitable for publishing habitat- or policy-relevant maps showing species trends over time, with annual and multi-year summaries.
  - Indices are relative; appropriate for identifying spatial hotspots, monitoring changes, and informing biodiversity status assessments.