# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

## Aim and scope
- Assess how pollinator-focused flower-rich schemes on farmland influence solitary bee foraging and pollen resources.
- Compare Higher Level Stewardship (HLS) with Entry Level Stewardship (ELS) farms in Hampshire and West Sussex, UK.
- Use standardized data to evaluate environmental health and policy performance regarding pollinators.

## Study design and site selection
- Farms: nine HLS and ten ELS farms; HLS had an average of ~5.6 ha of pollinator-focused schemes for at least three years; ELS farms served as controls with minimal to no such management.
- Farm types: predominantly arable or mixed arable/dairy; major crops included wheat, barley, oilseed rape, and grassland.
- Flower-rich schemes typically included seed mixes with 15–30 flowering forb species; sown species were treated as 'sown' for comparison, even when found wild.

## Bee and floristic surveys (2013–2015)
- 3 km standardized transects per farm:
  - 2013–2014: transects passed through all major habitats; HLS farms surveyed for pollinator schemes, non-agricultural margins, hedgerows, and woodland edges; ELS farms surveyed only non-agricultural margins and hedgerows/woodland edges.
  - 2015: fixed-time surveys (3 hours total) with habitat-allocated blocks; HLS included pollinator schemes, non-agricultural margins, and hedgerows/woodland edges.
- Sampling rounds:
  - 2013: three rounds (late May–early June, late June–mid July, early August).
  - 2014: three rounds (late May–late July).
  - 2015: four rounds (April/May, May/June, June/July, July/August).
- Data collection:
  - Bee walks: identify all bees within 2 m of the observer to species; first flower visited and visit purpose (pollen or nectar) recorded.
  - Solitary bees with pollen on the body recorded; Hylaeus noted for pollen handling differences.
  - Floristic surveys: record flowering plant species within 2 m of the observer; abundance not quantified; grasses, sedges, and rushes excluded.
  - Weather and time windows: surveys conducted 09:30–17:00 (temp >13°C, or >17°C with any cloud); no surveys in rain.
- Data consistency: all bee and floristic surveys conducted by the same observer to minimize bias.

## Pollen load collection and analysis (2015)
- Pollen loads from foraging solitary bees collected, stored, and later analyzed microscopically.
- Pollen identification approach:
  - Pollen loads estimated relative to full load (8/8 to 1/8) and converted to final weights reflecting volume proportion of each pollen type.
  - Pollen identified to species when possible (Sawyer 1981); some to genus when necessary.
  - Pollen from taxa representing less than 1% of the load excluded to avoid contamination noise.
  - A pollen reference library was created from sampled plant species.
- Special note: pollen from Brassica crops (e.g., oilseed rape) treated separately, as most such pollen derived from crops rather than wild plants.

## Data handling and datasets
- Data files generated (metadata and outputs):
  - 2013_2014_floral_abundance_data.csv: farm, type, round, year, species, status (wild/sown), abundance.
  - 2013_2015_floral_richness_data.csv: farm, type, round, year, species.
  - 2013_2014_bee_abundance_data.csv: farm, type, round, date, species, number.
  - 2013_2015_bee_richness_data.csv: farm, type, round, date, species.
  - 2013_2015_flower_visitation_data.csv: farm, type, round, date, bee species, number, caste, visiting plant, status, purpose, family.
  - 2015_pollen_load_data.csv: farm, type, round, date, bee species, load, netted on, pollen plant, status, proportion, weight.
- These datasets support analyses of bee abundance/diversity, floral resources, pollinator foraging behavior, and pollen use.

## Statistical analyses and modelling (2013–2015)
- Modelling framework: Generalised Linear Mixed-Effect Models (GLMMs) in R (v3.1.1) using lme4.
- Error structures: Poisson and negative binomial; final models used negative binomial due to overdispersion.
- Fixed and random effects:
  - Fixed: management type (HLS vs ELS) for abundance and richness comparisons; plant richness as a fixed factor for bee richness and oligolectic bee richness.
  - Random: sampling year and farm (to account for temporal structure and repeated measures); for some analyses, sampling round as random factor.
- Analyses included:
  - Differences in total bee and plant species abundance and floral abundance by farm type.
  - Impact of plant species richness on bee species richness (including oligolectic and polylectic bees).
  - Relationship between plant richness and pollen species richness in bee pollen loads.
  - Pollen load analyses for seven common polylectic bee species (across the majority of loads).
  - Relationship between plant richness and pollen richness across bee species.
  - Proportion of sown vs wild flowers and its relation to observed pollen visits and bee species visiting sown flowers (Spearman correlations due to non-normality).
  - Binomial tests for differences in pollen proportions from sown vs wild plant types.
- Data treatment notes:
  - 2013–2014 data used for total bee/plant abundance and 2013–2015 data for richness analyses.
  - 2015 pollen data used for pollen load analyses.
  - Brassica pollen excluded from sown vs wild comparisons to avoid crop-derived bias.

## Considerations for environmental monitoring and policy relevance
- Demonstrates how standardized, long-term monitoring can reveal the extent to which targeted pollinator schemes affect actual foraging resources for solitary bees.
- Highlights challenges in translating seed mixes and flower-rich habitats into measurable changes in bee foraging and pollen diversity.
- Emphasizes the value of combining survey data, floristic richness, and pollen analysis to assess ecosystem health and guide agri-environment scheme design.
- Addresses data accessibility and reusability through clearly defined datasets and metadata, supporting broader monitoring and policy scrutiny.

## Funding and acknowledgements
- Funded by the Natural Environment Research Council (NE/J016802/1) and the Game and Wildlife Conservation Trust.