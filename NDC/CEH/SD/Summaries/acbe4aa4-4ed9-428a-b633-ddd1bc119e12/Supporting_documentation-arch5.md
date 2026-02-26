# Feather isotope ratios and sexing of oystercatchers breeding in Iceland

## Overview
- Study location and period: oystercatchers breeding in Iceland (south, west, north-west, north-east) during summers 2013–2017.
- Objectives: analyse stable carbon and nitrogen isotopes in chest feathers to infer diet/habitat during the winter moult; determine molecular sex for a subset of individuals.
- Data products: two CSV datafiles containing isotope and sex data linked by a unique Individual ID.

## Study design and sampling
- Capture method: incubating oystercatchers captured on nests using a spring trap; birds uniquely ringed with metal and colour rings.
- Sampling per individual: 4–5 chest feathers grown during the wintering period; subset also sampled for blood for molecular sexing.
- Rationale for feather isotopes: reflects diet/habitat during the pre-nuptial moult (wintering grounds).

## Data files and variables
- OystercatcherFeatherIstotopes.csv
  - Includes data for 552 individuals.
  - Columns: Year (2013–2017), Individual ID, d15N (‰), d13C (‰), Status (Migrants, Unknown, or Resident), WinterLocation (country of winter observations).
- OystercatcherSexing.csv
  - Includes data for 321 individuals.
  - Columns: Individual ID, DNA-derived sex.

## Isotope analysis methodology
- Sample preparation: feathers washed in 2:1 chloroform/methanol, air-dried, cut into fragments; weighed 0.45–0.55 mg per sample.
- Instrumentation: combustion elemental analyser coupled to a Thermo Scientific Delta XP IRMS via Conflo III.
- Isotopes reported as δ values relative to standards: δ13C (V-PDB), δ15N (AIR N2).
- Quality control: internal laboratory standard (collagen) used; replication indicates measurement errors of 0.2‰ (δ13C) and 0.1‰ (δ15N).

## Molecular sexing methodology
- DNA extraction: from blood using ammonium acetate method; working concentration 10–50 ng/μL.
- Sexing method: Fridolfsson & Ellegren (1999) universal molecular sexing approach for birds.
- Sex data provided in OystercatcherSexing.csv as DNA-derived sex.

## Data quality, provenance, and governance
- Data linkage: both files use a unique Individual ID to enable cross-file integration.
- Documentation of methods: detailed lab protocols, isotope reference standards, and measurement error metrics are provided to support reuse and reproducibility.
- Potential data considerations for stewardship:
  - Ensure integrity of linkage across files via Individual ID.
  - Maintain clear versioning and documentation of any reprocessing or reannotation.
  - Verify unit consistency for isotope values (‰) and keep notes on reference standards used.
  - Be mindful of interpretation of “Status” and “WinterLocation,” which derive from field observations and may have some uncertainty.
- Data sharing and updates: described as supporting information for datafiles from the NERC grant NE/M012549/1; plan to upload and catalogue in appropriate data portals with proper metadata and citation.