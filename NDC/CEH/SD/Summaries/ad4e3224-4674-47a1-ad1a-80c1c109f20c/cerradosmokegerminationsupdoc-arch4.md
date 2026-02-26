# Data structure: CerradoSpeciesGermination_BrazilianSmokeWater.csv

## Overview
- The document describes two data structures and their associated metadata for seed germination experiments involving smoke-water treatments.
- Data files:
  - CerradoSpeciesGermination_BrazilianSmokeWater.csv (germination data with viability constraints)
  - CerradoSpeciesGermination_RegenSmokeWater.csv (germination data with multiple smoke concentrations)
- Includes Table 1 details for seed collection sites and a list of collection-site abbreviations with coordinates.
- Protocols cover smoke-water preparation, germination conditions, replication, observation schedules, and viability assessments.
- Aims to support reproducibility, data discovery, and cross-study comparisons within a data-management and data-strategy context.

## Data files and key columns
- CerradoSpeciesGermination_BrazilianSmokeWater.csv
  - Core columns: Species, Collection_site, Collection_date, Experiment_date, Treatment (Control_SW or SW), Replicate, Viable_seeds, Dead_seeds, Total_seeds.
- CerradoSpeciesGermination_RegenSmokeWater.csv
  - Core columns: Species, Treatment (Control, Smoke_I 2.5%, Smoke_II 5.0%), Replicate, Day, Germinated.
  - Expanded metadata (for context and provenance): Species_details, Family, Life_form, Collection_site, Collection_date, Seed_storage_months, Seeds_per_replicate.
- Both datasets capture day-by-day germination observations (Day) and daily germination counts (Germinated), with differences in treatment granularity between the two experiments.
- Observations are collected over a monitored period (30 days) or until germination stabilizes (no germination for 10 consecutive days).

## Experimental design and treatments
- Smoke-water exposure (BrazilianSmokeWater experiment)
  - Treatments: Control (distilled water) and smoke-water (1:1 concentration).
  - Seed treatment: 24-hour imbibition in solution at room temperature.
  - Smoke solution preparation: biomass (5 g) from native grasses heated at 200°C for 30 minutes; biomass soaked in 50 ml distilled water for 10 minutes and filtered.
  - Replication: 5 replicates per experiment; each replicate is prepared separately to avoid pseudoreplication.
  - Germination conditions: 27°C, 12 h light/12 h dark cycle; 60-mm Petri dishes with filter paper; daily checks for up to 30 days.
  - Post-treatment viability: tetrazolium assay (1% solution, pH 7) for seeds that did not germinate.
- Smoke solution exposure (RegenSmokeWater experiment)
  - Treatments: Control (distilled water), Smoke_I (2.5%), Smoke_II (5.0%).
  - Replication: 3–5 replicates per species.
  - Seed preparation: Non-scarified diaspores placed in Petri dishes or boxes with smoke solution or water; 24-hour imbibition at 27°C in the dark.
  - Post-imbibition handling: For smoke treatments, filter paper reset with fresh solution/water; germination monitored under a 12 h photoperiod at 27°C.
  - Smoke concentrations derived from 2.5% and 5.0% dilutions of Regen 2000® solution.
  - Seed volume per replicate: 3 mL (smaller diaspores) or 5 mL (larger diaspores).
  - Observation: daily for up to 30 days or until stabilization of germination.

## Data collection, quality control, and provenance
- Data collection and entry
  - Data recorded manually and curated to ensure accuracy and traceability.
- Quality controls
  - Viability tests constrain maximum potential germination.
  - Explicit notes on low microbial contamination; filter papers changed as needed to prevent fungal growth.
- Provenance and replication
  - Replicate handling designed to avoid pseudoreplication (separate replicates for each replicate).
  - Treatments and data collection schedules aligned with cited literature (e.g., Fichino et al. 2016; Jäger et al. 1996; Lakon 1949; Le Stradic et al. 2015; Moreira et al. 2010).

## Metadata structure and collection-site details
- Metadata fields (for context and reuse)
  - Species, Species_details, Family, Life_form, Collection_site, Collection_date, Seed_storage_months, Seeds_per_replicate, Day, Germinated.
- Collection sites (Table 1)
  - Estação Ecológica de Itirapina (EEI) – Itirapina, SP – 22°13'10"S, 47°53'54"W
  - Reserva Natural Serra do Tombador (RNST) – Cavalcante, GO – 13°35′56"S, 47°45′34"W
  - Parque Estadual do Jalapão (Jalapão) – Mateiros-TO – 10°22'40"S, 46°40'30"W
  - Parque Nacional Serra do Cipó (SC) – Jaboticatubas, MG / Santana do Riacho, MG – 19°22′01"S, 43°32′17"W
  - Pirenópolis (Pirenópolis) – Pirenópolis, GO – 15°51′14"S, 48°57′31"W
  - Estação Ecológica de Santa Bárbara (EESB) – Águas de Santa Bárbara, SP – 22°48′59"S, 49°14′12"W
  - Parque Nacional das Sempre-Vivas (PNSV) – Diamantina, MG – 17°48′18"S, 43°45′50"W
- Notes on site details
  - Abbreviations used to link data points to site details about location and coordinates.
  - Site-level details support geographic comparisons of germination responses.

## Data governance, standards, and usage considerations for Data Leaders
- Data discoverability and reuse
  - Structured CSV formats with explicit column definitions, replicate IDs, and per-day observations to support replication and cross-study comparisons.
  - Metadata fields capture biological, collection, and storage context to support provenance and data quality assessments.
- Data quality and gaps
  - Potential gaps in granularity for some fields (e.g., some fields present mainly in RegenSmokeWater data); ensure alignment to a common schema if integrating across studies.
  - Replicate autonomy is explicitly addressed to minimize pseudoreplication.
- Practical considerations for use
  - Germination counts are daily and non-cumulative by day; germination is defined by radicle emergence.
  - Viability constraints should be considered when interpreting germination potential versus observed germination.
  - The datasets support analysis of species-specific germination responses to different smoke treatments, enabling cross-site and cross-treatment comparisons within Cerrado germination ecology.

## References
- Fichino, B.S., et al. 2016. Does fire trigger seed germination in the Neotropical savannas? Biotropica.
- Jäger, A.K., et al. 1996. Effects of source of plant material on smoke extract germination. Environ. Exp. Bot.
- Lakon, G. 1949. Tetrazolium method for seed germination capacity. Plant Physiol.
- Le Stradic, S., et al. 2015. Germination in Tropical Grasslands. Austral Ecology.
- Moreira, B., et al. 2010. Disentangling the role of heat and smoke as germination cues. Ann. Bot.