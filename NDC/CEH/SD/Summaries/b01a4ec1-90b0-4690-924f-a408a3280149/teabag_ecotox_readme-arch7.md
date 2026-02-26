# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

## Overview
- Lab-based ecotoxicology study assessing sub-lethal effects of earthworms (Eisenia fetida) exposed to four concentrations of three anonymised bio-based teabag brands with varying PLA–cellulose blends.
- Data collected include mortality, growth, and reproduction metrics following OECD TG 222 Earthworm Reproduction Test.
- Dataset comprises a single CSV file: Teabags_worm_ecotoxicology.csv.
- Supported by the BIO-PLASTIC-RISK project (NERC grants NE/V007556/1 and NE/V007246/1).
- Related publication: Courtene-Jones et al. (2024) in Science of the Total Environment.

## Experimental design and methods
- Test materials: Three anonymised teabag brands (TBagA, TBagB, TBagC) with different PLA–cellulose compositions; plus a control.
- Concentrations: 0% (none), 0.02%, 0.04%, 0.07% teabag material by weight.
- Soil: 500 g LUFA 2.2 standard sandy-loam soil (Germany), used per replicate.
- Organisms: Adult clitellate Eisenia fetida; acclimated before testing.
- Replication: 4 replicates per treatment; 10 worms per container (40 worms per treatment).
- Conditions: 20 ± 1 °C, in the dark.
- Duration and measurements:
  - Day 0 and Day 28: survival and body weight recorded.
  - Day 28: number of egg cocoons produced quantified.
  - Post-28 days: containers incubated for a further 28 days to quantify juveniles (number and mass).

## Data content and variables
- File: Teabags_worm_ecotoxicology.csv
- Key variables (columns):
  - Test_material: Teabag or control group.
  - Treatment: Unique identifier combining teabag brand and concentration.
  - n_teabags: Equivalent number of teabags worms were exposed to (0.5, 1, or 2 per replicate).
  - Teabag_mass_soil: Mass of teabag discs in soil (grams).
  - Teabag_n_soil: Number of teabag discs in soil.
  - Mass_dw_soil: Mass of soil per replicate (grams).
  - Exposure: Exposure duration (days).
  - worms: Number of worms per container.
  - survival: Number surviving after 28 days.
  - survival_percent: Survival percentage after 28 days.
  - worms_mass_start: Mass of the 10 worms at day 0.
  - worms_mass_end: Mass of the 10 worms at day 28.
  - Mass_change: Change in worm mass (grams).
  - n_eggs: Number of egg cocoons produced after 28 days.
  - n_juv: Number of juveniles produced after 28 days.
  - mass_juv: Total mass of juveniles per replicate (grams).
- Ecotoxicological endpoints represented:
  - Mortality (survival, survival_percent)
  - Growth (Mass_change, worms_mass_start, worms_mass_end)
  - Reproduction (n_eggs, n_juv, mass_juv)

## Quality control and provenance
- OECD TG 222 earthworm reproduction test protocol followed.
- Soil and chemical properties: LUFA 2.2 soil characteristics provided (pH ~5.5, organic carbon ~1.66%, nitrogen ~0.19%, CEC ~8.5 meq/100 g).
- Earthworms sourced from Blades Biological; acclimated for ~3 weeks prior to the experiment.
- Data align with the OECD guideline and the associated peer-reviewed publication.

## Data usage and references
- Primary data file: Teabags_worm_ecotoxicology.csv.
- Publication reference: Courtene-Jones et al. 2024, Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment. https://doi.org/10.1016/j.scitotenv.2024.172806
- OECD (2016). OECD TG 222 – Earthworm reproduction test guidelines.

## Potential GIS and map-based applications
- Although generated in a controlled lab setting, the data can inform spatial hazard assessments when integrated with site-level soil properties and land-use data.
- Visualization possibilities:
  - Map endpoints (mortality, growth, reproduction) by teabag brand and concentration.
  - Compare toxicity responses across treatments to support risk communication in map-based dashboards.
- Use cases:
  - Sub-lethal toxicity mapping for risk assessment of biobased teabags in soils with varying properties.
  - Integrating lab-derived ecotoxicology endpoints into spatial decision-support tools for policy and stakeholder engagement.

## Limitations and considerations
- Dataset reflects laboratory conditions with a single soil type and controlled environment; field-relevant variability may differ.
- Four concentrations and three teabag brands only; broader environmental conditions could influence outcomes.