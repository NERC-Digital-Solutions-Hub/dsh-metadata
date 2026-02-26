# Supporting information for: Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

- Purpose and scope
  - Provides phenotypic data from an experimental infection study of house finches inoculated with Mycoplasma gallisepticum isolates to investigate phenotypic plasticity in infection dynamics.
  - Focuses on how host phenotype (e.g., clinical signs, body mass) relates to pathogen load and presence across time.

- Access, licensing, and citation
  - Open Government Licence; data accessible at the provided DOI.
  - Primary citation: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. https://doi.org/10.5285/ef96a901-a728-493d-8648-641e450d555d

- Study design and sampling
  - Species and origin: wild house finches (N=171; 93 males, 78 females) captured in Arizona and Alabama.
  - Ethics and approvals: IACUC approvals (Auburn University and Arizona State University) and institutional authorizations; animals screened to ensure no prior M. gallisepticum infection.
  - Inoculation: 53 birds from Alabama and 59 from Arizona inoculated with one of 56 M. gallisepticum isolates collected during epidemics (1994–2015); inoculation by 20 μL of culture containing 1 × 10^4 to 1 × 10^6 CFU/mL, administered to both eyes.
  - Housing: birds housed in pairs in Arizona; random assignment to isolates; controls for non-infected birds included.
  - Monitoring and endpoints: clinical eye lesion scores (0–5) recorded at days 3, 6, 8, 14, 21, 25, 28, 34 post-inoculation; body mass measured at multiple time points; pathogen clearance assessed by PCR from conjunctival/tracheal swabs at multiple days; euthanization at day 35.

- Data collected and key variables
  - Identification and demographics: ID, Sex, Population (Pop; AO = Auburn/Opelika; GT = Greater Tempe).
  - Pathogen information: Pathogen (isolate year), isolates, MG_PCR_dX (presence/absence of M. gallisepticum DNA in swabs at specified days), Pload_dX (MG load as cell copies at specified days), PCR_XXt fields for non-infected birds across multiple days.
  - Phenotypic measurements: Mass_d-7, Mass_0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34 (body mass in grams at specified days).
  - Clinical signs: RE_score.d3, LE_score.d3; RE_score.d6, LE_score.d6; RE_score.d8, LE_score.d8; RE_score.d13, LE_score.d13; RE_score.d14, LE_score.d14; RE_score.d21, LE_score.d21; RE_score.d25, LE_score.d25; RE_score.d28, LE_score.d28; RE_score.d34, LE_score.d34 (eye lesion scores for right/left eyes, 0–5).
  - Load and detection metrics: MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (PCR detection for infected birds at these days; 0 = no, 1 = yes).
  - Pathogen load metrics: Pload_8, Pload_14, Pload_21, Pload_28 (MG load in cell copies at respective days).
  - Data completeness: Data structure notes that N/A indicates missing measurements or failed molecular assays.

- Data structure and quality notes
  - Data fields include IDs, dates, units, data types (mostly numeric, some text).
  - Non-infected birds have PCR results recorded for days 2–35 in multiple timepoints.
  - Measurements ensure blinding for lesion scoring (scorer unaware of treatment).

- Potential data use and products
  - Time-series analyses of host response to different M. gallisepticum isolates.
  - Analyses linking clinical symptoms with pathogen presence/loads over time.
  - Cross-isolate comparisons to study phenotypic plasticity in infection dynamics.
  - Data can be transformed into dashboards or self-serve tables for end users interested in host–pathogen interaction dynamics.

- References (used in data collection)
  - Key references related to field isolates and experimental infection protocols are cited within the metadata (listed in the document).