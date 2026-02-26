# Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama

## Overview
- A dataset describing nitrogen fixation, phosphatase activity, and plant nutrient demands alongside soil nutrient availability for seven tree species grown in a Panama plantation.
- Data were used to test hypotheses about nutrient trading and nutrient balance in tropical rainforest trees.
- Accompanied by a scholarly article: Batterman et al. 2018 (Ecology Letters).

## What the data contain
- One CSV file with 13 columns and 98 rows (NA indicates missing or unmeasured values).
- Variables cover:
  - Nitrogen fixation measures (via nodules biomass, acetylene reduction, and 15N labeling)
  - Phosphatase activity (measured on five fine root samples per tree)
  - Plant nitrogen and phosphorus demand (derived from tissue biomass and literature N/P contents)
  - Soil nitrogen and Bray-extractable phosphorus availability at the base of each tree
  - Morphometrics used to derive biomass (basal diameter converted to tissue-specific biomass for leaves, branches, and stem)

## Data collection context and design
- Location: Agua Salud Native Species Plantation, El Giral, Panama.
- Plot design: seven species planted around 2008 in ~3 m spacing on sloped terrain; fertilized once with N-P-K; vegetation cleared annually to reduce competition.
- Data collection period: August–September 2011 (wet season).
- Tree-level representation: each row corresponds to a tree; root samples and measurements taken near the trunk base.

## Measurement methods and data structure
- Nitrogen fixation assessment (three approaches):
  1) Nodule biomass from soil cores near the base.
  2) In-nodule acetylene reduction assay for fixation rates.
  3) Isotope labeling with 15N to quantify fixed N relative to controls.
- Phosphatase activity: measured from 5 fine root samples per tree within two weeks of collection and stored cold.
- Soils: sampled at tree bases for nitrate, ammonium, and Bray-extractable phosphorus.
- Biomass and nutrient demand:
  - Basal diameter converted to tissue-specific biomass using site- and species-specific allometric equations.
  - Leaf and wood N and P contents sourced from literature to estimate N and P demand from biomass growth (2009–2011).
- Data provenance: dataset described alongside a published study; metadata file provides the key to the dataset.

## Metadata, provenance, and citation
- Metadata: a metadata file accompanies the dataset (key to data variables and methods).
- Primary publication: Batterman, S.A. et al. 2018. Dataset: Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama.
- Citation guidance: Please cite Batterman et al. 2018 when using the dataset; DOI available in the accompanying Ecology Letters article (10.1111/ele.13129).

## Data quality, limitations, and considerations for use
- Missing values explicitly indicated as NA.
- Data cover seven species in a single plantation over a specific period (2011); derived variables depend on literature values for N/P contents and allometric equations.
- Measurements are snapshots in time and space; variability across species and sites should be considered when comparing results or generalizing.

## Relevance for data strategy and governance (Data Leaders perspective)
- Data asset type: biological/eco-physiological measurements with rich metadata and derived metrics.
- Strengths for data strategy:
  - Clear documentation of measurement methods, processing steps, and derived variables.
  - Comprehensive linkage of plant physiology (nitrogen fixation, phosphatase activity) to soil nutrient availability and plant nutrient demands.
  - Facilitates cross-species comparisons and testing of nutrient cycling hypotheses.
  - Metadata and citation requirements support data discoverability and reuse across networks.
- Considerations for management and reuse:
  - Ensure discoverability of the dataset and metadata file; maintain citation integrity with the Batterman 2018 reference.
  - Assess data quality and applicability to other contexts due to site-specific design and time window.
  - Leverage as a model for future data collection on nutrient fixation and turnover in tropical forests, including governance of data provenance and methodological transparency.