# Experimental Design/Sampling Regime

- Aim
  - Investigate effects of land use change (development of irrigation schemes in pastoral rangelands) on access to selected ecosystem services, focusing on Rift Valley fever (RVF) as a case study.
  - Use households as primary sampling units; compare across land-use types (irrigated vs non-irrigated) with 220 households per type.

- Study Area and Sampling Design
  - Locations: Bura and Hola irrigation schemes in Tana River County; villages bordering these schemes; areas in Ijara and Sangailu divisions, Garissa County (transhumance/pastoralism).
  - Design: cross-sectional survey conducted alongside existing RVF surveys; sampling frame created from household lists and irrigation-scheme registers; households randomly selected, as are animals within households.
  - Sample size: determined by formal power calculation for comparing two independent proportions; 220 households per land-use type.

- Field Data Collection (Two Steps)
  - Step 1: Household data
    - Collect household ID, geographic coordinates (decimal degrees), altitude, and numbers of animals by species.
  - Step 2: Animal data
    - Identify animals by household, record animal ID, species, age, and sex.
    - Collect up to 20 ml venous blood per animal (jugular vein); split into whole blood (heparinised) and serum (non-heparinised).

- Sample Processing and Storage
  - Serum separated after clotting and centrifugation; aliquoted into 2 ml cryo tubes in duplicates for working and long-term storage.
  - Samples preserved and transported on dry ice; transferred to liquid nitrogen tanks upon arrival at the Nairobi laboratory.

- Analytical Methods
  - Serological testing: RVF virus immunoglobulin G (IgG) via an RVF inhibition ELISA validated for humans, domestic and wild ruminants.
  - Reference: Paweska et al., 2005; protocol fully described in the cited publication.

- Dataset and Data Management
  - Data file: DDDAC_Kenya_livestock_rvfdata.csv (18 variables described in Table 1).
  - Data collection tools: Open Data Kit (ODK) on smartphones; barcoded sampling tubes linked to household and animal data.
  - Data storage: daily uploads to a central ODK Aggregate server (ILRI) and subsequent biorepository storage.

- Quality Control
  - Field team: minimum of 2 researchers and 3 technicians; one researcher oversees animal-level data capture; peers correct observations.
  - Sampling logistics: pre-labeled tubes; barcodes scanned with smartphone cameras to link samples to data; dry ice replenished weekly.
  - Laboratory QA: analyses conducted in duplicates; borderline results re-tested.

- Variables in Dataset (Table 1)
  - hhid: Household identification number
  - animalid: Animal identification number
  - altitude: GPS-derived altitude (meters)
  - goats, sheep, cattle, donkeys: counts per household
  - species: Species of sampled animal
  - breed: Breed of animal (not reliably recorded)
  - sex: Sex of animal
  - age: Age category (Adult, Weaner, Kid/Lamb/Calf)
  - bdt: Bar code for parent whole-blood sample
  - bsr: Bar code for parent serum sample
  - avaq: Bar code for working serum aliquot
  - area: Sampling location
  - pathogen: Pathogen screened for (RVF serology)
  - landuse: Land-use category (irrigated vs non-irrigated)
  - result: Serological test result

- Data Quality and Gaps
  - Missing values primarily due to non-disclosure by owners; some blank cells indicate not recorded or collected.

- Link to Environmental Monitoring Objectives
  - Demonstrates standardized, verified data collection and QA processes.
  - Produces clear outputs (datasets, serology results) suitable for integration with other environmental data.
  - Data management supports storage, accessibility, and potential sharing via appropriate portals and repositories.