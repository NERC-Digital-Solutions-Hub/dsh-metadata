# Species Traits and derivation of hairiness of oilseed rape pollinators

## Purpose and usage
- Describes functional effect traits derived for 57 taxonomic units (species, genus, and family level) of oilseed rape insect pollinators.
- Data used to assess links between pollinator functional characteristics and oilseed rape yield, as part of the meta-analysis reported in Nature Communications (2019).

## Data scope and taxonomy
- Field studies identified Hymenoptera (e.g., Apoidea, Vespidae, Tenthredinidae), Diptera (Syrphidae), and Lepidoptera to species, genus, or functional levels.
- When reliable species-level IDs were lacking, genus classifications or broader groups were used; certain taxa (e.g., some Coleoptera and parasitic Hymenoptera) were excluded due to low taxonomic resolution.
- Most butterflies were Pieris spp. (97.5%); other butterflies collapsed into a single functional group.
- International data include both published and unpublished sources; some data were augmented with unpublished observations.

## Effect traits and hairiness index
- Fifteen pollinator effect traits were derived, in categories including:
  - Body length (size-related trait, e.g., inter-tegular distance in bees).
  - Behavioral interactions with oilseed rape flowers (e.g., time spent on flowers, pollen foraging, dry pollen on bodies).
  - Morphological characteristics affecting pollen retention (corbiculae, scopa, etc.).
  - Pollen carriage and mouthpart structure (short/medium/long tongues; chewing mouthparts).
- Hairiness index defined as an overall measure related to pollen deposition efficiency and pollination cues.
  - Derived by scoring 12 body parts likely to contact stigmas (head, thorax sternum, abdomen underside, femora, tibiae, metatarsus; legs assessed separately for each of three pairs).
  - Scoring scheme: 0 = coarse setae/extremely short hairs; 1 = short but dense hairs; 2 = long dense hairs.
  - Sum across all body parts to a maximum of 24; expressed as a proportion (0 to 1) as the hairiness index.

## Metadata and data structure
- Meta data for 'Woodcock et al 2019 Species functional traits.csv':
  - Includes taxonomic classification (Order, Family, Species) and trait fields such as Mean_time_on_flower, Nectar_foraging, Pollen_foraging, Stigmal_contact, Dry_pollen, Mouthpart, Pollen_carried_only_in_crop, and various corbicula/scopa-related traits.
  - Trait values are numerical (probabilities 0–1 or continuous measures) or categorical; NA indicates data not available for a species.
  - Some data originate from Woodcock et al. (2019) and are augmented with unpublished data.
- Meta data for 'Woodcock et al 2019 Derivation of hairiness index.csv':
  - Details the hairiness values used to derive the index.
  - Fields include taxonomic classification (Order, Family, Species), hairiness_index (0–1), Summed_scores (0–24), and scores for each of 12 body parts (e.g., Face, Thorax, Abdomen, Femora_1, Tibiae_1, Metatibiae, etc.), with ordinal descriptors for body-part scores.
  - Notes that where classifications are not at the species level, generic or higher-level classifications were used.

## Data provenance and usage
- Traits and hairiness data are drawn from direct behavioural observations on oilseed rape flowers and morphology from taxonomic and literature sources.
- When species-level data were unavailable, higher-level classifications were used, and generic means were applied.
- The dataset supports replication and traceability through explicit references to the original studies and explicit provenance notes (e.g., data from Woodcock et al. 2019 augmented with unpublished data).

## References and funding
- Key references include multiple studies on pollinators and oilseed rape, culminating in the 2019 Nature Communications meta-analysis demonstrating that pollinator functional diversity and abundance enhance crop pollination and yield.
- Funding: Natural Environment Research Council (NERC) under programme NE/N018125/1 (ASSIST - Achieving Sustainable Agricultural Systems), with joint support from BBSRC.

## Relevance to monitoring frameworks
- Provides trait-based data critical for monitoring environmental health and ecosystem service delivery (pollination and crop yield).
- Highlights the importance of:
  - Clear metadata standards and provenance to ensure data usefulness across studies and time.
  - Open sharing of underlying data where possible, while acknowledging potential barriers (e.g., data sensitivity or unpublished components).
  - Addressing data gaps and resolving taxonomic resolution issues to enable robust, comparable monitoring.
  - Transparent data governance and quality control to support transformation, analysis, and reporting to stakeholders.