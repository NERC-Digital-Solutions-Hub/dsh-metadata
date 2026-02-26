# Species Traits and derivation of hairiness of oilseed rape pollinators

## Overview
- Describes the functional effect traits derived for 57 taxonomic units (species, genus, and family level) of oilseed rape insect pollinators.
- Data used to assess links between pollinator functional characteristics and oilseed rape yield, in support of the associated Nature Communications meta-analysis (2019).

## What the data set includes
- Taxa: Hymenoptera, Diptera, and Lepidoptera identified to species, genus, or functional level; where identification was uncertain, genus or functional group classifications were used.
- Trait types: 15 effect traits categorized as:
  - Body length (size)
  - Behavioral interactions with oilseed rape (e.g., time on flowers, pollen foraging, pollen on bodies)
  - Hairiness index (overall body hairiness)
  - Morphology affecting pollen retention (corbicula and scopa-related traits)
  - Pollen availability (whether pollen carried in crop, etc.)
  - Mouthpart structure (short/medium/long tongues or chewing)
- Data sources: direct field observations, published studies, and unpublished data; where species-level data were missing, species-level means from available observations were used for generic or functional groups.
- Exclusions: some taxa (e.g., certain Coleoptera and parasitic Hymenoptera) were excluded due to limited taxonomic resolution; some taxa were represented as functional groups.

## Hairiness index and trait derivation
- Hairiness index: a species-specific score reflecting contact with stigmas, derived by scoring 12 body parts (head, thorax, sternum, abdomen underside, femora, tibiae, metatarsus; legs assessed separately) on a 0–2 scale:
  - 0 = coarse setae or extremely short hairs
  - 1 = short but dense hairs
  - 2 = long and dense hairs
- Index calculation: scores summed across all body parts and expressed as a proportion of the maximum (24), yielding a 0–1 hairiness index.
- Body parts scored: head, thorax underside, abdomen underside, femora (three positions), tibiae (three positions), and metatarsus.
- Data source for hairiness: metadata files detailing the scoring scheme and per-body-part scores.

## Data provenance and metadata
- Meta data files:
  - Species functional traits.csv: taxonomic associations, derived morphological and behavioural effect traits (e.g., body length, mean_time_on_flower, nectar_foraging, pollen_foraging, stigmal_contact, dry_pollen, mouthpart, pollen_carried_in_crop, various corbicula/scopa traits).
  - Derivation of hairiness index.csv: detailed values used to derive the hairiness index, including per-body-part scores and aggregated indices.
- Data quality notes:
  - Data include both observed values and author-augmented values where necessary.
  - Some traits have missing values (NA) at the species or higher taxonomic levels.
- Taxonomic resolution: variable across records; some taxa described at species level, others at genus or family/functional level.

## Relationship to the wider study
- The traits were used in the 2019 Nature Communications paper by Woodcock et al. to demonstrate that pollinator functional diversity and abundance enhance crop pollination and yield.
- The dataset provides the underlying trait measurements and metadata enabling analyses of how pollinator characteristics influence oilseed rape pollination services.

## Practical considerations for data management and reuse
- User needs and governance:
  - Ensure discoverability and proper metadata documentation to facilitate reuse across networks and with policy colleagues.
  - Maintain clear provenance, definitions, and units for all traits; document any data augmentations or generic classifications used in place of species-level data.
- Data quality and gaps:
  - Acknowledge variability in taxonomic resolution and reliance on unpublished data for some traits.
  - Identify gaps where data are missing (NA) and note needing cautious interpretation or targeted data collection.
- Reusability across contexts:
  - Trait-based approach supports cross-study comparisons and integration with other pollination and yield datasets.
  - Suitable for collaboration across research networks aiming to link pollinator traits to agricultural outcomes and ecosystem services.