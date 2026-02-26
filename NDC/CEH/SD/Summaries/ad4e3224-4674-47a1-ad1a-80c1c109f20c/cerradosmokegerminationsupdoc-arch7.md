# Data structure: CerradoSpeciesGermination_BrazilianSmokeWater.csv and CerradoSpeciesGermination_RegenSmokeWater.csv

- Overview
  - Describes two datasets of seed germination experiments in Cerrado plant species, focusing on smoke-water treatments to assess germination responses.
  - Data are structured for per-replicate, day-by-day germination tracking and include detailed metadata on collection and experimental conditions.
  - The information supports GIS-style mapping and spatial analysis of germination outcomes across collection sites.

## Data structure details

- CerradoSpeciesGermination_BrazilianSmokeWater.csv
  - Key columns
    - Species: seeds used; includes notes on accession types for Vellozia squamata (different collection areas).
    - Collection_site: site abbreviation or name; ties to Table 1 for location details.
    - Collection_date: when seeds were collected.
    - Experiment_date: date of the germination experiment.
    - Treatment: Control_SW or smoke-water treatment.
    - Replicate: replicate number (typically 5 replicates per experiment).
    - Day: days since imbibition (start of germination test).
    - Germinated: seeds germinated on that day.
    - Viable_seeds, Dead_seeds, Total_seeds: used for quality/viability context (from initial viability tests).
- CerradoSpeciesGermination_BrazilianSmokeWater.csv (procedural details)
  - Smoke solution treatments
    - Smoke solutions prepared from biomass of native grasses; 5 g biomass heated at 200°C for 30 min, soaked in 50 mL distilled water for 10 min, then filtered.
    - Solutions prepared separately for each replicate to avoid pseudoreplication.
    - Imbibition: 24 h at room temperature before sowing; control uses distilled water.
- Germination procedure (BrazilianSmokeWater)
  - After imbibition, seeds placed on double-filter-paper in 60-mm Petri dishes with water or smoke solution.
  - Incubation: germination chambers at 27°C; lighting regime starts with 12 h light (after initial 24 h imbibition conditions).
  - Observations every two days for 30 days; germination defined by appearance of the radicle.
  - Post-trial viability tests on non-germinated seeds using 1% tetrazolium (pH 7).
  - Data quality: manually recorded and curated; viability constrains maximum potential germination.

- CerradoSpeciesGermination_RegenSmokeWater.csv
  - Key columns
    - Species: seeds used (binomial name).
    - Species_details: full species name including authorities.
    - Family, Life_form: taxonomic and life-form information.
    - Collection_site, Collection_date: site and date of seed collection.
    - Seed_storage_months: storage duration between collection and germination.
    - Seeds_per_replicate: number of seeds used per replicate.
    - Treatment: Control, Smoke_I (2.5% smoke-water), Smoke_II (5.0% smoke-water).
    - Replicate: 3 to 5 replicates per species.
    - Day, Germinated: daily germination counts (not cumulative).
- RegenSmokeWater procedure details
  - Microbial setup and treatment
    - Seeds exposed to two smoke concentrations (2.5% and 5.0%) and a water control.
    - Three to five replicates per experiment.
    - Inoculum: 3 mL (small diaspores) or 5 mL (larger diaspores) per replicate with corresponding solutions.
  - Growth conditions
    - After 24 h imbibition in dark at 27°C, germination monitored daily for up to 30 days or until stabilization (no germination for 10 consecutive days).
- Common experimental notes
  - Germination criteria: germination defined by root and/or cotyledon protrusion.
  - Photoperiod adjustments: initial 24 h imbibition in dark, then 12 h photoperiod with light.
  - References for methodology: works by Fichino et al. (2016), Jäger et al. (1996), Lakon (1949), Le Stradic et al. (2015), Moreira et al. (2010).

## Collection sites and geospatial details

- Table 1: Collection site details with abbreviations and coordinates
  - EEI: Itirapina Ecological Station, Itirapina, SP (22°13'10"S; 47°53'54"W)
  - RNST: Serra do Tombador Natural Reserve, Cavalcante, GO (13°35′56"S; 47°45′34"W)
  - Jalapão: Parque Estadual do Jalapão, Mateiros-TO (10°22'40"S; 46°40'30"W)
  - SC: Serra do Cipó National Park, Jaboticatubas/Santana do Riacho, MG (19°22′01" S; 43°32′17"W)
  - Pirenópolis: Pirenópolis, GO (15°51′14″ S, 48°57′31″W)
  - EESB: Santa Bárbara Ecological Station, Águas de Santa Bárbara, SP (22°48'59"S; 49°14'12"W)
  - PNSV: Sempre-Vivas National Park, Diamantina, MG (17°48′18″S; 43°45′50″W)
- Use in GIS
  - Site abbreviations and precise coordinates enable mapping of seed collection origins and potential spatial analysis of germination responses by region and habitat type.

## Experimental treatments and data capture notes for GIS integration

- Smoke-treatment methodology (Brazilian data)
  - Smoke solutions prepared from local biomass; replicated per dataset; 24 h imbibition; treatment vs. water control; 27°C germination environment.
- Smoke-treatment methodology (Regen data)
  - Two smoke concentrations (2.5%, 5.0%) plus control; replication per species; standardized dosing (3 mL or 5 mL) per replicate depending on seed size.
- Temporal data
  - Day-by-day germination counts allow temporal GIS analyses of germination dynamics across sites and species.
- Data quality and provenance
  - Manual data entry with curation; viability tests provide constraints on maximum potential germination, informing data interpretation and mapping of usable germination capacity.

## References (methods and context)

- Fichino et al., 2016; Moreira et al., 2010; Jäger et al., 1996; Lakon, 1949; Le Stradic et al., 2015; additional methodological context in the cited works.