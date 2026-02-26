# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

## Objective and study design
- Lab-based ecotoxicology assessment of sub-lethal effects on Eisenia fetida exposed to three anonymised teabags with different PLA-cellulose blends (TBagA, TBagB, TBagC).
- Four exposure concentrations: none, 0.02%, 0.04%, 0.07%.
- Follows OECD TG 222 Earthworm Reproduction Test.
- Experimental setup: 4 replicates per treatment, 10 worms per container (40 worms per treatment), 20 ± 1 °C, dark conditions.

## Experimental procedure and materials
- Soil: 500 g LUFA 2.2 standard sandy-loam soil.
- Teabags added to soil as discs; exposure durations and containers per OECD guideline.
- Test materials and treatment combinations are recorded in detail (including teabag mass and number of teabags per soil).

## Ecotoxicological measures collected
- Survival (mortality) and body weight change.
- Reproduction metrics: number of egg cocoons, number of juveniles, and total mass of juveniles.
- Measurements taken at 28 days, with an additional 28-day incubation to assess fecundity.

## Data file and variable descriptions
- Data file: Teabags_worm_ecotoxicology.csv.
- Variables (columns) include:
  - Test_material: Teabag or control group.
  - Treatment: Unique teabag name + concentration.
  - n_teabags: Number of teabags worms were exposed to (0.5, 1, or 2).
  - Teabag_mass_soil: Mass of teabag discs in soil (g).
  - Teabag_n_soil: Number of teabag discs in soil.
  - Mass_dw_soil: Mass of soil per replicate (g).
  - Exposure: Exposure duration (days).
  - worms: Number of worms per container.
  - survival, survival_percent: Mortality data.
  - worms_mass_start, worms_mass_end: Mass of worms at start and end (g).
  - Mass_change: Mass change of worms (g).
  - n_eggs: Number of egg cocoons after 28 days.
  - n_juv: Number of juveniles after 28 days.
  - mass_juv: Total mass of juveniles (g).

## Quality control and provenance
- Adheres to OECD TG 222 (2016) Earthworm Reproduction Test protocol.
- Soil characteristics and pH, organic carbon, nitrogen content, and cation exchange capacity provided.
- Earthworms sourced from Blades Biological; acclimated for 3 weeks prior to experiment.

## Context and references
- Data accompany the publication Courtene-Jones et al (2024) on deterioration of bio-based PLA teabags and effects on earthworms (Science of the Total Environment).
- OECD guidelines cited: OECD TG 222 (2016) for the testing framework.