# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Overview
- Presents a subset of DBIF: 13,277 species-level interactions, Great Britain only, expert-verified.
- Data derived from a national-scale DBIF containing ~60,000 interactions.
- Available as two main data products: interaction frequencies and a summary with plant traits.

## Data files and contents
- DBIFInteractionFrequencies.csv
  - Plant species name, insect species name, data source, and interaction frequency (how many times the interaction was reported by each source).
- DBIFSummaryWithPlantTraits.csv
  - Plant species name with: associated insect richness, native status (native/archaeophyte/neophyte), phylogenetic isolation metrics, distribution size (hectads), years since introduction for neophytes, and a distinctiveness measure for insect communities (for non-native hosts with richness ≥10).
- Additional trait columns include: PI (mean divergence to all plants), NPN (nearest non-native relative), PIN (mean divergence from non-native to natives), NPNN (nearest native relative), Years Since Plant Introduction, Hectads, Distinctiveness.

## Plant traits and data included
- Native statuses: native, archaeophyte (pre-1500 non-native), neophyte (post-1500 non-native).
- Plant traits included with the summary data: distribution size, introduction date, and four phylogenetic isolation metrics.
- Insect-community distinctiveness calculated for non-native hosts with sufficient sampling.

## Plant taxonomy and data cleaning
- Only higher plants (seed plants and ferns) with expert verification and GB occurrence included.
- Records resolved to species level; subspecies/cultivar/variety upgraded to species level.
- Synonyms reconciled using BSBI, Stace, UKSI, Fauna Europaea, and EPPO databases.
- Final counts: 4,397 insect species; 679 native plant species; 120 archaeophytes; 223 neophytes.

## Native status and introduction dates
- Native vs. non-native classification based on multiple sources:
  - Archaeophyte: pre-1500 arrival
  - Neophyte: post-1500 arrival
  - Native: Holocene or later natural colonists
- Introduction dates and statuses sourced from Stace & Crawley (Alien Plants), PlantAtt, Stace (New Flora), and Hill et al. (PlantAtt validation).
- Exclusions: 78 plant species with unreliable native status; 19 hybrids removed.

## Distribution size
- Measured as the number of hectads (10x10 km) where the plant was recorded 1987–1999 (Great Britain including Isle of Man).
- Plants with no data assigned a distribution size of zero.

## Phylogenetic isolation
- Derived from a global vascular plant megaphylogeny (Qian & Jin 2016) using the pez R package.
- Four metrics:
  - Mean phylogenetic isolation (average divergence time to other plants)
  - Nearest phylogenetic neighbour distance
  - Mean isolation of natives from non-natives
  - Nearest native phylogenetic neighbour distance
- Data limitations: 17% replaced with polytomies; 11 species excluded due to missing placement.

## Insect community distinctiveness
- Calculated as Chao-Sørensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants.
- Only plants with insect richness ≥ 10 included (206 native, 30 archaeophyte, 26 neophyte hosts).

## Data sources and provenance
- DBIF data sources trimmed to article level; sources per plant range 1–64 (mean 6, median 3).

## Access, citation, and references
- Data accessible at the provided DOI URL.
- Required citation:
  Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418
- Key references informing DBIF construction, trait assignment, and methods (e.g., Chao et al. 2005; Ward et al.; Stace; Hill et al.; Qian & Jin; Pescott et al.; Pearse et al.).