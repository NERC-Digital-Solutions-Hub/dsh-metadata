# Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

## Data Access and Citation
- Data are available under the Open Government Licence.
- Access: https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d
- Reuse citation: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

## Study Background
- Investigates adaptive phenotypic plasticity: ability of individuals to modify phenotype in response to environment.
- Aims to test how plasticity influences host–pathogen interactions and potential evolutionary dynamics.
- Uses a unique repository of a songbird pathogen (M. gallisepticum) collected during an epizootic, observing changes as host resistance evolves.

## Study Design and Methods
- Ethics and approvals: Protocols approved by IACUCs at Auburn University and Arizona State University; additional Institutional Biological Use Authorizations and Exeter ethics approval.
- Subjects and origin:
  - Wild house finches (N = 171): 93 males, 78 females.
  - Captured in Arizona and Alabama; birds housed in aviaries at Arizona State University and Auburn University.
  - Preliminary infection status confirmed as negative for M. gallisepticum via SPA assay and endpoint PCR.
- Inoculation and isolates:
  - 53 birds from Alabama and 59 birds from Arizona inoculated with 1 of 56 M. gallisepticum isolates (spanning 1994–2015).
  - Inoculation method: 20 µL culture containing 1 × 10^4 to 1 × 10^6 color-changing units/mL, applied to both eyes.
  - Isolates prepared from naturally infected birds; stocks stored at -80°C; inoculum prepared in SP4 medium.
  - Post-inoculation housing involved pairings of inoculated birds with non-inoculated partners.
- Health and quarantine:
  - Some Alabama-origin birds were initially positive and released; remaining birds underwent a 30-day quarantine before transfer to Arizona.
  - All birds screened for other diseases; management included treatment for Trichomonas gallinae and Coccidia spp as a precaution.
- Phenotypic and pathogen measurements:
  - Eye lesion scoring: eye health scored 0–5 per eye on days 3, 6, 8, 14, 21, 25, 28, and 34 post-inoculation; scorers were blinded to treatment.
  - Body mass: measured at -7, 0, 3, 8, 14, 21, 28, and 34 days post-inoculation.
  - Pathogen clearance and load:
    - PCR-based detection of M. gallisepticum DNA from conjunctival/tracheal swabs at days 8, 14, 21, 28.
    - Quantitative PCR (qPCR) used to determine pathogen load (MGload) on corresponding days.
  - Non-infected controls: swabs collected and tested to monitor background detection up to day 35.
- Laboratory protocols:
  - DNA extraction and PCR conditions standardized; primers and probes designed for M. gallisepticum detection; cycling conditions specified for reproducibility.

## Data Structure and Variables
- ID: Unique bird identifier; Sex: f or m; Pop: origin population (AO = Auburn/Opelika; GT = Greater Tempe).
- Pathogen: Year of pathogen sampling.
- Mass measurements (grams): Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34.
- Eye scores (0–5): RE_score and LE_score across days (e.g., d3, d6, d8, d13, d14, d21, d25, d28, d34).
- MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28: Presence (0 = no, 1 = yes) of M. gallisepticum DNA in swabs at specified days.
- Pload_8, Pload_14, Pload_21, Pload_28: Pathogen load (cell copies) on corresponding days.
- PCR_2t, PCR_3t, ..., PCR_35t: PCR detection results for non-infected birds across days 2–35 (0 = no, 1 = yes).
- Data types and units are defined per variable (numbers for measurements, text for categorical fields); missing measurements are indicated where applicable.

## Data Quality and Handling
- Clear documentation of measurement days and methods to support replication.
- Data include both infected and non-infected birds with longitudinal time points.
- Some measurements may be missing (N/A) or not collected on certain days; table-style data structure notes missing or unsuccessful assays.

## Potential Uses for Data Leaders
- Analyze time-series of phenotypic responses (eye lesion progression, body mass changes) in relation to pathogen isolates across years.
- Examine how phenotypic plasticity mediates infection dynamics and host resistance evolution.
- Integrate pathogen isolate history with host response to explore linkages between pathogen variation and host outcomes.
- Support cross-institution data collaboration by providing detailed metadata, protocols, and measurement schedules.
- Inform data governance practices by exemplifying licensing (Open Government Licence), citation requirements, and data provenance.

## Ethics, Licensing, and Citation
- Data collected under approved animal care and use protocols with explicit ethics oversight.
- Data licensed for open reuse under the Open Government Licence; requires appropriate citation as specified above.