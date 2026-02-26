# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

## Overview
- Lab-based ecotoxicology study assessing sub-lethal toxicity of Eisenia fetida to three anonymised teabag brands with varying PLA-cellulose blends.
- Four exposure concentrations (none, 0.02%, 0.04%, 0.07%) in LUFA 2.2 sandy-loam soil.
- Endpoints: survival, growth (mass change), reproduction (egg cocoons, juveniles, juvenile mass).
- Followed OECD TG 222 earthworm reproduction test protocol.

## Data file and schema
- Data file: Teabags_worm_ecotoxicology.csv.
- Table 1 variables (column descriptions included in dataset):
  - Test_material: Teabag or control group.
  - Treatment: Unique teabag name + concentration.
  - n_teabags: Equivalent number of teabags worms were exposed to (0.5, 1, or 2 teabags).
  - Teabag_mass_soil: Mass of teabag discs in soil (g).
  - Teabag_n_soil: Number of teabag discs in soil.
  - Mass_dw_soil: Mass of soil per replicate (g).
  - Exposure: Exposure duration (days).
  - worms: Number of worms per container.
  - survival: Number of worms surviving after 28 days.
  - survival_percent: Survival percentage after 28 days.
  - worms_mass_start: Mass of 10 worms at day 0 (g).
  - worms_mass_end: Mass of 10 worms at day 28 (g).
  - Mass_change: Mass change of the worms (g).
  - n_eggs: Number of egg cocoons produced after 28 days.
  - n_juv: Number of juveniles produced after 28 days.
  - mass_juv: Total mass of juveniles per replicate (g).

## Experimental design and data collection
- Four teabag brands (TBagA, TBagB, TBagC, plus control) with different PLA–cellulose compositions.
- Four treatment levels corresponding to teabag concentration: 0%, 0.02%, 0.04%, 0.07%.
- Experimental setup: 4 replicates per treatment, 10 earthworms per container (40 worms per treatment), total n=40 per treatment.
- Test conditions: 20 ± 1 °C, dark.
- Duration: 28 days of exposure, with survival and body weight measured; cocoons counted at day 28; containers incubated an additional 28 days to quantify juveniles and their mass.

## Quality control and standards
- Protocol: OECD TG 222 Earthworm Reproduction Test (OECD, 2016) followed.
- Soil: LUFA 2.2 sandy-loam soil (pH 5.5 ± 0.1; organic carbon 1.66 ± 0.6%; nitrogen 0.19 ± 0.06%; cation exchange capacity 8.5 ± 1.8 meq/100 g).
- Earthworms: sourced from Blades Biological; acclimated to laboratory conditions for 3 weeks prior to the experiment.

## Data provenance and related outputs
- Part of the BIO-PLASTIC-RISK project (NERC grants NE/V007556/1 and NE/V007246/1).
- Data accompany Courtene-Jones et al. (2024): Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms (Science of the Total Environment). DOI: https://doi.org/10.1016/j.scitotenv.2024.172806.

## Potential data uses and applications
- Enables assessment of sub-lethal ecotoxicity of bio-based teabags to earthworms.
- Suitable for meta-analyses or comparative risk assessments with other soil ecotoxicology datasets.
- Can be transformed into dashboards or self-serve data products focusing on mortality, growth, and reproductive endpoints.
- Supports data-driven discussions on environmental risk of PLA–cellulose blends in consumer products.

## References
- OECD (2016). OECD Guideline for the Testing of Chemicals, Technical Guidance 222: Earthworm Reproduction Test (Eisenia fetida/Eisenia andrei). Vol. OECD TG 222.
- Courtene-Jones et al. (2024). Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment.