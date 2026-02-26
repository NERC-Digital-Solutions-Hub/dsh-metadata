# Species Traits and derivation of hairiness of oilseed rape pollinators

- An data description of functional effect traits for 57 taxonomic units (species, genus, and family level) of oilseed rape insect pollinators.
- Data were used to assess the link between pollinator functional characteristics and oilseed rape yield, notably in the Nature Communications 2019 meta-analysis by Woodcock et al.

## Scope and taxonomic approach

- Taxa include Hymenoptera (e.g., Apoidea, Vespidae, Tenthredinidae), Diptera (primarily Syrphidae), and Lepidoptera.
- Abundance data from field studies 1–8 and unpublished data; where species-level ID was unreliable, data used genus or functional group classifications.
- Functional types used for taxonomically complex groups; majority of butterflies pooled (Pieris spp.) due to low resolution for others.
- Some taxa (coleopteran and parasitic Hymenoptera) excluded due to variable taxonomic resolution; their traits not derived.

## Pollinator effect traits (15 traits)

- Traits are behavioural and morphological with high likelihood of influencing pollen transfer to oilseed rape stigmas (referred to as effects traits).
- Trait categories include:
  - Trait 1: Body length (related to body size and inter-tegular distance in bees).
  - Traits 2–6: Behavioural interactions with oilseed rape flowers (e.g., time on flowers, pollen foraging, dry pollen on bodies).
  - Trait 7: Hairiness index (overall body hairiness affecting pollen transfer).
  - Traits 8–14: Morphological characteristics affecting pollen retention (corbiculae and scopa, pollen-carrying structures).
  - Traits 14–15: Pollen availability dictated by pollen carried in bee crops and mouthpart structure (short/medium/long tongue; separate category for chewing mouthparts).
- Although traits 8–15 focus on bees, their absence can affect pollen carrying capacity and pollen stigmal transfer for non-bee pollinators, making them cross-taxon relevant.

## Hairiness index

- Purpose: hair density linked to pollen deposition on stigmas; also a potential pollination cue in bees.
- Derivation: species-specific scoring of body parts likely to contact stigmas (head, thorax, sternum, abdomen underside, femora, tibiae, metatarsus; legs assessed separately).
- Scoring scheme for each body part:
  - 0: coarse setae or extremely short hairs
  - 1: short but dense hairs
  - 2: long and dense hairs
- Scores summed across 12 body parts and expressed as a proportion of the maximum score (24), yielding a hairiness index from 0 to 1.

## Data files and meta-data

- Woodcock et al 2019 Species functional traits.csv
  - Taxonomic associations and derived morphological/behavioural effect traits for each species/unit.
  - Traits derived from direct behavioural observations on oilseed rape flowers and morphology from literature; where data were missing, generic or higher-level classifications were used.
  - Key fields include: Mean_time_on_flower, Nectar_foraging, Pollen_foraging, Stigmal_contact, Dry_pollen, Mouthpart, Pollen_carried_only_in_crop, Various corbicula/scopa-related traits, and related probability/ordinal fields.
- Woodcock et al 2019 Derivation of hairiness index.csv
  - Details values used to derive the hairiness index.
  - For each species: body parts scored (12 parts) with scores 0–2; summed to indicate hairiness; expressed as proportion of maximum 24.
  - Includes per-part descriptors (Face, Thorax, Abdomen, Femora_1/2/3, Tibiae_1/2/3, Meta-tibiae_1/2/3) and overall Summed_scores.
- Woodcock et al 2019 Hairiness index.csv
  - Hairiness index as a proportion (0–1) per species, plus summed scores and per-body-part scores (12 parts), with descriptive labels for each body part.
- Meta data for the above CSVs
  - Provides unit definitions, taxonomic description, and data detail for each trait (e.g., length units, probability bounds, categorical vs. numerical), and notes on data availability (NA where not available).

## Context and provenance

- Data originate from the ASSIST project (Achieving Sustainable Agricultural Systems), funded by NERC (NE/N018125/1) with BBSRC support.
- Traits are derived from Woodcock et al. (2019) meta-analysis, supplemented with unpublished data.
- The dataset includes detailed references to supporting literature on pollinator effects on oilseed rape yield and pollination ecology.

## References and usage

- Core related publication: Woodcock, B. A. et al. (2019). Meta-analysis reveals that pollinator functional diversity and abundance enhance crop pollination and yield. Nature Communications, 10, 1481.
- Additional references (14 listed) cover related pollinator studies and trait-context relationships.

## Practical notes for analysts

- Data enable cross-taxon analysis of how functional traits relate to pollination effectiveness and crop yield.
- Trait derivation relies on varying taxonomic resolution; where species data are missing, higher-level classifications are used, which may affect precision.
- The hairiness index provides a standardized cross-body-part metric to explore how physical pollen-carrying capacity influences stigmal deposition.
- When integrating with other datasets, ensure consistent taxonomic resolution and trait definitions, and account for NA trait values or inferred classifications.