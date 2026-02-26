# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

## Overview
- Lab-based ecotoxicology study to assess sub-lethal effects of Eisenia fetida when exposed to three anonymised bio-based teabags with varying PLA-cellulose blends.
- Endpoints include mortality, growth, and reproduction, following OECD TG 222 Earthworm Reproduction Test protocol.
- Supported by the NERC BIO-PLASTIC-RISK project; data accompany Courtene-Jones et al. (2024) in Science of the Total Environment.
- Data file: Teabags_worm_ecotoxicology.csv.

## Experimental design and data generation
- Test materials: three anonymised teabag brands (TBagA, TBagB, TBagC) with different PLA-cellulose blends.
- Concentrations: four exposure levels (0, 0.02%, 0.04%, 0.07%) added to 500 g LUFA 2.2 sandy-loam soil.
- Organisms and setup: Eisenia fetida adults, 4 replicates per treatment, 10 worms per container (40 worms per treatment), incubated at 20 ± 1 °C in the dark.
- Duration and measurements: survival and body weight at day 0 and day 28; after 28 days, cocoons counted and containers incubated for an additional 28 days to quantify juveniles and their mass.
- Ecotoxicological measures reported: mortality, growth (mass change), reproduction (egg cocoons, number of juveniles, mass of juveniles).

## Data structure and variables
- Datafile: Teabags_worm_ecotoxicology.csv.
- Key variables (described in Table 1 of the dataset):
  - Test_material, Description
  - Treatment, Description (teabag name and concentration)
  - n_teabags (equivalent teabag exposure per container)
  - Teabag_mass_soil (g teabag discs in soil)
  - Teabag_n_soil (number of teabags in soil)
  - Mass_dw_soil (g soil per replicate)
  - Exposure (days)
  - worms (count per container)
  - survival, survival_percent
  - worms_mass_start, worms_mass_end
  - Mass_change (g)
  - n_eggs, n_juv, mass_juv (egg cocoons, juveniles, juvenile mass)

## Quality control and provenance
- Protocol adherence: OECD TG 222 Earthworm Reproduction Test followed.
- Soil: LUFA 2.2 standard sandy-loam soil; pH 5.5 ± 0.1; organic carbon 1.66 ± 0.6%; nitrogen 0.19 ± 0.06%; CEC 8.5 ± 1.8 meq/100 g.
- Biological material: Eisenia fetida sourced from Blades Biological; acclimated 3 weeks prior to experimentation.

## Context and data availability
- Linked publication: Courtene-Jones et al. (2024) Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment. DOI: 10.1016/j.scitotenv.2024.172806
- Funding: NERC BIO-PLASTIC-RISK project (grants NE/V007556/1 and NE/V007246/1).

## Relevance for monitoring frameworks
- Demonstrates a standardized end-to-end process for evaluating environmental health risks of bio-based materials in soil ecosystems.
- Provides explicit measurement endpoints and a detailed metadata structure, facilitating data sharing, comparability, and governance.
- Useful for informing monitoring strategies on soil invertebrate responses to emerging polymer technologies and guiding future data collection standards.

## Considerations for implementation in monitoring
- Anonymised materials and controlled laboratory conditions limit direct field extrapolation; emphasize standardized protocols to enable cross-study comparisons.
- Data sharing and metadata completeness are central to enabling reuse across monitoring programs; the dataset includes explicit variable descriptions and units.