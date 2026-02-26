# Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama

## Overview
- Dataset on nitrogen fixation, phosphatase activity, plant nitrogen and phosphorus demand, and soil nitrogen and phosphorus availability for seven tree species grown in an experimental plantation in Panama.
- Collected in August–September 2011 during the wet season at the Agua Salud Native Species Plantation, El Giral, Panama (coordinates provided).
- Purpose: support testing of two hypotheses about plant investment in nitrogen fixation and phosphatase activity (nutrient trading vs nutrient balance).
- Accompanying publication: Batterman et al. 2018 (Ecology Letters) describing overall questions, site characteristics, methods, and a metadata file; dataset cited within the context of that work.

## Dataset structure
- Format: one CSV file.
- Size: 13 columns and 98 rows (one row per tree; some values may be NA if not measured).
- Includes a metadata file with the key to the dataset.

## Study context and sampling design
- Trees planted ~2008 at ~3 m spacing on sloped terrain; plots fertilized once with N-P-K and allowed to grow with annual vegetation clearance.
- Measurements conducted on each tree within two weeks of sampling; roots located from the trunk; phosphatase activity measured on five fine root samples.
- Soils sampled at the base of each tree for nitrate, ammonium, and Bray-extractable phosphorus.
- Plant growth and nutrient demand estimated by converting basal diameter to tissue-specific biomass using species/site-specific allometric equations; then converting biomass growth to nitrogen and phosphorus demand using literature N and P contents for leaves and wood.

## Nitrogen fixation assessment methods
- Three complementary approaches:
  1) Nodule biomass from six 5.5 cm soil cores near the tree base, examined for nodules.
  2) Acetylene reduction assay on nodules excavated from fine roots to measure fixation rates.
  3) Isotopic method on a subset: nodules incubated with labeled 15N to determine nitrogen fixed relative to controls, analyzed by isotope ratio mass spectrometry.
- Data are expressed as nodule biomass and nitrogen fixation rate per area of rooting zone.

## Variables and data processing
- Phosphatase activity data for fine roots (per root biomass basis).
- Soil nitrogen (nitrate, ammonium) and phosphorus (Bray-extractable P) at the base of each tree.
- Nitrogen fixation metrics (nodule biomass, fixation rate, isotope-derived fixation) and the scale-adjusted fixation metrics.
- Plant N and P demand derived from tissue-specific biomass (leaves, branches, stems) using literature-based N and P contents.
- Growth in biomass between 2009 and 2011 estimated from basal diameter measurements (with 2009 diameter as the starting point).

## Hypotheses and conclusions
- Aimed to test:
  - Nutrient trading hypothesis (investment in fixation/phosphatase as a trade-off with nutrient availability).
  - Nutrient balance hypothesis (investment driven by overall nutrient balance).
- The associated Ecology Letters paper reports that phosphatase activity and nitrogen fixation reflect species differences rather than supporting nutrient trading or nutrient balance across tropical rainforest trees.

## Data provenance and funding
- Collected by Smithsonian Tropical Research Institute and Princeton University; analyzed by University of Leeds.
- Funding and support from multiple sources, including ForestGEO, Heising-Simons Foundation, HSBC, Stanley Motta, Small World Institute Fund, Smithsonian grants and fellowships, NSF (EAR-1360391), National University of Singapore, Yale-NUS College, Princeton programs, and related initiatives.

## Usage guidance and citation
- When using the dataset, cite:
  Batterman, S.A., Hall, J.S., Turner, B., Hedin, L.O., LaHaela Walter, J.K., Sheldon, P., and van Breugel, M. 2018. Dataset: Nitrogen fixation and phosphatase activity of 97 nitrogen-fixing and non-fixing trees in Panama.
- The dataset accompanies the Batterman et al. (2018) Ecology Letters article, which provides description of site characteristics, methods, and a metadata file with the dataset key.