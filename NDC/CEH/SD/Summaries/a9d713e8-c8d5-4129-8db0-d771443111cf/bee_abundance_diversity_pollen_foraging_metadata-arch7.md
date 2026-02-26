# Providing foraging resources for solitary bees on farmland: current schemes for pollinators benefit a limited suite of species

- Purpose of the metadata: describe datasets on bee abundance/diversity and pollen foraging from English farms; detail study design, sampling methods, pollen analysis, data files, and statistical analyses to support GIS-based interpretation and mapping.

## Study area and sampling design

- Location: Nine Higher Level Stewardship (HLS) farms and ten Entry Level Stewardship (ELS) farms in Hampshire and West Sussex, UK.
- Management contrast:
  - HLS: flower-rich pollinator schemes covering ~2.17% of farm area (average 5.56 ha) for at least three years.
  - ELS: control group with limited uptake of flower-rich schemes; seeds present but not managed as pollinator-focused.
- Farm types: predominantly arable or mixed arable/dairy; major crops include wheat, barley, oilseed rape, and grassland.
- Plant materials: pollinator-focused seed mixes typically contain 15–30 flowering forb species; some additional species occasionally included but not characterized as sown in this study.
- Sown vs wild: species in pollinator-friendly schemes treated as 'sown' for comparison, even when found growing wild; full species lists in Appendix S1.
- Habitat surveys: HLS farms surveyed across pollinator schemes plus non-agricultural margins, hedgerows, and woodland edges; ELS farms surveyed in non-agricultural margins and hedgerows/woodland edges only.
- Transect/area metrics: standard 3 km transects; average 1496 ± 148 m of flower-rich habitat per farm; ~3.77 ± 0.24 discrete habitat patches per farm.

## Bee and floristic surveys

- 2013–2014 surveys:
  - Standardized 3 km transects per farm; habitat-specific sections.
  - 16 farms surveyed in 2013; 17 farms in 2014.
  - Bee activity recorded within 2 m of the recorder; field identifications to species; some specimens netted for later ID.
  - Flora: first flowering plant visited and purpose (pollen or nectar) recorded; number of flowering plant species and units within 2 m of recorder estimated per section.
  - Exclusions: grasses, sedges, rushes not recorded.
  - Sampling blocks referred to as “sampling rounds.”
- 2015 surveys:
  - Fixed sampling: 3 hours per farm, with habitat-specific time splits (HLS: 1 h pollinator schemes, 1 h non-agricultural grass, 1 h hedgerow/woodland edge); ELS: similar but without pollinator schemes.
  - All bees within 2 m identified to species; solitary bees with pollen visible on body collected for pollen analysis.
  - Pollen reference library built; pollen from observed plant species collected for reference.
  - Time of day/weather: surveys 09:30–17:00 (32–60°F thresholds or equivalents), no surveys in rain.

## Pollen identification and weighting

- 2015 pollen loads analyzed via light microscopy following Westrich and Schmidt (1986).
- Load estimation: total load relative to species-specific full load (8/8 to 1/8); pollen removed from scopae and mounted on slides.
- Proportional weighting: proportions by volume estimated along three random lines at 400x; less than 1% of load excluded as potential contamination.
- Weight assignment: final weight proportional to load size (e.g., 50:50 split yields weights of 50 each for two species).
- Identification: pollen identified to species when possible; otherwise to genus (e.g., Brassica, Plantago, Geranium).
- Reference materials: Sawyer (1981) and project-based reference collection.
- Appendix S3 lists taxa and level of identification.

## Data and variables (CSV metadata)

- 2013_2014_floral_abundance_data.csv
  - Farm, Type (ELS/HLS), Round, Year, Species, Nature (wild or sown), Abundance (flowering units)
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

## Statistical analysis

- Approach: Generalised Linear Mixed-Effects Models (GLMMs) to test effects of management type on bee/plant abundance and diversity; relationships between plant richness and bee richness/diet breadth.
- Model details:
  - Software: R (v3.1.1) with lme4
  - Error structures: Poisson and negative binomial, with overdispersion checks; negative binomial chosen when appropriate.
  - Fixed effects: management type (HLS vs ELS)
  - Random effects: sampling year; other random factors as applicable
- Analyses by dataset and year:
  - 2013–2014: bee and plant abundance
  - 2013–2015: bee and plant richness
  - 2015: pollen load analyses
  - Seven common polylectic bee species with substantial pollen load data
- Proportion and relationship analyses:
  - Spearman correlations between proportion of sown flowers and visitation/ pollen visits
  - Binomial tests for pollen-type proportions (sown vs wild; Brassica largely from crops)
- Considerations:
  - Brassica pollen largely from crop sources; excluded from sown vs wild comparisons
  - Non-integer pollen-load data handled via proportional weight calculations

## Notes and acknowledgments

- Weather, timing, and single-observer consistency noted as important to minimize bias.
- Funding: Natural Environment Research Council (NE/J016802/1); Game and Wildlife Conservation Trust.
- References and related methodologies cited throughout for context and reproducibility.

## Implications for GIS and data use

- Datasets enable spatial analyses of pollinator resources across farmed landscapes:
  - Spatial distribution of HLS pollinator schemes vs surrounding habitats
  - Relationship between flower-rich habitat extents and bee diversity/foraging patterns
  - Temporal changes across 2013–2015 at farm and habitat patch levels
- Data can be mapped by:
  - Farm identifiers, habitat types, and pollinator scheme status
  - Bee species distributions, floral abundance/richness, and pollen-foraging patterns
  - Pollen load composition linked to specific plant species and plant types (sown, wild, crop)