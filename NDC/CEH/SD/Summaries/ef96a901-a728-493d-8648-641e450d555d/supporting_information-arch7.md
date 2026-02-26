# Supporting information for: Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates

- Purpose and context
  - Investigates adaptive phenotypic plasticity and its role in pathogen infection dynamics, focusing on whether pathogens can plastically alter replication and transmission in response to host defenses.
  - Leverages a unique strain repository from an epizootic outbreak to test how plasticity relates to evolution during host resistance dynamics.

- Study design and ethics
  - Populations and subjects: 171 wild house finches (93 males, 78 females) captured in Arizona; 53 birds from Alabama and 59 from Arizona used in the study.
  - Health screening: prior infection ruled out using anti-M. gallisepticum antibodies and PCR testing.
  - Isolate inoculation: birds randomly inoculated with one of 56 M. gallisepticum isolates collected across multiple years (1994–2015).
  - Inoculation method: 20 μL culture containing 1×10^4 to 1×10^6 color-changing units/mL, applied to both eyes.
  - Housing and experimental design: Arizona birds housed in pairs; Alabama birds quarantined for 30 days before transfer to Arizona; additional health checks and treatment for other diseases.
  - Ethical approvals: IACUC approvals at Auburn University and Arizona State University; institutional biosafety authorizations and ethics committee approvals noted.

- Data collected (phenotypic and infection metrics)
  - Clinical scoring: eye lesion severity (0–5) for both eyes at days 3, 6, 8, 14, 21, 25, 28, 34 post-inoculation.
  - Morphometrics: body mass measured at -7, 0, 3, 8, 14, 21, 28, 34 days post-inoculation.
  - Infection dynamics: conjunctival and tracheal swabs collected for MG DNA detection (via PCR) and for MG load (qPCR) across multiple timepoints (e.g., days 8, 14, 21, 28; additional checks for non-infected birds across a broader range).
  - Pathogen clearance: MG DNA presence/absence in swabs over time; MG load quantified by qPCR.
  - Additional data: time-series measurements for non-infected birds (PCR results across multiple days); detailed isolate IDs and year of sampling.

- Data structure and variables (as described)
  - Core identifiers: ID (unique bird), Sex (f/m), Pop (Auburn/Opelika = AO; Greater Tempe = GT), Pathogen (year of sampling).
  - Phenotypic/time metrics: Mass_d-7, Mass_d0, Mass_d3, Mass_d8, Mass_d14, Mass_d21, Mass_d28, Mass_d34 (body mass); RE_score and LE_score for various days (eye pain/severity) across days 3, 6, 8, 13, 14, 21, 25, 28, 34.
  - Infection metrics: MG_PCR_d8, MG_PCR_d14, MG_PCR_d21, MG_PCR_d28 (MG DNA detection in swabs); Pload_8, Pload_14, Pload_21, Pload_28 (MG load in cell copies).
  - Additional infection checks: PCR_2t through PCR_35t (detection in non-infected birds across days).
  - Data quality: N/A entries used to indicate missing measurements or unsuccessful assays; data are stored with explicit data types and units (e.g., grams for mass, 0/1 for PCR detection, 0–5 for eye scores).

- Data access and citation
  - Access: Open Government Licence; dataset available at the provided DOI.
  - Citation: Bonneaud, C. (2019). Phenotypic data collected in the experimental infection study of house finches with M. gallisepticum bacterial isolates. NERC Environmental Information Data Centre. DOI provided.

- Provisions for GIS use and data integration
  - Geographic and population metadata (Pop) enables mapping of phenotypic outcomes and infection measures by origin (AO vs GT) or by site.
  - Time-series measurements (mass, eye scores, MG DNA/load) support longitudinal mapping of disease dynamics, enabling spatiotemporal visualizations when combined with location-based attributes.
  - Data cleaning and harmonization may be required due to missing measurements and complex, multi-day schedules, but the structured variable definitions support integration into map-based data products.

- References and context
  - References provide foundational methods for infection scoring, PCR and qPCR assays, and previous experimental infection protocols relevant to interpreting phenotypic and infection data.