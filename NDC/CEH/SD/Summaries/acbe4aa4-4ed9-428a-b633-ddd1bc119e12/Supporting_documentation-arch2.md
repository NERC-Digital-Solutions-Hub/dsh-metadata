# Feather isotope ratios and sexing of oystercatchers breeding in Iceland Supporting information for datafiles from NERC Grant: NE/M012549/1: Environmental and demographic drivers of migratory strategies in birds

## Aim and scope
- Document supporting data and methods for analyzing environmental and demographic drivers of migratory strategies in oystercatchers breeding in Iceland.
- Use stable isotope ratios from chest feathers to infer winter diet and habitat, and molecular sexing to determine sex ratios.

## Study design and sampling
- Location and period: Iceland (south, west, north-west, north-east) during summers 2013–2017.
- Field methods: incubating oystercatchers captured on nests with spring traps; birds uniquely marked with metal rings and colour rings.
- Sample collection:
  - Feathers: 4–5 chest feathers grown during the pre-nuptial moult on wintering grounds.
  - Blood: collected for molecular sex determination in a subset of individuals.

## Data files and contents

- OystercatcherFeatherIstotopes.csv
  - 552 individuals sampled during breeding in Iceland.
  - Columns:
    - Year of feather collection (2013–2017)
    - Individual ID (unique ring-based ID)
    - d15N: Nitrogen isotope ratio of each feather
    - d13C: Carbon isotope ratio of each feather
    - Status: Migrant, Unknown, or Resident (based on winter observations)
    - WinterLocation: country where individuals were observed in winter
  - Analytical notes:
    - Feathers washed (2:1 chloroform/methanol), dried, cut into fragments; ~0.45–0.55 mg per sample weighing.
    - Isotopes measured with combustion elemental analyzer and IRMS; δ13C vs VPDB, δ15N vs AIR N2.
    - Internal standard (collagen) indicates measurement errors of 0.2‰ (δ13C) and 0.1‰ (δ15N).

- OystercatcherSexing.csv
  - 321 individuals with molecular sexing data.
  - Columns:
    - Individual ID (unique ring-based ID)
    - DNA-derived sex: sex assigned from molecular analysis
  - Analytical notes:
    - DNA extracted from blood using ammonium acetate protocol; concentration 10–50 ng/μL.
    - Sex determined using Fridolfsson & Ellegren (1999) method.

## Analytical methods and quality assurance
- Isotopic analysis
  - Standardized sample preparation and measurement protocols to ensure comparability.
  - Isotopic values reported as per international standards (δ13C_VPDB, δ15N_AIR N2).
  - Replicate and internal standard usage to quantify precision.
- Molecular sexing
  - Established protocol for avian sexing (Fridolfsson & Ellegren) ensuring consistent sex assignment across individuals.

## Data structure, usage, and monitoring relevance
- Data are organized to enable temporal monitoring of environmental and demographic factors influencing migratory strategies.
- Datasets are suitable for integration with other environmental datasets and for generating outputs (reports, maps, charts) to assess environmental health and policy performance over time.
- Clear data provenance and methods support scrutiny and reuse in monitoring and evaluation efforts.