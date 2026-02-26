# Species Traits and derivation of hairiness of oilseed rape pollinators

## Overview
- Describes a dataset of functional effect traits for 57 taxonomic units (species, genus, and family level classifications) of oilseed rape insect pollinators.
- Purpose: to assess how pollinator functional characteristics relate to oilseed rape yield, as reported in Woodcock et al. (2019) Nature Communications.

## data scope and content
- Taxonomic scope: Hymenoptera (e.g., Apoidea, Vespidae, Tenthredinidae), Diptera (primarily Syrphidae), and Lepidoptera; where species-level IDs were uncertain, genus-level or functional-group classifications were used.
- Taxonomic resolution: mix of species, genus, and family/functional-level classifications; functional types used for taxonomically complex groups.
- Traits: 15 effects traits derived to capture behavioural and morphological factors likely influencing pollen transfer, including body length, time on flowers, pollen foraging, nectar foraging, stigmal contact, pollen on body, and mouthpart type.
- Hairiness: a unique Hairiness index quantifying body hair density across multiple body parts to relate to pollen deposition.

## Methods and trait derivation
- Data sources: field studies with abundance data and, where needed, unpublished data; where species-level data were not available, higher-level aggregates were used.
- Trait derivation: traits derived at species level when possible; otherwise uses generic or higher-level means based on dominant classifications in the assessed datasets.
- Trait categories:
  - Body size: body length (mm) and inter-tegular distance for bees.
  - Behavioural interactions: mean time spent on flowers, probabilities of nectar foraging, pollen foraging, and dry pollen on the body; stigmal contact probability.
  - Pollen handling: presence of corbiculae and/or scopa, pollen carried in the crop, and other pollen-retention morphologies.
  - Morphology: mouthpart type (short/medium/long tongue or chewing).
  - Pollen availability and contact: multiple traits detailing pollen availability and contact likelihood.

### Hairiness index derivation
- Scoring: for each species, twelve body parts that contact stigmas were scored as 0 (coarse setae/extremely short hairs), 1 (short but dense hairs), or 2 (long dense hairs).
- Body parts assessed: head, thorax underside, sternum, abdomen underside, and three pairs of legs (femora, tibiae, metatarsus).
- Calculation: sum of scores across body parts, expressed as a proportion of the maximum possible score (24), yielding a hairiness index ranging from 0 to 1.

## Data files and metadata
- Woodcock et al 2019 Species functional traits.csv: metadata describing taxonomic associations and derived behavioural and morphological effect traits for each species (or higher-level unit). Data fields include taxonomic classifications and trait values (e.g., mean time on flower, nectar/pollen foraging probabilities, stigmal contact, mouthpart, pollen-carried in crop, various corbicula/scopa-related traits, and pollen moisture indicators). Missing values (NA) indicate data not available; where species-level data are missing, generic or higher-level means may be used.
- Woodcock et al 2019 Derivation of hairiness index.csv: metadata for the hairiness index derivation, including per-body-part scores and summed scores (0–24) and the resulting hairiness index as a proportion (0–1). Includes the same taxonomic fields as the trait dataset (Order, Family, Species, etc.) and the per-body-part scoring fields (Face, Thorax, Abdomen, Femora_1–3, Tibiae_1–3, Meta-tibiae_1–3).
- Woodcock et al 2019 Species functional traits.csv and Derivation of hairiness index.csv largely rely on the same taxonomic descriptors to enable cross-linking between trait values and hairiness metrics.

## Variables and trait definitions (highlights)
- Length: body length (mm).
- Mean_time_on_flower: mean seconds spent foraging on a flower.
- Nectar_foraging: probability of nectar foraging during a foraging event (0–1).
- Pollen_foraging: probability of pollen foraging during a foraging event (0–1).
- Stigmal_contact: probability that stigmal contact occurs during foraging (0–1).
- Dry_pollen: probability of presence of free dry pollen on the body (0–1).
- Mouthpart: tongue length category (long/medium/short) or chewing mouthparts.
- Pollen_carried_only_in_crop: presence/absence of pollen carried only in the crop (0/1) and related probability.
- Strict_tibia_corbicula, Propodeal_corbicula, Abdominal_corbicula, Femoral_corbiculae: presence/absence probabilities for various pollen-collecting structures (0/1).
- Basitarsal_scopa: presence/absence probability of basitarsal scopa (0/1).
- Corbiculula_pollen_moist: pollen stored in corbicula may be dry or moistened; associated 0/1 probability.
- Data may include missing values (NA) for certain species, with higher-level aggregates used where appropriate.

## Data quality, limitations, and use
- Mixed taxonomic resolution and occasional missing data; higher-level means are used when species-level data are unavailable.
- Data were augmented with unpublished observations to strengthen trait coverage.
- The dataset underpins analyses linking pollinator functional traits to oilseed rape pollination success and yield, as demonstrated in the cited Nature Communications meta-analysis.

## Provenance and funding
- Primary funding: Natural Environment Research Council (NERC) under ASSIST programme (NE/N018125/1), jointly supported with BBSRC.
- Data and metadata were compiled to support trait-based assessments of pollination services in oilseed rape, with direct involvement in the 2019 Nature Communications publication.

## References
- Core study: Woodcock, B.A. et al. (2019). Meta-analysis reveals that pollinator functional diversity and abundance enhance crop pollination and yield. Nature Communications, 10, 1481.
- Supporting references span a range of pollination ecology studies (1–14) detailing related findings on pollinator roles, body size, pollination efficiency, and pollination structures.