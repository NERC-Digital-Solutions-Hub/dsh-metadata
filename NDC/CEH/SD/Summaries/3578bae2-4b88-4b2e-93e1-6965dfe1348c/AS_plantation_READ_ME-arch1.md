# Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama

## Overview
- Dataset on nitrogen fixation, phosphatase activity, plant nitrogen and phosphorus demand, and soil nitrogen and phosphorus availability for 97 nitrogen-fixing and non-fixing trees from seven species.
- Planted at the Agua Salud Native Species Plantation, El Giral, Panama (coordinates provided).
- Collected by Smithsonian Tropical Research Institute and Princeton University; analyzed by the University of Leeds to test two hypotheses about plant investment in nitrogen fixation and phosphatase activity: nutrient trading and nutrient balance.
- Related to Batterman et al. 2018 Ecology Letters; dataset accompanies a metadata file with the dataset key for descriptions of site characteristics and methods.

## Data structure and contents
- One CSV file with 13 columns and 98 rows; missing values indicated as NA.
- Each row represents a tree; measurements include:
  - Nitrogen fixation metrics (nodule biomass, fixation rates, and 15N-based measures for nitrogen fixed relative to controls).
  - Phosphatase activity in fine root samples.
  - Soil ammonium, nitrate, and Bray-extractable phosphorus.
  - Tissue biomass estimates for leaves, branches, and stem derived from basal diameter via allometric equations.
  - Plant nitrogen and phosphorus demand derived from tissue biomass and literature-based elemental contents.
- Site and method metadata referenced in Batterman et al. 2018; basal diameter from 2009 used to estimate growth to 2011.

## Sampling design and field methods
- Trees planted ~3 meters apart in plots across a sloped landscape; establishment began in 2008.
- One-time fertilization with N-P-K; vegetation cleared by hand annually to reduce competition.
- Data collection occurred August–September 2011 (wet season).
- Phosphatase sampling: 5 fine root samples per tree; activity expressed per dry root biomass; samples analyzed within two weeks of collection.
- Soil sampling at the base of each tree for nitrate, ammonium, and Bray-extractable phosphorus.

## Nitrogen fixation measurements
- Three approaches:
  1) Nodule biomass measured from six 5.5 cm cores near each tree.
  2) Acetylene reduction assay on nodules to estimate fixation rate.
  3) Isotope labeling with 15N and mass spectrometry to determine nitrogen fixed relative to non-enriched controls.
- Results expressed as nodule biomass and nitrogen fixation rate per rooting zone.

## Data usage and interpretation
- Metadata file provides a key to the dataset; full site characteristics and methods described in Batterman et al. 2018 Ecology Letters.
- Primary aim: test nutrient trading and nutrient balance hypotheses; findings indicate that phosphatase activity and nitrogen fixation reflect species differences rather than the hypothesized trading or balance mechanisms.
- When using the dataset, cite: Batterman, S.A. et al. 2018 (Dataset: Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama).

## Practical considerations for analysts
- 98 trees with 13 variables; some data presented as NA where not measured.
- Requires linking soil and plant measurements with species and site context; appropriate for plantation-scale tropical rainforest analyses.
- Suitable for correlational and comparative analyses of nitrogen fixation, phosphatase activity, nutrient demand, and soil nutrient availability, with attention to scale and seasonality.

## Funding and citation
- Funded by multiple foundations and institutions (listed in dataset).
- Citation guidance: Batterman, S.A., Hall, J.S., Turner, B., Hedin, L.O., LaHaela Walter, J.K., Sheldon, P., and van Breugel, M. 2018. Dataset: Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama.