# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

## Study area
- Nine Higher Level Stewardship (HLS) farms and ten Entry Level Stewardship (ELS) farms in Hampshire and West Sussex, UK.
- HLS farms had pollinator-focused flower-rich schemes averaging 5.56 ha (2.17% of owned farm area) for at least three years.
- ELS farms served as the control group; basic ELS without pollinator-focused management.
- Seed mixes typically contained 15–30 flowering forb species; occasional inclusion of Hypochaeris radicata and Trifolium repens, though these were not consistently characterized as sown for this study.
- In practice, many sown species occur naturally on farms; to compare pollen choices, species in pollinator schemes were treated as 'sown' even if found wild in the broader flora.
- Farms predominantly arable or mixed arable/dairy with crops such as wheat, barley, oilseed rape, and permanent/silage grassland.

## Bee and floristic surveys
- 2013 and 2014: standardized 3 km transects per farm across major habitats. HLS transects included pollinator-focused schemes, non-agricultural margins, hedgerows, and woodland edges; ELS transects covered margins and hedgerow/woodland edges only.
- Crops and large areas of agricultural grassland not surveyed.
- Transects subdivided into sections by habitat type; HLS farms surveyed to maximize coverage of pollinator schemes (average ≈1496 m of flower-rich habitat across ~3.77 patches per farm).
- Bee activity recorded along transects; bees within 2 m identified to species; field-identified specimens collected for later ID as needed.
- First flowering plant visited and visit purpose (pollen or nectar) recorded. Some Hylaeus visits categorized as general visits due to pollen handling behavior.
- Floral metrics: number of flowering plant species and flowering units within 2 m of recorder estimated per transect section.
- 2013: 16 farms (8 HLS, 8 ELS); 2014: 17 farms (8 HLS, 9 ELS).
- 2013–2014 sampling rounds: three rounds across the season (late May–early August, with a later May/June and June/July window); 2015 used fixed time sampling instead of distance-based transects.
- 2015: 14 farms (7 HLS, 7 ELS); surveys lasted 3 hours per farm with partitioned time across habitats; bees collected for pollen analysis when visible.
- All surveys conducted by the same researcher to minimise observer bias.
- All flowering plant species recorded; abundance not quantified in 2015.

## Pollen identification
- 2015 scopal pollen loads from solitary foraging bees analyzed by light microscopy following Westrich and Schmidt (1986).
- Total pollen load estimated relative to the species’ typical full load (8/8 to 1/8); pollen removed from scopae and identified.
- Proportions of pollen by species estimated along three randomly selected lines; proportions expressed as relative volume, not grain counts, to reflect pollen load composition accurately.
- Species representing <1% of the load excluded from analyses.
- Proportions corrected for overall load size to yield final weights per species.
- Pollen identified to species where possible; otherwise to genus (e.g., Brassica, Plantago, Geranium).
- A pollen reference library was built; full taxonomic lists and identification levels provided in Appendices.

## Statistical analysis
- Generalized Linear Mixed-Effect Models (GLMMs) used to assess:
  - Impact of management type on bee and plant abundance and diversity.
  - Impact of plant species richness on bee species diversity and diet breadth.
- Model fitting: maximum likelihood (Laplace Approximation) in R (v3.1.1) using lme4; both Poisson and negative binomial error structures tested; negative binomial selected to address overdispersion.
- Model comparison via ANOVA against null models with the same random factors.
- Analyses by dataset:
  - Bee and plant abundance/diversity: 2013–2014 data (abundance) and 2013–2015 data (richness).
  - Bee richness and diet breadth vs. plant richness: 2013–2015 data.
  - Pollen load diversity vs. plant richness: 2015 data.
  - Subset analyses for seven common polylectic bee species (n ≈ 30 pollen loads per species) to summarize pollen load diversity.
  - Relationship between plant richness and number of pollen species in loads: mixed-effects with plant richness as fixed factor and bee species as random factor.
- Additional analyses:
  - Proportion of sown vs total flowers and proportion of solitary bee pollen visits to sown flowers; Spearman’s rank correlations due to non-normal data.
  - Binomial tests to compare pollen proportions from sown vs wild plant sources.
  - Handling of Brassica pollen (predominantly crop-derived) by excluding it from sown/wild comparisons where appropriate.
- Data scope:
  - 2013–2014: floral abundance and richness analyses.
  - 2013–2015: bee abundance and richness analyses.
  - 2015: pollen load analyses.

## Datasets and metadata
- Files include:
  - 2013_2014_floral_abundance_data.csv: Farm, Type, Round, Year, Species, Nature, Abundance.
  - 2013_2015_floral_richness_data.csv: Farm, Type, Round, Year, Species.
  - 2013_2014_bee_abundance_data.csv: Farm, Type, Round, Date, Species, Number.
  - 2013_2015_bee_richness_data.csv: Farm, Type, Round, Date, Species.
  - 2013_2015_flower_visitation_data.csv: Farm, Type, Round, Date, Species, Number, Caste, Visiting, Status, Purpose, Family.
  - 2015_pollen_load_data.csv: Farm, Type, Round, Date, Species, Load, Netted on, Plant pollen, Status, Proportion, Weight.
- Metadata explains column meanings, data collection methods, and how to interpret status (wild, sown, crop) and plant status for analyses.

## Acknowledgements
- Funded by Natural Environment Research Council (NE/J016802/1) and the Game and Wildlife Conservation Trust.