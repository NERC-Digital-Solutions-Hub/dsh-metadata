# Data structure: CerradoSpeciesGermination_BrazilianSmokeWater.csv

## Overview
- Describes seed germination experiments for Cerrado species exposed to smoke-water treatments.
- Two linked data files: a primary germination dataset and a metadata dataset.
- Aims to capture species, collection details, treatment types, replication, germination counts over time, and viability checks.

## Data structure: Key columns (CerradoSpeciesGermination_BrazilianSmokeWater.csv)
- Species: seed species (e.g., Vellozia squamata and related CR/CS collections).
- Collection_site: site abbreviation (e.g., EEI, RNST) with details in Table 1.
- Collection_date: date seeds were collected.
- Experiment_date: date of the original germination experiment.
- Treatment: Control_SW or smoke-water treated (SW).
- Replicate: replicate number (typically 5 replicates per experiment).
- Viable_seeds: seeds viable by tetrazolium assay.
- Dead_seeds: non-viable seeds by tetrazolium assay.
- Total_seeds: total seeds used in the replicate.

## Data structure: Metadata (CerradoSpeciesGermination_BrazilianSmokeWaterMetadata.csv)
- Species: seed species (consistent with the main file).
- Treatment: Control_SW or SW.
- Replicate: replicate number (usually 5).
- Day: day of observation (days since imbibition).
- Germinated: number of seeds germinated on that day (not cumulative).

## Collection sites (Table 1)
- Provides abbreviations, full site names, locations (city/state), and precise coordinates for each seed source:
  - EEI: Estação Ecológica de Itirapina, Itirapina, SP. Coordinates: 22°13'10"S, 47°53'54"W.
  - RNST: Reserva Natural Serra do Tombador, Cavalcante, GO. Coordinates: 13°35′56"S, 47°45′34"W.
  - Jalapão: Parque Estadual do Jalapão, Mateiros-TO. Coordinates: 10°22'40"S, 46°40'30"W.
  - SC: Parque Nacional Serra do Cipó, Jaboticatubas/Santana do Riacho, MG. Coordinates: 19°22′01" S, 43°32′17"W.
  - Pirenópolis: Pirenópolis, GO. Coordinates: 15°51′14" S, 48°57′31"W.
  - EESB: Estação Ecológica de Santa Bárbara, Águas de Santa Bárbara, SP. Coordinates: 22°48'59"S, 49°14'12"W.
  - PNSV: Parque Nacional das Sempre-Vivas, Diamantina, MG. Coordinates: 17°48′18"S, 43°45′50"W.

## Smoke solution treatments (BrazilianSmokeWater dataset)
- Purpose: evaluate effects of smoke on germination using smoke aqueous solutions at 1:1 concentration.
- Control: seeds imbibed in distilled water for 24 h.
- Smoke preparation:
  - Biomass: native grasses from one study site; 5 g biomass exposed to 200°C for 30 min.
  - After exposure, biomass soaked in 50 ml distilled water for 10 minutes, then filtered.
  - Solutions prepared separately for each replicate to avoid pseudoreplication.
- Post-treatment: seeds germinated after 24 h imbibition under specified conditions.

## Germination procedure
- After treatments, seeds on double-filter-paper in 60-mm Petri dishes with distilled water.
- Growth conditions: germination chambers, 12 h light/12 h dark, 27°C; fluorescent light 15 W.
- Water added as needed; observations every two days for 30 days.
- Germination definition: emergence of the radicle.
- Contamination management: filter paper changes as needed to prevent fungal growth.
- Non-germinated seeds: viability tested with 1% tetrazolium solution (pH 7) after the experiment.
- Data: daily counts of germinated seeds; germinated seeds removed from dishes.

## Quality control
- Data recorded manually and curated.
- Viability (tetrazolium test) used as a constraint on maximum potential germination.

## Data usage notes (Brazilian SmokeWater)
- Data are structured to support models of germination response to smoke exposure across species and sites.
- Each replicate is kept independent to avoid pseudoreplication and to enable robust statistical analysis.

## References (methodology context)
- Fichino et al., 2016 – germination tests in Neotropical savannas.
- Jäger et al., 1996 – smoke extract preparation effects.
- Lakon, 1949 – tetrazolium viability method.
- Le Stradic et al., 2015; Moreira et al., 2010 – germination cues and conditions.

## Data structure: CerradoSpeciesGermination_RegenSmokeWater.csv

### Overview
- Secondary dataset focusing on RegenSmokeWater treatments with two smoke concentrations (2.5% and 5.0%) plus control.
- Captures species-specific germination responses under regeneration-related smoke exposure.

### Key columns
- Species: seed species (binomial name).
- Treatment: Control, Smoke_I (2.5%), Smoke_II (5.0%).
- Replicate: 3–5 replicates per experiment.
- Day: day of observation since imbibition.
- Germinated: cumulative or per-day germination counts (as recorded).

### Additional species- and collection-related columns
- Species_details: full species name including authorities.
- Family: taxonomic family.
- Life_form: plant life form classification.
- Collection_site: site abbreviation (with details as in Table 1).
- Collection_date: date seeds collected.
- Seed_storage_months: time between collection and germination experiment (months).
- Seeds_per_replicate: number of seeds used per replicate.

### Experimental setup
- Non-scarified diaspores placed in Petri dishes or acrylic boxes with either smoke solutions or water.
- Incubation: 24 h exposure to smoke solutions in dark; post-exposure germination under 27°C with 12 h photoperiod.
- Post-exposure, setups adjusted to 12 h light, in 27°C conditions; daily monitoring for up to 30 days or until germination stabilizes (no germination for 10 consecutive days).
- Smoke concentrations: 2.5% and 5.0% using Regen 2000® diluted in distilled water.
- Treatment groups: Control, Smoke 2.5% (Smoke_I), Smoke 5.0% (Smoke_II).
- Volume per replicate: 3 mL for small diaspores; 5 mL for larger diaspores.

## References (RegenSmokeWater context)
- Fichino et al., 2016; Jäger et al., 1996; Lakon, 1949; Le Stradic et al., 2015; Moreira et al., 2010 (same methodological references as above).