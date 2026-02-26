# Metadata for 4_Hot_Particle_Activity.csv

## Overview
- Defines the metadata schema for the 4_Hot_Particle_Activity.csv dataset, which captures radiological and physical properties of Chernobyl hot particles.
- Includes unique identifiers, spatial coordinates in a polar system, particle physical characteristics, visual classifications, and measured radiological activities (in Bq) with associated uncertainties.
- Documents date metadata for gamma, alpha, and beta measurements and the classification/interpretation of isotopic content.
- Draws on multiple published sources to support methodology and provenance.

## Key Fields and Data Model
- Identifiers
  - Code: Database serial number - unique ID
  - Identifier: UIAR unique label - chemical analysis number
- Spatial coordinates (polar system relative to Chernobyl NPP)
  - Angle_degree: Angle coordinate of the HP sampling point (clockwise from North, 0°/360°)
  - DIST_km: Distance from sampling point; note that some Polish samples have an approximate distance (e.g., 500 km)
- Particle characteristics
  - MAXSIZE_um: Maximum particle size (micrometers)
  - MINSIZE_um: Minimum particle size (micrometers)
  - VIEW: Visual representation descriptor (see field notes)
  - COLOR: Particle color
  - FORM: Inclusions or form type
  - STRUCT: Structure of particle or sampling location (e.g., crystalline, fine grained, fragmented)
  - Notes for STRUCT include sample locations (e.g., Mikolajki, Warsawa, Lomza, Bialystok, Suwalki) and HP type classification (fuel vs condensed)
  - Burnup_MW_d_kg-1: Burnup category calculated from activity ratios of low-mobile refractory radionuclides and Cs isotopes; classified into 17 groups
- Visual/qualitative grouping (Poland samples)
  - Poland particles are divided into Group A (Ru-103, Ru-106), Group B (additional Ru-103, Ru-106 and Cs/Rh isotopes), and Group C (similar to B but with higher Ru)
- Measurement dates and types
  - DATE_Gamma: Data of gamma measurement; date format dd-mmm-yyyy
  - DATE_Alpha: Data of alpha measurement; date format dd-mmm-yyyy
  - DATE_Beta: Data of beta measurement; date format dd-mmm-yyyy
- Isotopic activities (and uncertainties)
  - Activity_of_95Zr_Bq, STD_of_95Zr_Bq
  - Activity_of_95Nb_Bq, STD_of_95Nb_Bq
  - Activity_of_106Ru_Bq, STD_of_106Ru_Bq
  - Activity_of_125Sb_Bq, STD_of_125Sb_Bq
  - Activity_of_134Cs_Bq, STD_of_134Cs_Bq
  - Activity_of_137Cs_Bq, STD_of_137Cs_Bq
  - Activity_of_144Ce_Bq, STD_of_144Ce_Bq
  - Activity_of_154Eu_Bq, STD_of_154Eu_Bq
  - Activity_of_155Eu_Bq, STD_of_155Eu_Bq
  - Activity_of_54Mn_Bq, STD_of_54Mn_Bq
  - Activity_of_60Co_Bq, STD_of_60Co_Bq
  - Activity_of_241Am_Bq, STD_of_241Am_Bq
  - Date/format indicators accompany each activity field (1 = value, 2 = units/bequerels, 3 = not used)
  - Other gamma/beta/alpha activity-related fields include Total_alpha_activity_Bq
  - Activity_of_90Sr_Bq (Total 90Sr activity in the particle)
- Other descriptors
  - CODE and Identifier serve as key identifiers for data discovery and linkage
  - VIEW/FORM/STRUCT/COLOR provide multi-faceted descriptions to support interpretation and stratification

## Data Quality, Provenance, and Standards
- Measurement context and methodology
  - Activities are reported with associated standard deviations (STD_of_*_Bq) to express measurement uncertainty.
  - Burnup_MW_d_kg-1 is a calculated metric derived from activity ratios and linked to published methodology.
- Dates and formats
  - Dates are provided for gamma, alpha, and beta measurements with explicit formats (dd-mmm-yyyy) or categorical indicators.
- Data provenance and references
  - References underpinning the data and classifications:
    - Begichev et al. (1990): Reactor fuel of Unit 4 of the Chernobyl NPP
    - Kashparov et al. (1996, 1997): Formation of hot particles; maximal temperature/annealing duration
    - Kuriny et al. (1993): Particle-associated Chernobyl fallout in local/intermediate zones
    - Zhurba et al. (2009): The "hot particles" database
  - The dataset aligns with the broader “hot particles” database and related radiochemical analyses cited in the references.
- Metadata completeness and consistency
  - While most fields include explanations, some Units/Notes fields contain missing or inconsistent values (e.g., occasional typos like “bequerels” vs. “Bq”).
  - Some structural notes reference sampling locations and Polish particle groupings, requiring careful standardization for cross-dataset interoperability.
- Governance implications
  - The dataset supports standard discovery and reuse, but may require harmonization of units, date formats, and field naming for interoperability across systems and portals.
  - The metadata enables traceability back to measurement methods and literature, aiding reproducibility and data stewardship.

## Governance, Sharing, and Practical Considerations
- Data discovery and reuse
  - The presence of unique IDs (Code) and human-readable labels (Identifier) facilitates dataset discovery and cross-referencing with published sources.
- Standards and interoperability
  - Recommend standardizing units (Bq) and ensuring consistent naming for all STD_of_* fields.
  - Align date fields to a uniform date representation and ensure consistent interpretation of the DATE_* fields across datasets.
- Data sharing constraints
  - While not explicitly stated, references to embargoes and data availability limitations suggest potential sharing constraints; stewardship should capture any such constraints in portal metadata.
- Data maintenance
  - Given Burnup_MW_d_kg-1 and multiple isotopic activities, periodic updates or re-evaluations may be warranted as methods or references evolve.

## References
- Begichev S. N. et al. Preprint IAE-5268/3: Reactor Fuel of Unit 4 of the Chernobyl NPP (1990)
- Kashparov V. A. et al. Formation of Hot Particles During the Chernobyl Nuclear Power Plant Accident (1996)
- Kashparov V. A. et al. Assessment of the maximal temperature and annealing duration of Chernobyl fuel particles (1997)
- Kuriny V. D. et al. Particle associated Chernobyl fallout in local/intermediate zones (1993)
- Zhurba M. et al. The 'hot particles' data base (2009)