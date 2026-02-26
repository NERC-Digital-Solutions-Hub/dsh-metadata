# Species Traits and derivation of hairiness of oilseed rape pollinators

## Overview
- Describes functional effect traits derived for 57 taxonomic units (species, genus, and family level) of oilseed rape insect pollinators.
- Used to assess links between pollinator functional characteristics and oilseed rape yield (in Woodcock et al. 2019, Nature Communications).

## Data content and taxonomic scope
- Taxonomic resolution: species, genus, and family-level classifications; some taxa excluded due to limited taxonomic resolution in the source studies.
- Taxa groups: Hymenoptera (e.g., Apoidea, Vespidae, Tenthredinidae), Diptera (primarily Syrphidae), Lepidoptera (largely Pieris spp. as a functional group).
- Data sources: field studies 1–8 and unpublished data; where species-level identifications were unreliable, genus or functional-group aggregates were used.
- Trait scope: 15 effect (functional) traits derived to influence pollen transfer efficiency to oilseed rape stigmas.
- Trait types include body size, flower-foraging behaviors, pollen handling, and pollen-carrying morphology; several traits are cross-taxon (relevant to bees and non-bee pollinators).

## Pollinator effect traits (15 traits)
- Trait 1: Body length (body size; related metrics like inter-tegular distance in bees).
- Traits 2–6: Behavioral interactions with oilseed rape flowers (e.g., time spent on flowers, pollen foraging, dry pollen on bodies).
- Trait 7: Hairiness index (overall body hairiness affecting pollen deposition).
- Traits 8–14: Morphological characteristics affecting pollen retention (e.g., presence of corbicula and scopa).
- Trait 15: Mouthpart structure (tongue length: long, medium, short; plus a category for chewing mouthparts).
- Traits 8–15 are focused on bees but have cross-taxon relevance due to shared pollen-transfer processes.

## Hairiness index (derivation and interpretation)
- Hairiness index reflects pollen deposition potential and, in bees, responsiveness to flower cues.
- Scoring for each body part likely to contact stigmas: head, thorax, sternum, abdomen underside, femora, tibiae, metatarsus (legs 1–3 assessed separately).
- Scoring scale for each part: 0 = coarse setae/extremely short hairs; 1 = short but dense hairs; 2 = long and dense hairs.
- Per-species score: sum across 12 body parts, expressed as a proportion of the maximum score (24) to yield a hairiness index between 0 and 1.

## Data structure and metadata
- Meta data files included:
  - "Species functional traits.csv": taxon, trait values (e.g., body length, mean_time_on_flower, nectar_foraging, pollen_foraging, stigmal_contact, dry_pollen, mouthpart, pollen_carried_only_in_crop, strict_tibia_corbicula, propodeal_corbicula, abdominal_corbicula, femoral_corbiculae, basitarsal_scopa, corbiclula_pollen_moist) with specified data types and units.
  - "Derivation of hairiness index.csv": per-species body-part scores, summed scores, and hairiness index details.
  - "Hairiness index.csv": per-species hairiness index and scores for each body part (12 parts) with descriptive field definitions.
- Units and data types:
  - Lengths in millimeters (mm); time on flower in seconds; probabilities/foraging probabilities in 0–1 ranges; mouthpart is categorical (long/medium/short or chewing).
  - NA values used where data are not available.
- Taxonomic fields:
  - Order, Family, Species (Unit) with corresponding descriptions and categories.

## Provenance and usage
- Trait data derived from direct behavioral observations on oilseed rape flowers (for species-level data) and supplemented with unpublished observations.
- Used in the referenced meta-analysis to link pollinator functional diversity and abundance to crop pollination and yield outcomes.
- Funded by Natural Environment Research Council (NERC) under ASSIST—Achieving Sustainable Agricultural Systems.

## Potential GIS applications
- Map-based visualization of pollinator trait distributions and functional diversity across landscapes, once species distribution or occurrence data are available.
- Integration with environmental covariates to explore spatial patterns in body size, foraging behavior, and pollen-carrying morphology.
- Use of hairiness index and other trait data to model spatially explicit pollen transfer potential and its relation to oilseed rape yield.

## Considerations and limitations for GIS work
- Taxonomic resolution varies; some data are aggregated at genus or functional-group level, which may affect spatial mapping at finer scales.
- Missing data (NA) for several traits across species necessitates careful imputation or uncertainty representation in maps.
- Traits are derived from multiple studies with potential methodological differences; cross-study harmonization is important for reliable map visualizations.
- Data are primarily trait-level and do not include explicit spatial coordinates; integration with occurrence/distribution data is required for geospatial analyses.