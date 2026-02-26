# CerradoSpeciesGermination_BrazilianSmokeWater.csv

## Overview
- Describes germination experiments on Cerrado seeds subjected to smoke-water treatment versus control.
- Contains data from Brazilian smoke-water germination experiments and accompanying metadata to enable self-serve analysis.

## Data structure: BrazilianSmokeWater
- Core data file: CerradoSpeciesGermination_BrazilianSmokeWater.csv
- Key columns
  - Species: seed species used in germination experiment (e.g., Vellozia squamata; codes indicate collection areas)
  - Collection_site: site of seed collection
  - Collection_date: date seeds were collected
  - Experiment_date: date of the original germination experiment
  - Treatment: Control_SW or smoke-water treated (SW)
  - Replicate: replicate number (typical 5 replicates)
  - Viable_seeds: number viable by tetrazolium assay
  - Dead_seeds: number non-viable by tetrazolium assay
  - Total_seeds: total seeds used in the replicate
- Metadata linkage: paired with CerradoSpeciesGermination_BrazilianSmokeWaterMetadata.csv

## Data structure: BrazilianSmokeWater Metadata
- Metadata file: CerradoSpeciesGermination_BrazilianSmokeWaterMetadata.csv
- Key columns
  - Species, Treatment, Replicate, Day, Germinated
  - Day: days since imbibition (time points post-imbibition)
  - Germinated: number of seeds germinated on that day (non-cumulative)

## Collection sites (Table 1)
- Estação Ecológica de Itirapina (EEI): Itirapina, SP
- Reserva Natural Serra do Tombador (RNST): Cavalcante, GO
- Parque Estadual do Jalapão (Jalapão): Mateiros, TO
- Parque Nacional Serra do Cipó (SC): Jaboticatubas / Santana do Riacho, MG
- Pirenópolis (Pirenópolis): Pirenópolis, GO
- Estação Ecológica de Santa Bárbara (EESB): Águas de Santa Bárbara, SP
- Parque Nacional das Sempre-Vivas (PNSV): Diamantina, MG
- Coordinates provided for each site (lat/long in degrees).

## Smoke solution treatments (Brazilian)
- Purpose: evaluate effects of smoke on seed germination using smoke aqueous solutions (1:1) prepared from native grass biomass.
- Control: seeds imbibed in distilled water for 24 h (same as treated seeds).
- Smoke solution preparation (per replicate): 5 g biomass combusted at 200°C for 30 min; biomass soaked in 50 ml distilled water for 10 min; filtered; solutions prepared separately for each replicate to avoid pseudoreplication.
- After 24 h imbibition in smoke solution, seeds proceed to germination as described below.

## Germination protocol (Brazilian)
- Post-treatment, seeds placed on double-layer filter paper in 60-mm Petri dishes with distilled water.
- Incubation: germination chambers with 12 h light/12 h dark (fluorescent light, 15 W) and 27°C (per Fichino et al. 2016 methodology).
- Watering: add water as needed during trials.
- Observations: every two days for 30 days to count germinated seeds (germination defined by radicle emergence).
- Microbial control: filter paper changed as needed to reduce fungal growth; microbial contamination generally low.
- Post-trial viability: non-germinated seeds tested with 1% tetrazolium solution (pH 7) to assess viability.

## Quality control (Brazilian)
- Data recorded manually and curated in spreadsheet format.
- Viability data act as a constraint on maximum potential germination.

## Data structure: RegenSmokeWater
- Core data file: CerradoSpeciesGermination_RegenSmokeWater.csv
- Key columns
  - Species: seed species used in germination experiment
  - Treatment: Control, Smoke 2.5% (Smoke_I), or Smoke 5.0% (Smoke_II)
  - Replicate: 3–5 replicates per species
  - Day: days since imbibition
  - Germinated: seeds germinated on that day (not cumulative)

- Secondary data/metadata (segmented in the document):
  - Species, Species_details, Family, Life_form: taxonomic and biological details
  - Collection_site: seed collection site (details in Table 1)
  - Collection_date: date of seed collection
  - Seed_storage_months: months between collection and germination experiment
  - Seeds_per_replicate: number of seeds used per replicate

## Experimental setup (RegenSmokeWater)
- Non-scarified diaspores placed in Petri dishes (9 cm) or acrylic boxes (10x10 cm) with smoke solutions or distilled water.
- Incubation: 24 h in dark at 27°C; then switch to 12 h photoperiod with 27°C.
- Seed volumes: small diaspores receive 3 mL per replicate; larger diaspores receive 5 mL per replicate.
- Temperature/photoperiod: 27°C, dark for first 24 h, then 12 h light/12 h dark.
- Concentrations: two smoke concentrations used—2.5% (Smoke_I) and 5.0% (Smoke_II)—plus a Control with distilled water.
- Observation window: daily checks for 30 days or until germination stabilizes (no germination for 10 consecutive days).
- Germination criteria: germination counted when diaspores show root and/or cotyledon protrusion.
- Replication: 3–5 replicates per species and treatment.

## Data provenance and references
- Methods draw from: Le Stradic et al. 2015; Fichino et al. 2016; Jäger et al. 1996; Lakon 1949; Pausas et al. and related seed germination literature.
- Data quality notes: manual entry with explicit viability controls; treatment replicates prepared separately to avoid pseudoreplication.

## Usage notes for data users
- Link BrazilianSmokeWater data with its metadata for day-by-day germination analysis and viability constraints.
- Use RegenSmokeWater data to compare responses across species to different smoke concentrations and to examine time-to-germination dynamics.
- Leverage Table 1 site details for geographic or biogeographic analyses; coordinates enable mapping and spatial filtering.
- Consider replicates and treatment structure (Control, Smoke_I, Smoke_II) when modeling germination rates or conducting meta-analyses.