# Kākāpō Egg Fertility 2019: Documentation

## Overview
- Dataset on origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season.
- Eggs laid in natural nests and artificially incubated as part of the Kākāpō Recovery Programme.
- Of 252 eggs laid, 129 undeveloped eggs were sampled; yolks were removed, preserved in formalin, and transported to the University of Sheffield for analysis of fertilization status and early embryo death, plus sperm counts on the perivitelline layer.

## Rationale and Aims
- The kākāpō has a high hatching failure rate, with undeveloped eggs historically attributed to male infertility.
- Recent evidence suggests fertilisation failure is rare; the project aimed to distinguish fertilisation failure from early embryo death to inform conservation management.
- Funded by Natural Environment Research Council Urgency Grant (NE/T00200X/1).

## Study Population and Management Context
- The kākāpō population is managed by the Department of Conservation (DOC) Kākāpō Recovery Team on predator-free offshore islands.
- Breeding occurs primarily on Whenua Hou / Codfish Island and Anchor Island, with 110 individuals and detailed mating/nest monitoring.
- Management practices include decoy nests, artificial incubation, and artificial insemination (12 females during this season).

## Methods and Analysis
- Eggs were candled daily during artificial incubation; undeveloped eggs were opened, yolks preserved in 5% formalin, and shipped to Sheffield (CITES GB041).
- At Sheffield: yolks were examined for fertilization and embryo presence using Hoechst 33342 staining and fluorescence microscopy; PVL (perivitelline layer) was inspected for sperm, and sperm counts were recorded.
- Sampled undeveloped eggs: 128 of 129 undeveloped eggs (98% of undeveloped eggs).

## Datasets and Structure
- Two CSV files:
  - kakapo_egg_fertility_2019-1_all_eggs: 252 eggs, 10 columns.
  - kakapo_egg_fertility_2019-2_undeveloped_eggs: 129 undeveloped eggs, 15 columns.
- Common key: egg_id (allows merging of datasets).
- File 1 fields (example): egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI.
- File 2 fields (example): egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight.

## Key Variables by Dataset
- Fertility and development: developed, early_EM, fertile, examined (File 1); fertilized (File 2).
- Sperm and PVL metrics: PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm (File 2).
- Physical egg characteristics: length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight (File 2).
- Demographics and management context: island, mother, clutch, female_multiple_males, female_AI (File 1).

## Governance, Access, and Context
- The broader Kākāpō Recovery Programme holds additional data on population, management methods, and reproductive histories.
- Samples and datasets are prepared to be integrated with other environmental monitoring data and stored in appropriate portals for accessibility.

## Implications for Environmental Monitoring and Policy
- Provides standardized, traceable data to assess fertilisation dynamics and embryo viability in a critically endangered species.
- Enables cross-dataset analyses to evaluate factors influencing reproductive success and the effectiveness of conservation interventions.
- Highlights the importance of making underlying data accessible to support broader monitoring, transparency, and policy evaluation.