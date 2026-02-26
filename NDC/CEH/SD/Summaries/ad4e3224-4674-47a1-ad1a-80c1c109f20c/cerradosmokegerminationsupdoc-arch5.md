# CerradoSpeciesGermination_BrazilianSmokeWater.csv and CerradoSpeciesGermination_RegenSmokeWater.csv

## Purpose and scope
- Documents seed germination experiments for Cerrado species under smoke-water treatments.
- Two data files: 
  - CerradoSpeciesGermination_BrazilianSmokeWater.csv (germination counts with 1:1 smoke-water treatment)
  - CerradoSpeciesGermination_RegenSmokeWater.csv (germination counts with two smoke concentrations: 2.5% and 5.0%)
- Includes both raw germination data and accompanying species-level metadata to enable cross-study reuse and comparison.

## Data structure and key fields

- CerradoSpeciesGermination_BrazilianSmokeWater.csv
  - Column information:
    - Species
    - Collection_site
    - Collection_date
    - Experiment_date
    - Treatment (Control_SW or SW)
    - Replicate (typically 5 replicates)
    - Viable_seeds
    - Dead_seeds
    - Total_seeds
  - Notes:
    - For Vellozia squamata, codes like Vellozia_squamata_CR and Vellozia_squamata_CS indicate seeds from specific sites (campos rupestres and campos sujos at RNST) detailed in Table 1.

- CerradoSpeciesGermination_BrazilianSmokeWaterMetadata.csv
  - Column information:
    - Species
    - Treatment (Control_SW or SW)
    - Replicate
    - Day (days since imbibition)
    - Germinated (seeds germinated on that day)
  - Additional metadata blocks:
    - Species
    - Species_details
    - Family
    - Life_form
    - Collection_site
    - Collection_date
    - Seed_storage_months
    - Seeds_per_replicate

- CerradoSpeciesGermination_RegenSmokeWater.csv
  - Column information:
    - Species
    - Treatment (Control, Smoke_I 2.5%, Smoke_II 5.0%)
    - Replicate (3–5 replicates)
    - Day
    - Germinated
  - Additional metadata blocks (same as above for species-level information)
  - Experimental specifics:
    - Non-scarified diaspores
    - Smoke concentrations derived from Regen 2000®
    - Volumes per replicate: small diaspores = 3 mL, larger diaspores = 5 mL
    - Imbibition and germination conditions: 24 h dark imbibition at 27°C; post-imbibition, 12 h light/12 h dark regime at 27°C
    - Observation window: up to 30 days or until germination stabilizes (no germination for 10 consecutive days)
  - Replicate setup avoids pseudoreplication by preparing smoke solutions separately for each replicate.

## Collection sites and provenance

- Table 1 provides collection-site details with standardized abbreviations, locations, and geographic coordinates, including:
  - EEI (Estação Ecológica de Itirapina) – Itirapina, SP
  - RNST (Reserva Natural Serra do Tombador) – Cavalcante, GO
  - Jalapão (Parque Estadual do Jalapão) – Mateiros, TO
  - SC (Parque Nacional Serra do Cipó) – Jaboticatubas / Santana do Riacho, MG
  - Pirenópolis – Pirenópolis, GO
  - EESB (Estação Ecológica de Santa Bárbara) – Águas de Santa Bárbara, SP
  - PNSV (Parque Nacional das Sempre-Vivas) – Diamantina, MG
- Each site entry includes an abbreviation, full location name, and precise coordinates.

## Experimental design and methods

- Smoke solution preparation (BrazilianSmokeWater trial):
  - 5 g biomass from native grasses, heated at 200°C for 30 minutes
  - Biomass soaked in 50 mL distilled water for 10 minutes, then filtered
  - Solutions prepared separately for each replicate to avoid pseudoreplication
  - 24 h imbibition in smoke solution or distilled water (control)
- Germination conditions:
  - Petri dish setup with double filter paper saturated with water
  - Germination chambers with 12 h light/12 h dark and 27°C
  - Daily monitoring for 30 days; germination defined by radicle emergence
  - Post-trial viability testing on non-germinated seeds using 1% tetrazolium solution (pH 7)
  - Microbial contamination kept low; paper changes as needed
- RegenSmokeWater trial:
  - Two smoke concentrations: 2.5% (Smoke_I) and 5.0% (Smoke_II) in Regen 2000®-based solutions
  - Control treatment with distilled water
  - Seeds placed on filter paper in Petri dishes, 24 h imbibition in dark at 27°C
  - Post-imbibition, 12 h light/12 h dark regimen at 27°C
  - Dishes monitored daily for up to 30 days or until germination stabilizes
  - Small diaspores receive 3 mL; larger diaspores receive 5 mL per replicate
  - Non-germinated seeds can be viability-tested as above

## Data quality, provenance, and governance

- Data capture and curation
  - Data recorded manually and curated to ensure quality
  - Viability tests used as a quality control constraint on maximum potential germination
- Replication and robustness
  - Multiple replicates per treatment to enable statistical comparisons
  - Separate replication of smoke solutions to avoid pseudoreplication
- Documentation and metadata standards
  - Species, site, collection date, and seed handling details included in metadata
  - Detailed site coordinates and standardized abbreviations facilitate data discovery and integration
- Reproducibility and interoperability
  - Clear procedural descriptions for smoke preparation, imbibition, germination conditions, and observation criteria
  - References provided for methodologies (Fichino et al. 2016; Jäger et al. 1996; Lakon 1949; Le Stradic et al. 2015; Moreira et al. 2010)
- Gaps and considerations for stewardship
  - Licensing and data access permissions not specified; consider applying an explicit data license
  - Date formats and units are specified in narrative; ensure ISO date formats and consistent units in the published dataset
  - Versioning and update workflow not described; establish a versioning scheme and update plan

## Data sharing, accessibility, and lifecycle

- Publication readiness
  - Well-structured data files with accompanying metadata support discoverability and reuse by researchers, educators, and policy-makers
- Governance implications
  - Align metadata with data governance practices to ensure long-term storage, cataloging in portals, and potential integration with data catalogs
  - Ensure ongoing updates reflect any new replication runs, sites, or methodological refinements
- Stewardship recommendations
  - Maintain a data dictionary and method snapshots to preserve experimental context
  - Link data to persistent identifiers (e.g., DOIs) and apply an explicit data license
  - Establish a curation workflow to preserve historical versions and capture changes over time

## Practical considerations for Data Stewards

- Anticipated challenges
  - Incomplete or evolving user needs across researchers and institutions
  - Timeliness of data receipt from collaborators and sites
  - Ensuring all data producers meet metadata and format standards
  - Interoperability across different data systems and formats
  - Handling large numbers of sites and replicates, and potential updates to site coordinates or taxonomy
- How this dataset addresses stewardship goals
  - Comprehensive site details, explicit replication, and robust metadata improve discoverability and usability
  - Clear treatment distinctions (Control vs. Smoke; 2.5% and 5.0% with Regen) support comparative analyses
  - Explicit methodological details enhance reproducibility and reusability in meta-analyses of fire and smoke-related germination cues