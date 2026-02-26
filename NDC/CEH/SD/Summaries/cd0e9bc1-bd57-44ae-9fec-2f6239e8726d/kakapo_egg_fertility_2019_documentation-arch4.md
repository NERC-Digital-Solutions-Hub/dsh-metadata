# Kākāpō Egg Fertility 2019: Documentation

- This dataset documents origin, fertility, and physical characteristics of kākāpō eggs laid in New Zealand during the 2018/19 breeding season, on Anchor and Whenua Hou islands.
- Eggs were laid in natural nests and then artificially incubated as part of the Kākāpō Recovery Programme.
- Of 252 eggs laid, 129 failed to develop; yolks from these undeveloped eggs were preserved in formalin and sent to the University of Sheffield, UK for analysis to determine fertilization status and sperm presence.

## Project Rationale and Context
- Goal: distinguish fertilisation failure from early embryo death to inform conservation management.
- Approach: collect, sample, and inspect undeveloped eggs to determine fertilization outcomes and sperm metrics.
- Funding: Natural Environment Research Council Urgency Grant (NE/T00200X/1).

## People & Roles
- University of Sheffield (UK): principal investigator and co-investigator analyzed undeveloped eggs and oversaw data management.
- Kākāpō Recovery Programme (New Zealand DOC): sampling of undeveloped eggs, data collection on egg sizes and sample weights, and liaison among teams.
- Wider Kākāpō Recovery Team: field monitoring of breeding, nests, incubation, and management activities.

## Study Population and Setting
- Managed population on predator-free offshore islands: Whenua Hou / Codfish Island and Anchor Island.
- Breeding population around 110 individuals; mating events recorded; large breeding season with 12 females artificially inseminated.
- Mating and reproduction are closely monitored; chicks are returned to nests after hatching.

## Sample Collection & Analysis
- Eggs candled daily during artificial incubation; undeveloped eggs opened and yolks preserved in 5% formalin.
- Samples shipped to the University of Sheffield (CITES GB041) for laboratory analysis.
- At Sheffield: yolks rinsed, PVL (perivitelline layer) examined for sperm; germinal discs checked for embryonic cells using Hoechst 33342 stain and fluorescence microscopy; sperm counts recorded.
- PVL metrics and egg characteristics collected include:
  - PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm
  - Fertilization status (fertilized), with 128 undeveloped eggs analyzed (out of 129 undeveloped eggs)
  - Egg dimensions and weights: length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
- Data include two merged datasets: one for all 252 eggs and a second for undeveloped eggs with detailed PVL and physical measurements.

## Dataset Structure
- File 1: kakapo_egg_fertility_2019-1_all_eggs
  - 252 rows, 10 columns
  - Key fields: egg_id, island, mother, clutch, developed, early_EM, fertile, examined, female_multiple_males, female_AI
- File 2: kakapo_egg_fertility_2019-2_undeveloped_eggs
  - 129 rows, 15 columns
  - Key fields: egg_id, egg_number, fertilized, PVL_sperm, PVL_holes, PVL_area_mm, mean_sperm_mm, note, length, width, preserve_weight, fresh_weight, alb_weight, yolk_weight, shell_weight
- egg_id is the linking key between files, enabling merging of data where needed

## Additional Notes and Data Context
- The NZ Department of Conservation Kākāpō Recovery Programme maintains broader population data, management methods, and reproductive histories for the eggs and mothers involved in this study.
- The dataset provides comprehensive metadata to support data quality, discoverability, and potential reuse for conservation decision-making and cross-network collaboration.

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: field data collection, sample handling, cross-border data transfer, laboratory analysis, and structured data publication.
- Highlights data governance considerations: handling of biologically sensitive samples, formalin preservation, and CITES-compliant transfers.
- Provides a clear, merged dataset design with a stable key (egg_id) to enable integration with broader population data and longitudinal analyses.
- Supports user-focused data practices: detailed documentation of variables and contexts to ensure data usability for policy colleagues and external partners.