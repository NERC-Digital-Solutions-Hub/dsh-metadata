# Species Traits and derivation of hairiness of oilseed rape pollinators

## Overview
- Describes functional effect traits for 57 taxonomic units (species, genus, or family level) of oilseed rape insect pollinators.
- Data used to assess links between pollinator traits and oilseed rape yield, in support of the related Nature Communications 2019 paper.

## Dataset scope and taxonomic resolution
- Taxonomic units include Hymenoptera, Diptera, and Lepidoptera; for some groups, identification was at genus or functional level due to unreliable species-level data.
- Functional-type aggregates used for taxonomically complex groups; butterflies largely represented by Pieris spp.
- Some taxa (e.g., coleopteran and parasitic Hymenoptera) were excluded from analyses due to variable taxonomic resolution.

## Pollinator effect traits (15 total)
- Trait 1: Body length (related to body size and inter-tegular distance in bees).
- Traits 2–6: Behavioral interactions with oilseed rape flowers (time spent on flowers, pollen foraging, dry pollen on bodies, etc.).
- Trait 7: Hairiness index (overall body hairiness affecting pollen deposition and possible pollination cues).
- Traits 8–14: Morphological characteristics affecting pollen retention (corbiculae and scopa presence in various body regions; pollen-carried in crop; mouthpart structure).
- Trait 15: Mouthpart category (short, medium, long tongues; separate category for chewing mouthparts).
- Note: Traits 8–15 focus on bees but have cross-taxon relevance for non-bee pollinators.

## Hairiness index: derivation and use
- Hairiness index reflects pollen deposition capability; scores body parts likely to contact stigmas: head, thorax (sternum), abdomen underside, femora, tibiae, and metatarsus (legs assessed separately for each leg).
- Scoring system (0–2 per body part): 0 = coarse setae/extremely short hairs; 1 = short but dense hairs; 2 = long dense hairs.
- Index calculation: sum across 12 body parts, expressed as a proportion of the maximum score (24), yielding a value from 0 to 1.
- Used to infer pollen transfer efficiency and potential pollination cues.

## Metadata and data files
- Metadata file: Woodcock et al 2019 Species functional traits.csv
  - Per-species (or group) records with taxonomic fields (Order, Family, Species) and trait values.
  - Traits include: Mean_time_on_flower, Nectar_foraging, Pollen_foraging, Stigmal_contact, Dry_pollen, Mouthpart, Pollen_carried_only_in_crop, Strict_tibia_corbicula, Propodeal_corbicula, Abdominal_corbicula, Femoral_corbiculae, Basitarsal_scopa, Corbiclula_pollen_moist, with corresponding units and data availability (NA where not available).
  - Data largely derived from Woodcock et al. (2019) with augmentation from unpublished data.
- Metadata file: Woodcock et al 2019 Derivation of hairiness index.csv
  - Details the body-part-specific scores used to compute the hairiness index for each species.
  - Fields include taxonomic identifiers and Hairiness index components (Face, Thorax, Abdomen, Femora, Tibiae, Meta-tibiae in multiple parts) with scores and summed values.
- Metadata file: Woodcock et al 2019 Species functional traits.csv (repeated description for context)
  - Expands on variable descriptions, data types, and provenance notes for each trait, including data origin and handling of missing data.

## Data quality, provenance, and governance considerations
- Provenance: Combines multiple field studies with some unpublished data; explicit attribution to Woodcock et al. (2019) and ASSIST-funded work.
- Provenance notes aid discoverability and reuse by Data Stewards (source, method, and transformation history).
- Data resolution variability (species-level vs. genus/group-level) necessitates careful interpretation and consistent metadata for interoperability.
- Missing data (NA) is present across several traits, which may affect downstream analyses and require appropriate handling.
- The dataset is hosted in a published context (Nature Communications) and should be reused with proper citation and acknowledgment of original authors and funding.

## Practical implications for data stewardship
- Ensure clear metadata standards: taxonomic resolution, trait definitions, units, and NA conventions.
- Maintain linkage between trait data and underlying methodological notes (field methods, identification criteria, and trait scoring rules).
- Document data transformations and aggregation rules used to derive the hairiness index and trait composites.
- Facilitate data discoverability by indexing under pollinator traits, oilseed rape yield, and related meta-analyses; preserve data lineage to support reproducibility.
- Consider licensing and access requirements for unpublished data portions and ensure appropriate attribution when data are reused.

## References
- Related primary paper: Woodcock, B. A. et al. Meta-analysis reveals that pollinator functional diversity and abundance enhance crop pollination and yield. Nature Communications, 2019.
- Supporting references listed within the dataset description (1–14) detailing supporting studies on pollination, pollinator traits, and morphological features.