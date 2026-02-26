# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

## Study design and scope
- Location: Hampshire and West Sussex, UK
- Farm types: Nine Higher Level Stewardship (HLS) farms and ten Entry Level Stewardship (ELS) farms
- Timeframe: Surveys conducted 2013–2015
- Objective: Compare pollinator foraging resources between flower-rich HLS schemes and less-managed ELS farms; assess pollen foraging patterns and plant-bee relationships
- Landscape with major crops: arable or mixed arable/dairy (wheat, barley, oilseed rape, grassland)

## Data collection and survey methods
- Bee and floristic surveys
  - Standardized 3 km transects per farm covering major habitats
  - HLS: pollinator-focused flower-rich schemes plus non-agricultural margins and hedgerow/woodland edges
  - ELS: non-agricultural margins and hedgerow/woodland edges only
  - Sampling rounds: 2013 (three rounds), 2014 (three rounds), 2015 (four rounds with fixed-time protocol)
  - Data collected: bee species observed within 2 m, flowering plant species and flowering units, status of plants (wild, sown, or crop)
  - Plants not recorded: grasses, sedges, rushes; flower counts treated as units
- Bee sampling and pollen collection (2015)
  - Solitary bees collected when pollen visible on bodies; pollen loads from foraging bees recorded
  - Pollen reference library developed; pollen identified to species or genus where necessary
  - Pollen loads adjusted to reflect relative load volume and corrected for species size
  - Brassica (oilseed rape) pollen treated as crop-derived and excluded from sown vs wild comparisons
- Transect execution and conditions
  - Surveys conducted 09:30–17:00 (or until conditions suitable); weather thresholds applied
  - All bee and floristic surveys performed by a single researcher to minimize bias

## Data processing and analysis
- Pollen analysis
  - Pollen proportions estimated along three randomly selected lines per slide
  - Weighting of pollen by proportion and total load size; taxa <1% excluded to reduce contamination risk
- Statistical approach
  - Generalised Linear Mixed-Effect Models (GLMMs) in R (lme4) to test effects of management type and plant richness
  - Model types: Poisson and negative binomial with overdispersion checked
  - Random effects: sampling year and farm
  - Analyses covered: bee and plant abundance and richness; bee richness vs. plant richness; pollen load diversity; proportion of pollen from sown vs wild plants
  - Special analyses: seven most common polylectic bee species; relationship between plant richness and pollen species detected
  - Correlations: Spearman’s rank tests for proportion of sown flowers versus observed pollen visitation and bee visitation to sown flowers
  - Pollen-type comparisons: binomial tests for proportion of pollen from different plant types; Brassica excluded from sown vs wild comparisons
- Data structure and formats
  - Multiple data files with metadata describing fields and meanings; consistent naming across years and data types

## Data files and metadata (contents at a glance)
- 2013_2014_floral_abundance_data.csv
  - Farm, Type, Round, Year, Species, Nature (wild or sown), Abundance
- 2013_2015_floral_richness_data.csv
  - Farm, Type, Round, Year, Species
- 2013_2014_bee_abundance_data.csv
  - Farm, Type, Round, Date, Species, Number
- 2013_2015_bee_richness_data.csv
  - Farm, Type, Round, Date, Species
- 2013_2015_flower_visitation_data.csv
  - Farm, Type, Round, Date, Species, Number, Caste, Visiting, Status, Purpose, Family
- 2015_pollen_load_data.csv
  - Farm, Type, Round, Date, Species, Load, Netted on, Plant pollen, Status, Proportion, Weight
- Metadata and methodological notes
  - Detailed explanations of sampling rounds, plant statuses, and pollen identification methods
  - Appendices S1–S3 referenced for full species lists and identification resolution

## Particular considerations for data users
- Data scope: 2013–2015 field data from southern England arable/dairy farms; focus on foraging resources for solitary bees
- Data coding: sown vs wild classifications applied to seed-mield floral resources; crop pollen (Brassica) treated separately in certain analyses
- Methodology shifts: 2015 used fixed sampling time rather than distance-based transects; implications for cross-year comparability acknowledged
- Data quality and biases: potential biases from differing sampling methods across years; efforts to minimize bias include single-operator data collection and standardized protocols
- Intended use: enabling analysis of how agri-environment schemes influence bee foraging patterns, plant-pollinator interactions, and self-serve data products (e.g., species richness, pollen-source proportions)

## Funding and acknowledgments
- Funded by Natural Environment Research Council (NERC NE/J016802/1) and the Game and Wildlife Conservation Trust