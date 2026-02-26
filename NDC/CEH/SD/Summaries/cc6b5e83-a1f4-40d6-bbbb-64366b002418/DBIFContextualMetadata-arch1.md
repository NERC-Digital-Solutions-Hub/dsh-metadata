# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Overview and scope
- Presents a subset of DBIF: 13,277 interactions at species level, Great Britain only, expertly verified
- Data are provided in two CSV files:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z
  - DBIFSummaryWithPlantTraits.csv: total number of insect species interacting with each plant species
- The summary file includes:
  - plant native statuses (native, archaeophyte, neophyte)
  - several plant phylogenetic isolation metrics
  - plant distribution size
  - time since non-native neophyte introduction
  - a quantitative measure of the distinctiveness of the insect communities on a subset of non-native plants (only those hosting insect richness ≥ 10)

## Data structure and contents
- DBIFInteractionFrequencies.csv
  - Plant Species Name
  - Insect Species Name
  - DBIF Source
  - Interaction Frequency (number of times the interaction was reported by the source)
- DBIFSummaryWithPlantTraits.csv
  - Plant Species Name
  - Associated Insect Richness (summed across sources)
  - Native Status (N, ARCH, NEO)
  - PI (Mya): mean divergence time from the plant to every other plant in the phylogeny
  - NPN (Mya): nearest phylogenetic neighbour distance
  - PIN (Mya): mean divergence time from a non-native plant to every other native plant
  - NPNN (Mya): nearest native phylogenetic neighbour distance
  - Years Since Plant Introduction
  - Hectads: number of 10x10 km grid squares containing the plant (1987–1999)
  - Distinctiveness: Chao-Sorensen abundance-based dissimilarity between the insect community on the non-native host and the insect pool on native plants (restricted to hosts with insect richness ≥ 10)

## Plant trait data and native status assignment
- Native statuses:
  - N = native (primarily Holocene colonists)
  - ARCH = archaeophyte (non-native, arrived pre-1500)
  - NEO = neophyte (non-native, arrived post-1500)
- Introduction dates and native status sources:
  - Stace & Crawley (Alien Plants), Hill et al. (PlantAtt), Stace (New Flora of the British Isles)
  - 78 plant species could not be reliably classified and were excluded
  - 19 hybrids excluded
- Distribution size:
  - Based on hectads 1987–1999 from the New Atlas project data (O. Pescott et al.)
  - Plants with no distribution information assigned a size of zero
- Phylogenetic isolation (using a global plant megaphylogeny and the pez package):
  - Four metrics calculated:
    - Mean phylogenetic isolation
    - Nearest phylogenetic neighbour distance
    - Mean phylogenetic isolation from natives
    - Nearest native phylogenetic neighbour distance
  - Some species could not be placed in the phylogeny and were excluded (17% of species); 11 species excluded for phylogeny issues

## Data curation and taxonomy
- Focused on higher plants (seed plants and ferns); records must be expertly verified and GB-native
- Records upgraded to species level; excluded genus-level records and captive-breeding data
- Synonym reconciliation across multiple taxonomic sources:
  - BSBI, Stace, UKSI, Fauna Europaea, EPPO Global Database
- Plant native status and introduction dates assembled from multiple sources; hybrids and ambiguous native statuses removed to ensure reliability

## Data sources and quality
- DBIF sources were trimmed to article level; number of reporting sources per plant varies (mean 6, median 3)
- Core references include Ward et al. (multiple works), Stace (flora), Hill et al. (PlantATT), Pearse et al. (pez), Pescott et al., Qian & Jin (megaphylogeny), among others

## Access and citation
- Data available and citable via the provided DOI
- Citation guidance:
  Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Practical implications for analysts
- Enables analysis of:
  - Insect-plant interaction frequencies by species across Great Britain
  - How insect richness relates to plant native status, distribution, and phylogenetic context
  - Distinctiveness of native versus non-native insect communities on plants with sufficient sampling
- Facilitates cross-dataset integration by providing standardized plant traits (native status, introduction date, distribution, phylogenetic metrics) alongside interaction data
- Useful for exploring correlations and generating predictive questions about invasion effects and plant–insect network structure