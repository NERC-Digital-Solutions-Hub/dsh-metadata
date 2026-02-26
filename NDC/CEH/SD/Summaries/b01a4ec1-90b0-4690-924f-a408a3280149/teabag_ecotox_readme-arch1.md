# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

## Overview
- Lab-based ecotoxicology study assessing sub-lethal effects on Eisenia fetida exposed to four concentrations of three anonymised bio-based teabags with varying PLA-cellulose blends.
- Focus on mortality, growth, and reproduction (egg cocoons and juveniles) following OECD TG 222 guidelines.
- Data accompany the published work by Courtene-Jones et al. (2024) and are provided in a single CSV file: Teabags_worm_ecotoxicology.csv.

## Experimental design
- Organisms: Eisenia fetida (adult, clitellate), acclimated for 3 weeks prior to testing.
- Test materials: Three anonymised teabag brands (TBagA, TBagB, TBagC) with different PLA-cellulose compositions.
- Concentrations: Four levels — none (control), 0.02%, 0.04%, 0.07% teabag material in soil.
- Soil: LUFA 2.2 standard sandy-loam soil (500 g per replicate).
- Replication: Four replicates per treatment, with 10 earthworms per container (40 worms per treatment).
- Conditions: 20 ± 1 °C, dark.
- Duration and endpoints: 28-day exposure with survival and body weight measured at days 0 and 28; then incubation for an additional 28 days to assess fecundity (egg cocoons, juveniles, juvenile mass).

## Data collected
- Ecotoxicological measures:
  - Mortality (survival, survival_percent)
  - Growth (mass change; start vs end mass)
  - Reproduction (n_eggs, n_juv, mass_juv)
- Timescales:
  - Day 0 and Day 28 measurements for survival and growth
  - Post-28-day incubation for juvenile production and mass
- Data file: Teabags_worm_ecotoxicology.csv

## Dataset structure and key variables
- Test_material: Teabag or control group (description of teabag brand/type)
- Treatment: Unique identifier combining teabag name and concentration
- n_teabags: Number of teabags worms were exposed to (0.5, 1, or 2 per container)
- Teabag_mass_soil: Mass of teabag discs in soil (grams)
- Teabag_n_soil: Number of teabag discs in soil
- Mass_dw_soil: Mass of soil per replicate (g)
- Exposure: Exposure duration (days)
- worms: Number of worms per test container
- survival: Number of worms surviving after 28 days
- survival_percent: Survival percentage after 28 days
- worms_mass_start: Mass of the 10 worms at day 0
- worms_mass_end: Mass of the 10 worms at day 28
- Mass_change: Mass change of the worms (grams)
- n_eggs: Number of egg cocoons produced after 28 days
- n_juv: Number of juveniles produced after 28 days
- mass_juv: Total mass of juveniles per replicate (grams)

## Quality control and environmental context
- OECD TG 222 Earthworm Reproduction Test followed (OECD, 2016).
- Soil characterized as loamy sand with documented pH, organic carbon, nitrogen content, and cation exchange capacity.
- Earthworms sourced from Blades Biological and acclimated prior to testing.

## Data usage and references
- Data enable analysis of sub-lethal toxicity effects of bio-based teabags on earthworms, including growth and reproductive outcomes across dose levels.
- Dataset supports correlations between teabag exposure, survival, growth, and reproductive output, and can inform risk assessments of PLA-based packaging in soils.
- Related publication: Courtene-Jones et al. (2024), Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment. DOI: 10.1016/j.scitotenv.2024.172806
- Primary methodological reference: OECD (2016) OECD Guideline for the Testing of Chemicals, TG 222.