# Database of British Insects and their Foodplants (DBIF)

## Scope and data subset
- Presents a subset of 13,277 interactions at the species level for Great Britain, expertly verified, drawn from the ~60,000 interactions in DBIF.
- Data are provided in two formats:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z.
  - DBIFSummaryWithPlantTraits.csv: summary view including total insect species interacting with each plant species and various plant/insect traits.

## Plant traits and associated metrics in the summary data
- Plant native status: native, archaeophyte (pre-1500 non-native), neophyte (post-1500 non-native).
- Plant distribution size: hectads (10x10 km grid squares) in Great Britain (1987–1999).
- Time since introduction: years since a non-native neophyte introduction (as of 2018).
- Plant phylogenetic isolation metrics (from a plant megaphylogeny):
  - Mean phylogenetic isolation (average divergence time to all other plants).
  - Nearest phylogenetic neighbour distance.
  - Mean phylogenetic isolation from natives (non-native plants to native plants).
  - Nearest native phylogenetic neighbour distance.
- Insect community distinctiveness: Chao-Sørensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants (calculated only for hosts with insect richness ≥ 10).

## Data collection, cleaning, and verification
- DBIF is based on a systematically compiled list of British herbivorous invertebrates; records sourced from literature, checklists, books, journals, and correspondence.
- Records were limited to higher plants (seed plants and ferns) and GB-native occurrences, excluding captive breeding records.
- Species- and synonym-level harmonisation used BSBI, Stace, UKSI, Fauna Europaea, and EPPO to standardise taxa.
- Excluded 78 plant species due to unreliable native status classification and 19 hybrids.
- Substantial data cleaning to upgrade sub-species/cultivar records to species level; nomenclature updates not uniform for pre-1990 entries.
- Phylogenetic assignment used Qian & Jin (2016) megaphylogeny; where species were not in the phylogeny, related clades were collapsed to polytomies; 11 species could not be placed and were excluded.
- Distribution size data derived from 1987–1999 New Atlas records (Pescott et al. 2018); plants with missing distribution data assigned a size of zero.

## Data structure and definitions
- DBIFSummaryWithPlantTraits.csv includes: Plant Species Name, Associated Insect Richness, Native Status, PI, NPN, PIN, NPNN, Hectads, Years Since Plant Introduction, Sources, Distinctiveness.
- DBIFInteractionFrequencies.csv includes: Plant Species Name, Insect Species Name, DBIF Source, Interaction Frequency, References.
- Data sources for the DBIF were trimmed to article level; number of reporting sources per plant species varied (mean 6, median 3; range 1–164).

## Data provenance and references
- Core DBIF foundations and trait calculations draw on key sources including Ward et al. (1988, 1993, 1995, 2003), Ward et al. (2019), PlantATT (Hill et al. 2004), Stace (2010), Stace & Crawley (2015), Fauna Europaea (de Jong et al. 2014), EPPO Global Database, Qian & Jin (2016), and others.
- Full DBIF dataset accessible via the DBIF homepage.