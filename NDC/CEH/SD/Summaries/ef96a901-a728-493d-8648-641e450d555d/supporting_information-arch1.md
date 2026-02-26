# Supporting information for: Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

## Aim and context
- Investigates adaptive phenotypic plasticity in the context of pathogen infection.
- Explores whether a pathogen (M. gallisepticum) can plastically alter replication and transmission in response to host defenses.
- Uses a unique collection of pathogen isolates from an epizootic to test relationships between plasticity and evolution.

## Data access and citation
- Data available under the Open Government Licence.
- Access and dataset: https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d
- For reuse, cite: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

## Project and authors
- NERC project: Evolution of phenotypic plasticity in an emerging pathogen
- Grant: NE/M00256X/1
- Principal investigator: Dr Camille Bonneaud
- Co-investigator: Prof Alastair Wilson

## Ethics and approvals
- Protocols approved by Institutional Animal Care and Use Committees (IACUC) at Auburn University (PRN 2015-2721) and Arizona State University (15-1438R).
- Additional approvals: Institutional Biological Use Authorizations (Auburn University BUA 500) and the University of Exeter ethics committee.

## Study design and sampling
- Subjects: Wild house finches (N=171; 93 males, 78 females).
- Origin: Captured in Arizona (AZ) and Alabama (AL).
- Pre-screening: All birds tested to confirm lack of prior M. gallisepticum infection (SPA antibody test and endpoint PCR on choanal swabs).
- Post-screening status: AZ birds negative; AL birds negative or positive were handled as described; AL positives released, remaining AL birds (N=53; 24M, 29F) quarantined for 30 days before transfer to ASU.
- Inoculation: 53 AL and 59 AZ birds randomly inoculated with one of 56 Mycoplasma gallisepticum isolates collected during the epidemic (1994–2015).
- Isolates: Obtained from naturally infected birds, grown in SP4 medium, stocks stored at -80 °C with glycerol; inoculum prepared from fresh culture for each bird.
- Housing: Arizona birds housed in pairs with one inoculated bird.

## Experimental procedures
- Inoculation method: 20 μL of culture containing 1 × 10^4 to 1 × 10^6 color-changing units/mL entrained in both eyes.
- Clinical monitoring: Eye lesion severity scored (0–5) in each eye at days post-inoculation (t) of 3, 6, 8, 14, 21, 25, 28, 34.
- Morphometrics: Body mass measured at -7, 0, 3, 8, 14, 21, 28, 34 days post-infection.
- Pathogen detection and load: Conjunctival and tracheal swabs collected at 8, 14, 21, 28 days; DNA amplified to assess presence/absence and load.
- Assays: qPCR performed with specific primers and fluorescent probes targeting M. gallisepticum DNA; cycling conditions detailed in the methods.
- Endpoint: Experiment terminated at 35 days post-inoculation with euthanasia of all birds.

## Measurements and data collection
- Phenotypic data per bird include:
  - Unique ID; Sex (f/m); Population of origin (Pop: AO/Auburn; GT/Greater Tempe).
  - Pathogen sampling year (Pathogen).
  - Body mass: Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34 (in grams).
  - Eye symptom scores by day for right and left eyes (RE_score and LE_score) at multiple days (d3, d6, d8, d13, d14, d21, d25, d28, d34).
  - Pathogen detection and load: MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (PCR 0/1 presence/absence on conjunctival/tracheal swabs).
  - Pathogen load: Pload_8, Pload_14, Pload_21, Pload_28 (cell copies).
  - Non-infected bird PCR timetable: PCR_2t, PCR_3t, PCR_4t, PCR_5t, PCR_6t, PCR_7t, PCR_8t, PCR_11t, PCR_14t, PCR_17t, PCR_20t, PCR_23t, PCR_26t, PCR_29t, PCR_32t, PCR_35t (0 = no, 1 = yes) for days 2–35.
- Data structure note: Some measurements missing on certain days or assays unsuccessful (N/A).

## Data structure and content
- Core identifiers: ID, Description; Sex; Pop; Pathogen.
- Temporal phenotypes: Mass measurements across multiple days; eye lesion scores across multiple days.
- Infection outcomes: PCR detection results at multiple post-inoculation days; pathogen load at select days.
- Additional contextual measurements: Note on non-infected birds included to track PCR positives over time.

## Potential uses and considerations for analysts
- Opportunities:
  - Analyze relationships between pathogen isolates and host phenotypic responses (disease severity, weight change, pathogen clearance, and load).
  - Model plastic responses of hosts and/or pathogen across time and across isolates.
  - Compare dynamics across populations/origins (AZ vs AL) and across sexes.
- Considerations:
  - Data at multiple time points with some missing values; account for missingness in models.
  - High-dimensional, multi-modal data (clinical scores, mass, molecular detections, and loads) requiring careful data integration.
  - Ethical and licensing constraints are noted via Open Government Licence; ensure proper citation and provenance when reusing.