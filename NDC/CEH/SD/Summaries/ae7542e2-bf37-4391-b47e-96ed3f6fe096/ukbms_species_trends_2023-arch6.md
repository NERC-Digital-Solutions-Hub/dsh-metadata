# UK Butterfly Monitoring Scheme data download

- Purpose and scope
  - Provides annual data on butterfly population status in the UK, derived from a wide-scale, site-based monitoring program.
  - Used to understand biodiversity trends and inform policy questions; in operation since 1976 with over 3000 active sites each year.
  - Data come from three sampling frameworks: standard butterfly transects (Pollard walks), Wider Countryside Butterfly Survey (WCBS), and targeted surveys (including single-species transects and alternative methods).

- How data are collected
  - Standard transects (Pollard walks): fixed-route 2–4 km, 5 m wide recording all species weekly (ideally 26 counts/year) across habitat units, weather permitting.
  - WCBS: stratified-random 1 km squares with two parallel 1-km transects, 2–3 visits per year, sampling common habitats like farmland.
  - Targeted surveys: single-species transects or alternative methods (timed counts, egg/larval web counts) focusing on specific species during key periods.

- Nature of the data and analysis
  - Data are abundance indices (relative measures) rather than absolute population counts.
  - Indices are combined across sites using the Generalised Abundance Index (GAI) with site- and year-weighting to reflect survey effort and flight periods.
  - All counts from Pollard walks, reduced surveys, and WCBS are used to estimate seasonal patterns and extrapolate gaps, prioritising observed data over extrapolated data.

- Quality control and validation
  - Field data recorded on standard forms; entered online or via Transect Walker, with automatic error checks (e.g., unusual counts, out-of-season records).
  - Regional transect coordinators validate data; ongoing checks throughout the season.
  - Additional automated and manual validation steps to flag records outside known distributions, unusual abundances, or first-time site records; corrections made as needed.

- Details of the data download
  - Contains long- and short-term trends in collated indices for species with sufficient data; delivered as a CSV file.
  - Time range: long-term trends from 1976 to 2023; some species start later due to data sufficiency.
  - Key columns include:
    - COMMON_NAME, SCI_NAME, NYEARS
    - F_LIN_B, F_LIN_SE, F_LIN_P, F_TRENDDETAIL, F_FULL_R
    - T20_LIN_B, T20_LIN_SE, T20_LIN_P, T20_TRENDDETAIL, T20_20_R
    - T10_LIN_B, T10_LIN_SE, T10_LIN_P, T10_TRENDDETAIL, T10_10_R
  - Descriptions specify how trends are calculated (slopes, p-values) and how trend meanings are assigned (rapid decline/increase, stable).

- Usage rights and attribution
  - Available under the Open Government Licence (OGL); allows free use with few conditions.
  - Must include citation details (DOI) in any publications using the data.
  - Attribution statement to include with outputs: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC.

- Collaboration and contact
  - UKBMS partners offer advisory support and interpretation help; opportunities for co-authorship or intellectual input in publications resulting from UKBMS data.
  - Contact points:
    - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
    - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)

- Practical notes for data support specialists
  - Outputs are designed for self-service exploration (dashboards, pivot-style reports) and can be extended with new analyses.
  - The dataset supports trend analysis across multiple timeframes (all years, last 20, and last 10 years) and across multiple species.
  - Be mindful of data limitations: indices are relative, detection probability varies by species, and data patchiness may affect some species more than others.
  - Useful for cross-dataset integration (e.g., policy data, biodiversity indicators) given standardized formatting and clear licensing.