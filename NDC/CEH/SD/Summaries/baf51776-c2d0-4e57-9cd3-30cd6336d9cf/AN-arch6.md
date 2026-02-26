# AN Protocol ATMOSPHERIC CHEMISTRY - NITROGEN DIOXIDE Version 1.1 (previously AC Protocol, updated Jan 2001)

- Purpose and context
  - Aim to detect and define changes in periodic mean atmospheric NO2 concentrations.
  - NO2 is a key urban pollutant from NOx sources; health and ecosystem impacts noted.
  - Measurement uses passive diffusion tubes; method is well-researched, low-cost, requires replication due to tube-to-tube variation.
  - Consideration of extending to other gases (NH3, SO2, O3) is ongoing but no reliable passive methods available yet.

- Data collection design
  - Core measurement: atmospheric NO2 using diffusion tubes; three experimental tubes (E1, E2, E3) and three blank tubes (B1, B2, B3) per site.
  - Site metadata: Site Identification Code, Core Measurement Code, Location Code; unique sampling identifiers to accompany analytical results.
  - Sampling cadence: fortnightly data collection at each ECN site; two-week exposure periods per sampling event.
  - Location and mounting: tubes mounted in clips at 1.5 m above ground, on bulk precipitation collectors or standard posts; if a meteorological enclosure exists, place within it.
  - Blank controls: three blank tubes transported to site but not exposed.

- Field deployment and sampling protocol
  - Deployment: remove white cap immediately prior to placement; tubes oriented with open ends downward.
  - Retrieval: collect after two weeks; re-fit white caps prior to removal from post.
  - Handling and storage: transport blanks and exposed tubes to laboratory the same day; store samples refrigerated during the two-week period; analysis prepared on/before use.
  - Labeling: tubes labeled with ECN Measurement Code, Site ID, Location Code, tube code, and Sampling Date; the labeling reference must accompany results.

- Lab analysis workflow and calculations
  - Reagents and preparation: use sulphanilamide and N-1-Naphthylethylene-diamine dihydrochloride (NEDA) with fresh reagents prepared on analysis day.
  - Analytical procedure: absorbent inside diffusion tubes treated and developed to measure nitrite formed from NO2.
  - Measurement: colorimetric read at 542 nm; calculate nitrite mass from calibration curve; convert to NO2 concentration (ppb) using diffusion-tube parameters.
  - Safety: operator gloves required; tubes rinsed after analysis to prevent cross-contamination.

- Data capture, formats, and transfer
  - Core data variables (fortnightly per site): site code, core measurement code, location code, setting out date/time, sampling date/time, tube code, and NO2 weight (µg).
  - Time and date recording: sampling date/time with GMT 24-h clock; precise to 1 minute for setting out; sample time precision specified.
  - Data standards: datasets must include a unique reference for ECN database transfer; follow ECNCCU data transfer documentation and restricted-access Site Managers’ extranet for dataset formats.
  - Data types and units: NO2 concentration in ppb derived from tube exposure; mass in µg; time stamps in GMT.

- Data quality assurance and controls
  - Replication and blanks to account for variability and contamination.
  - Fresh standards prepared daily; calibration against known NO2 standards (Stocks A and B) with defined working standards.
  - Handling protocols to prevent contamination (gloves, clean labware, immediate rinsing of tubes after analysis).
  - Documentation and field forms: standard field recording form available; appendix includes detailed equipment and procedural notes.

- Outputs, usability, and data products
  - Outputs enable self-serve exploration: time series of NO2 by site and location, comparison between exposed and blank tubes, and summary dashboards.
  - Potential integration with meteorological data and other ECN measurements for broader analyses (e.g., trends, seasonal patterns, source attribution).
  - Formal data transfer and documentation ensure reproducibility and re-use across teams and publications.

- Appendices and equipment
  - Appendix I: analytical procedure details, reagents, stock preparations, and measurement steps.
  - Appendix II: equipment details (diffusion tubes, disks, caps, and supplier information).
  - Figure references describe tube setup and field placement.

- Practical notes for data support
  - The data model requires linking sample metadata (site, location, setting out) with analytic results (NO2 mass, calculated concentration) within the ECN database.
  - Documentation emphasizes standardization of naming, coding (E1–E3, B1–B3), and timing to facilitate cross-site comparisons.
  - While extension to additional pollutants is considered, current data scopes focus on NO2 with validated passive methods.