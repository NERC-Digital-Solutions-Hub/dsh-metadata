# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

## Overview
- Investigates how pollinator-focused flower-rich schemes on English farmland (HLS) compare to basic environmental stewardship (ELS) in supporting solitary bees and floral resources.
- Aims to inform monitoring frameworks by detailing study design, data collection, and analytical approaches for evaluating policy interventions.

## Study area and management context
- Location: Hampshire and West Sussex, UK.
- Farms: 9 Higher Level Stewardship (HLS) and 10 Entry Level Stewardship (ELS) farms.
- HLS schemes: average of 5.56 ± 0.13 ha of pollinator-focused habitat (about 2.17 ± 0.05% of farm area) present for at least three years.
- ELS farms: served as controls; pollinator-focused schemes were present in some ELS but uptake was low, so basic ELS farms without such management were used for comparison.
- Farm types: predominantly arable or mixed arable/dairy; major crops include wheat, barley, oilseed rape, and grassland.

## Pollinator resources and plant data
- Seed mixes: typically 15–30 flowering forb species; some sites include additional species but not characterized as sown for this study.
- Classification: plant species in pollinator schemes labeled as “sown”; wild plants treated as part of the broader plant community.
- Floristic data: included a list of flowering units and plant species across habitats; grasses, sedges, and rushes excluded from bee observations.

## Bee and floristic surveys (Field methods)
- Years: 2013 and 2014 - standardized 3 km transects per farm through major habitats; 2015 - time-limited surveys with standardized hours.
- Habitats surveyed: HLS farms included pollinator schemes plus non-agricultural margins and hedgerows; ELS farms surveyed only non-agricultural margins and hedgerows (no pollinator schemes).
- Sampling rounds: 2013 (three rounds), 2014 (three rounds), 2015 (four rounds with fixed time blocks).
- Bee identification: all bees within 2 m recorded to species level; Hylaeus noted as foraging for pollen when species-level determination was not possible; netting for later identification.
- Floral observations: first flowering plant visited and purpose of visit (pollen or nectar) recorded; plant species within 2 m counted; plant clusters counted as single units.

## Pollen foraging and pollen load analysis (2015)
- Pollen collection: solitary bees with pollen on bodies were collected and frozen; sampling focused on the pollen loads on scopae.
- Pollen analysis: light microscopy following Westrich and Schmidt (1986); estimate load relative to full load (8/8 scale); proportions by volume calculated along three random lines across the slide.
- Identification: pollen identified to species where possible; otherwise to genus; rare taxa (<1% of load) excluded from detailed analysis to avoid contamination.
- Pollen load processing: proportions corrected for overall load size to yield final weights per species; Brassica pollen (mostly from crops like oilseed rape) treated as crop-derived and excluded from sown vs wild comparisons.
- Pollen dataset: 2015 data used for detailed pollen load analyses; analysis covered seven common polylectic species with substantial sample sizes.

## Data handling and metadata (data management)
- Datasets include multiple CSV files with detailed metadata for reproducibility:
  - floral_abundance_data.csv: farm, type, round, year, species, status (wild or sown).
  - floral_richness_data.csv: farm, type, round, year, species.
  - bee_abundance_data.csv: farm, type, round, date, species, number.
  - bee_richness_data.csv: farm, type, round, date, species.
  - flower_visitation_data.csv: farm, type, round, date, species (bee), visiting plant, status, purpose, family.
  - 2015_pollen_load_data.csv: farm, type, round, date, species, load, netted_on (plant), pollen details, proportion, weight.
- Metadata notes: describes field headings and meanings; provides a structured basis for reanalysis and replication.

## Statistical analysis and modeling (analytical approach)
- Primary methods: Generalised Linear Mixed-Effect Models (GLMMs) in R (lme4 package) with maximum likelihood estimation.
- Error structures: tested Poisson and negative binomial; negative binomial final models due to overdispersion considerations.
- Fixed and random effects:
  - Fixed: management type (HLS vs ELS) to assess differences in bee/plant abundance and diversity.
  - Random: sampling year to account for temporal data structure; date-specific effects in pollen analyses.
- Analyses conducted:
  - Bee and plant abundance and richness by management type (2013–2014 data for abundance; 2013–2015 data for richness).
  - Relationship between plant species richness and bee species richness (including Apis, Bombus, kleptoparastic, and oligolectic bees).
  - Impact of plant species richness on pollen load diversity among bees.
  - Pollen load diversity across seven common polylectic species (aggregated yearly data).
  - Relationship between proportion of sown flowers and bee visitation patterns (Spearman correlations).
  - Proportion of pollen visits to sown vs wild flowers (binomial tests); Brassica pollen excluded from sown vs wild comparison due to crop origin.
- Data interpretation: models assessed significance via ANOVA against null models with the same random structure.

## Key implications for monitoring frameworks
- Demonstrates a comprehensive, policy-relevant monitoring design:
  - Use of standardized transects and sampling rounds across multiple years and farm types to compare management regimes.
  - Integration of biodiversity metrics (bee abundance/diversity) with habitat resource data (floral abundance/richness) and functional evidence (pollen foraging).
  - Inclusion of detailed pollen analysis to link floral resource use with bee foraging behavior.
- Emphasizes data quality and transparency:
  - Clear metadata and Data Availability practices, enabling reproducibility, reanalysis, and potential data sharing within governance constraints.
  - Documentation of methods for sampling, identification, and statistical analyses to support data governance and standardization.
- Highlights practical monitoring considerations:
  - Challenges such as data gaps, data access, and the need for robust metadata to verify data suitability and comparability across schemes.
  - Importance of defining “sown” versus wild resources and accounting for crop-derived pollen in analyses.

## Funding and acknowledgements
- Funded by the Natural Environment Research Council (NE/J016802/1) and the Game and Wildlife Conservation Trust.