# Ecotoxicology data of Eisenia fetida earthworms exposed to four concentrations of bio-based teabags

- Purpose: Assess sub-lethal ecotoxicity (mortality, growth, reproduction) of Eisenia fetida exposed to three anonymised bio-based teabags with varying PLA-cellulose blends across four concentrations, following OECD TG 222 guidelines.
- Project and funding: BIO-PLASTIC-RISK project; funded by NERC (NE/V007556/1 and NE/V007246/1).
- Data file: Teabags_worm_ecotoxicology.csv
- Related publication: Courtene-Jones et al. (2024); Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms; Science of the Total Environment.

## Data generation and experimental design

- Test materials and concentrations:
  - Brands: TBagA, TBagB, TBagC (different PLA-cellulose blends)
  - Concentrations: 0% (control), 0.02%, 0.04%, 0.07%
- Biological system: Eisenia fetida earthworms
- Soil and environment:
  - Soil: LUFA 2.2 standard sandy-loam soil (Germany), with detailed soil properties provided
  - Temperature: 20 ± 1 °C, dark conditions
- Experimental setup:
  - Replication: 4 replicates per treatment
  - Group size: 10 earthworms per container (40 per treatment)
  - Duration: 28-day exposure; post-exposure incubation for 28 days to assess fecundity
- Measurements:
  - Survival and body weight at days 0 and 28
  - Reproduction: number of egg cocoons, number of juveniles, mass of juveniles

## Dataset structure and variables

- Data file: Teabags_worm_ecotoxicology.csv
- Key variables (described in Table 1 of the dataset):
  - Test_material: Teabag or control group
  - Treatment: Unique identifier combining teabag name and concentration
  - n_teabags: Equivalent number of teabags worms were exposed to (0.5–2 teabags)
  - Teabag_mass_soil: Mass of teabag discs exposed per 500 g soil
  - Teabag_n_soil: Number of teabag discs per 500 g soil
  - Mass_dw_soil: Mass of soil per test replicate
  - Exposure: Exposure duration (days)
  - worms: Number of worms per container
  - survival: Number surviving after 28 days
  - survival_percent: Survival percentage after 28 days
  - worms_mass_start: Mass of the 10 worms at day 0
  - worms_mass_end: Mass of the 10 worms at day 28
  - Mass_change: Change in worm mass
  - n_eggs: Number of egg cocoons produced after 28 days
  - n_juv: Number of juveniles produced after 28 days
  - mass_juv: Total mass of juveniles per replicate
- Data governance notes:
  - All measurements align with OECD TG 222 (2016)
  - Measurements captured for mortality, growth (mass change), and reproduction metrics (eggs, juveniles, juvenile mass)

## Quality control, provenance, and context

- Protocols adhered to: OECD TG 222 Earthworm Reproduction Test (2016)
- Soil and site details:
  - LUFA 2.2 soil: loamy sand; pH 5.5 ± 0.1 (0.01 M CaCl2), organic carbon 1.66 ± 0.6%, nitrogen 0.19 ± 0.06%, CEC 8.5 ± 1.8 meq/100 g
- Biological material:
  - Earthworms purchased from Blades Biological; acclimated for 3 weeks prior to testing
- Documentation and references:
  - Primary related data output cited against Courtene-Jones et al. (2024) in Science of the Total Environment
  - OECD (2016) TG 222 guidelines cited for methodology

## Data governance, sharing, and reuse considerations for Data Stewards

- Standards and interoperability:
  - Dataset adheres to a recognized test guideline (OECD TG 222) and uses clearly defined treatments and measurements
  - CSV format facilitates reuse and integration into data portals and catalogues
- Metadata and discoverability:
  - Include clear mapping of treatment codes to teabag brand and concentration
  - Document soil properties, acclimation details, and replication scheme to support reproducibility
  - Reference associated publication and funding to provide provenance
- Data curation and updates:
  - Maintain versioned records; potential to link to the accompanying research outputs (Courtene-Jones et al., 2024)
  - Include notes on any deviations, data cleaning steps, and quality checks
- Access considerations:
  - Data intended to accompany a research output; ensure appropriate metadata schemas are used to enable discoverability and reuse in data portals
- Usage notes:
  - Suitable for secondary analyses on ecotoxicity endpoints (mortality, growth, reproduction) under bio-based teabag exposure
  - Useful for cross-study comparisons with OECD TG 222 datasets and for assessments of environmental risks of PLA-based teabags

## References

- OECD. (2016). OECD Guideline for the Testing of Chemicals, Technical Guidance 222: Earthworm Reproduction Test (Eisenia fetida/Eisenia andrei). OECD TG 222.
- Courtene-Jones, et al. (2024). Deterioration of bio-based polylactic acid plastic teabags under environmental conditions and their associated effects on earthworms. Science of the Total Environment. DOI: https://doi.org/10.1016/j.scitotenv.2024.172806