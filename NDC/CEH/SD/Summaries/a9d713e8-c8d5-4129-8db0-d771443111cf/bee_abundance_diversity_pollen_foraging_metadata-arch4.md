# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

## Overview
- Assesses whether pollinator-focused agri-environment schemes on farmland increase bee resources, comparing Higher Level Stewardship (HLS) with non-sown habitats to Entry Level Stewardship (ELS) controls.
- Focuses on solitary bees and pollen foraging, including floral resource availability (sown vs wild) and pollen loads collected by bees.
- Data span 2013–2015 across farms in Hampshire and West Sussex, UK; aims to contrast management types and to understand data arising from long-term pollinator-focused schemes.

## Study Area and Experimental Design
- Farms: 9 HLS and 10 ELS farms in Hampshire and West Sussex; majority arable or arable/dairy systems.
- Management contrast: HLS farms had substantial pollinator-focused flower-rich schemes (average about 5.56 ha, ~2.17% of farm area) maintained for at least three years; ELS farms served as controls with limited or no flower-rich management.
- Seed mixes: Typically 15–30 flowering forb species; some additional species included, but not all represented in the study area.
- Sown vs wild: Plant species within pollinator schemes treated as 'sown' for comparison, even when present in wild plant communities to enable consistent pollen/resource interpretation.

## Data Collection and Field Methods
- Bee and floristic surveys conducted over 2013–2015 using standardized transects:
  - 3 km transects per farm traversing major habitat types; HLS included pollinator schemes, non-agricultural margins, hedgerows/woodland edges; ELS surveys focused on margins and hedgerows/edges only.
  - Sampling rounds: 2013 (3 rounds), 2014 (3 rounds), 2015 (4 rounds with fixed time periods).
  - Bee data: species-level identification within 2 m of surveyor; first flowering plant visited and purpose (pollen/nectar) recorded.
  - Floristic data: flowering plant species within 2 m recorded; grasses/sedges/rushes excluded.
- Temporal coverage and consistency:
  - 2013–2014 transects measured pollen and floral abundance; 2015 introduced fixed sampling times to standardize effort.
  - Surveys conducted under specific weather conditions and times to optimize bee activity.
- Pollen foraging data (2015):
  - Solitary bees collected to analyze pollen loads; pollen reference library built for identification.
  - Pollen loads processed on microscope slides, with proportions of pollen by species estimated by volume across three lines on slides.
  - Pollen identification relied on established keys and a project-specific reference collection.

## Pollen Identification and Analysis
- Method: Light microscopy following Westrich and Schmidt (1986) for pollen loads; proportion by volume estimated to reflect pollen use.
- Load correction: Proportions adjusted for overall load size to produce final weights per species.
- Taxonomic resolution: Majority identified to species; some taxa identified to genus (e.g., Brassica, Plantago, Geranium).
- Contaminant handling: Species <1% of load excluded from analysis.
- Data sources: Pollen identifications supported by Appendix S3 and a pollen reference library.

## Data Processing and Statistical Analysis
- Modelling approach:
  - Generalised Linear Mixed-Effect Models (GLMMs) using R (v3.1.1) and lme4; distributions included Poisson and negative binomial, with negative binomial preferred to avoid overdispersion.
  - Fixed effects: farm management type (HLS vs ELS); random effects: sampling year (and year-specific methods).
  - Analyses covered: bee and plant abundance, plant species richness, bee species richness (including specific groups), and pollen load diversity.
- Specific analyses:
  - Effects of management type on total bee/plant abundance and richness.
  - Relationships between plant species richness and bee diversity/diet breadth.
  - Relationship between plant richness and pollen species detected in bee loads, including seven common polylectic species.
  - Proportion analyses: proportion of sown vs wild flowers; correlation of sown-flower proportion with pollen visitation metrics (Spearman's tests).
  - Pollen type proportions (sown, wild, crop) examined via binomial tests; Brassica pollen from crops excluded from sown vs wild comparisons.
- Data integration: Multiple datasets (2013–2015) used to derive relationships between floral resources, bee visitation, and pollen foraging.

## Data Files and Metadata
- Data files included (2013–2015; supplemented by 2015 pollen-load data):
  - 2013_2014_floral_abundance_data.csv: Farm, Type, Round, Year, Species, Nature (wild/sown)
  - 2013_2015_floral_richness_data.csv: Farm, Type, Round, Year, Species
  - 2013_2014_bee_abundance_data.csv: Farm, Type, Round, Date, Species, Number
  - 2013_2015_bee_richness_data.csv: Farm, Type, Round, Date, Species
  - 2013_2015_flower_visitation_data.csv: Farm, Type, Round, Date, Species (bee), Number, Caste, Visiting, Status, Purpose, Family
  - 2015_pollen_load_data.csv: Farm, Type, Round, Date, Species, Load, Netted on, Plant pollen, Status, Proportion, Weight
- Metadata notes:
  - Clear definitions for fields such as Nature (wild/sown), Status (wild/sown/crop), and Purpose (pollen/nectar).
  - Pollen load data include proportional weights to reflect pollen volumes and a reference for plant taxa (Appendices S2 and S3).
- Data provenance: Survey methods and analyses align with published supporting information; dataset descriptions reference Appendix S1–S3 and associated methodological notes.

## Data Quality, Limitations, and Considerations
- Consistency and bias:
  - All surveys conducted by a single observer to minimize recorder bias; however, this may affect generalizability.
  Potential biases in pollen use estimates due to easily observable flowers and 2015 time-limited sampling.
- Taxonomic resolution:
  - Some pollen identifications limited to genus level, which may affect fine-scale interpretation of forage preferences.
- Crop pollen:
  - Brassica (oilseed rape) pollen treated as crop-origin and excluded from certain wild vs sown comparisons; acknowledges potential confounding by crop flowering periods.
- Metadata clarity:
  - The study provides extensive metadata and appendices, supporting data discoverability and reuse, but users should consult Appendices S1–S3 for full taxa lists and method specifics.

## Implications for Data Leadership and Data Management
- Data system design:
  - Demonstrates integration of ecological survey data, species-level identifications, and pollen-load analyses across multi-year farm trials.
  - Requires careful data governance for linking management type, habitat types, floral resources, bee communities, and pollen foraging.
- Metadata and discoverability:
  - Rich metadata with explicit field definitions, data lineage, and supplementary materials enhance discoverability and reuse by policymakers, researchers, and practitioners.
- Data standardization and interoperability:
  - Clear classifications for sown vs wild plants and explicit pollen-load processing steps support reproducibility; standardization of sampling rounds and observational protocols improves cross-study comparability.
- Data quality management:
  - Highlighted need for robust documentation of measurement methods, handling of outliers, and transparent reporting of model assumptions and diagnostics (e.g., overdispersion in GLMMs).
- Actionable insights for data strategy:
  - Emphasizes the value of longitudinal, multi-farm datasets to evaluate policy-like interventions (agri-environment schemes) and their ecological outcomes.
  - Demonstrates the importance of combining observational floral data with direct foraging measurements (pollen loads) to understand pollinator resource use.