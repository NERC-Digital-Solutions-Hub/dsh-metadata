# Metadata for: Herbivory rates, species traits and leaf traits across symbiotic nitrogen-fixing and non-fixing species from a Panamanian tropical forest, 2007-2019

## Overview and aim
- A dataset examining herbivory and potential controls on herbivory for nitrogen-fixing and non-fixing trees in a mature Panamanian tropical forest.
- Includes herbivory measures at leaf and seedling levels, plus leaf chemical and physical traits linked to herbivory.
- Data collected primarily in 2017–2018 with supplementary data from 2007–2019.
- Designed to assess whether nitrogen-fixers have higher herbivory and to identify traits driving herbivory.

## Study system and sampling design
- Location: Barro Colorado Island (BCI), Panama, within the 50-ha seedling census plot.
- Species: 23 nitrogen-fixing fixer species and 20 non-fixer species (across 43 species total).
- Sampling frame: Nearly all fixer species present at the site (23/26) and a representative set of non-fixer species across abundance ranges.
- Plot structure: Seedlings from 20 m x 20 m subplots (p5 microplots within each) in the 50-ha plot.
- Temporal scope: Field work during wet seasons of 2017 and 2018; additional data collected 2007–2019.
- Seedling criteria: Freestanding woody seedlings ≥20 cm stem height and <1 cm diameter at 1.3 m.

## Measures of herbivory
- Leaves: Herbivory on mature leaves (up to six leaves per individual; average ~4.9) scanned non-destructively; herbivory quantified via ImageJ by comparing damaged vs. undamaged leaf areas.
- Young leaves: 226 young leaves scanned in November 2017 to capture higher herbivory and turnover.
- Metrics:
  - Incidence of herbivory: binary indicator (any leaf area lost vs. none).
  - Proportion of leaf area lost: continuous measure (0–1).
- Seedlings: Herbivory summarized at the seedling level (proportion of leaves with herbivory and/or proportion of leaf area lost).

## Growth and traits
- Growth rate: relative growth rate calculated as the natural log difference in stem length between 2018 and 2017.
- Species traits at the leaf level:
  - Nutrients: nitrogen, carbon, phosphorus, potassium, calcium concentrations.
  - Physical defenses: cellulose, hemicellulose, lignin, silicon concentrations.
  - Toughness metrics: lamina toughness, vein toughness, lamina density, work to shear, leaf mass per area (LMA).
  - Chemical similarity metrics: measures of leaf secondary metabolite similarity (nnCSCS and mCSCS) based on UHPLC-ESI-MS profiling.
- Sampling for leaf traits: Shade leaves collected from the crown tops of the largest and smallest individuals; stored on ice and oven-dried; values averaged across individuals and light environments.

## Data structure and contents
- Five CSV files:
  - Leaf_herbivory_BCI_2017.csv: leaf-scale herbivory (incidence and proportion).
  - seedling_herbivory_BCI_2017.csv: seedling-scale herbivory (incidence, proportion, and growth rate).
  - herbivory_rate_BCI_2017.csv: herbivory rate on young leaves (incidence, proportion, and differential measures).
  - simulated_species_herbivory.csv: predicted average herbivory at the species scale (probability and proportion).
  - spp_leaf_traits.csv: species-level leaf traits (nutrients, structural traits, and similarity metrics).
- Column themes:
  - spp (species code), fix (fixation status), plot/p5 (spatial identifiers), tag (seedling ID), leaf (leaf identifier), area (leaf area), stem_length, incidence_of_herbivory, proportion_of_herbivory, growth rate, and trait measurements (e.g., n_shad, c_shad, Shade_lignin, mCSCS, nnCSCS).

## Data quality control and processing
- Automated herbivory measurement in ImageJ complemented by manual verification against leaf images.
- Two methodologies for young-leaf herbivory to capture tissue loss and leaf growth:
  - Method 1: difference in leaf area between time points divided by estimated initial leaf area (including lost tissue).
  - Method 2: percentage missing area at time point one vs. time point two for leaves that grew.
- Cross-checks ensure consistency; data handling aligns with the long-term Canopy ISA census framework.

## Analytical approaches and models
- Modeling targets:
  - Incidence of herbivory (binary): logistic regression at the species level.
  - Proportion of leaf area lost (0–1): beta regression at the species level.
- Random effects: plot-level random effects to account for spatial autocorrelation (20 m plots).
- Sample size filter: species with fewer than 10 leaves excluded from incidence modeling to avoid singularities.
- Prediction tools: bootpredictlme4 for binary models; predict for mixed models; glmmTMB for beta regression.
- Software: analyses conducted in R (version 3.5.1) with RStudio.

## Data governance, accessibility, and considerations for monitoring
- Data are comprehensive and structured for reuse in monitoring frameworks; includes clear metadata on data sources, collection methods, and units.
- Metadata and openness enable data governance and transparency but may raise considerations for publicly sharing lineage and trait data.
- Relevance for monitoring:
  - Enables comparison of herbivory pressures between nitrogen-fixers and non-fixers.
  - Links herbivory to leaf traits and chemical similarity, supporting mechanism-based monitoring.
  - Provides growth and seedling turnover context to interpret herbivory impacts on forest dynamics.
- Potential barriers to monitoring integration:
  - Metadata completeness and harmonization with other datasets.
  - Data access controls and ensuring timely availability.
  - Addressing organizational silos and ensuring standardized data governance at source.

## References
- Comita, L. S. et al. Asymmetric density dependence shapes species abundances in a tropical tree community. Science. 2010.
- Westbrook, J. W. et al. What makes a leaf tough? Am. Nat. 2011.
- Sprent, J. I. Legume nodulation: a global perspective. Wiley, 2009.
- R Core Development Team. R—A Language and Environment for Statistical Computing. 2018.