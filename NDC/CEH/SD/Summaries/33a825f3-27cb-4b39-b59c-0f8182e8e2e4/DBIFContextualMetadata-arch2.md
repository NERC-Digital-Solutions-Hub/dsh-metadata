# Database of British Insects and their Food Plants (DBIF)

## Overview
- Presents a subset of 13,277 verified interactions (species level, Great Britain only) from the national-scale DBIF, out of roughly 60,000 interactions.
- Data are provided in two formats: interaction frequencies and a plant-trait–augmented summary.
- Aims to support monitoring of environmental health and policy performance by documenting insect–plant interactions and associated plant traits.

## Data products and structure
- DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z.
- DBIFSummaryWithPlantTraits.csv: for each plant species, total insect interaction richness and a suite of plant traits and metrics.
- Summary data supplement: plant native statuses (native, archaeophyte, neophyte), phylogenetic isolation metrics, plant distribution size, time since introduction for non-natives, and a measure of insect-community distinctiveness on non-native plants (for those with insect richness ≥ 10).

## Methods: data cleaning and plant trait assignment
- Only higher plants (seed plants and ferns) with expert verification were included.
- Records were restricted to Great Britain with records at species resolution; subspecies/cultivar/variety info upgraded to species level.
- Synonym reconciliation using BSBI, Stace, UKSI, Fauna Europaea, EPPO databases.
- Excluded 78 plant species with unreliable native status and 19 hybrids.

## Plant native status and introduction timing
- Native status categories: Native, Archaeophyte (pre-1500 non-native), Neophyte (post-1500 non-native).
- Introduction dates used to derive Years Since Plant Introduction (as of 2018) for neophytes.
- Native status sources include PlantAtt (Hill et al. 2004) and Stace’s New Flora (2010) plus additional native confirmations.

## Distribution size and phylogenetic context
- Distribution size is measured as the number of hectads (10x10 km grid squares in GB) recorded between 1987–1999.
- Phylogenetic isolation metrics derived from a global plant megaphylogeny:
  - Mean phylogenetic isolation (average divergence time to all other plants)
  - Nearest phylogenetic neighbour distance
  - Mean phylogenetic isolation from natives (non-natives to native plants)
  - Nearest native phylogenetic neighbour distance

## Insect community distinctiveness
- Defined as the Chao-Sørensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants.
- Calculated using plants with insect richness ≥ 10; included 206 native, 30 archaeophyte, and 26 neophyte host plant species.

## Data sources and variable definitions
- DBIF data sources trimmed to article-level references (n varying by plant; mean 6, median 3 sources per plant).
- Key variables included in DBIFSummaryWithPlantTraits.csv:
  - Plant Species Name, Associated Insect Richness, Native Status, PI, NPN, PIN, NPNN, Hectads, Years Since Plant Introduction, Sources, Distinctiveness.
- Key variables in DBIFInteractionFrequencies.csv:
  - Plant Species Name, Insect Species Name, DBIF Source, Interaction Frequency.
- Distinctiveness and phylogenetic metrics rely on published phylogenies and methodological references (Chao et al. 2005; Qian & Jin 2016; Pearse et al. 2015).

## Final dataset characteristics
- The cleaned dataset comprises 4,397 insect species associated with 679 native plant species, 120 archaeophytes, and 234 neophytes.
- Phylogenetic assignment incomplete for some taxa (approximately 17% of plant species could not be placed in the megaphylogeny) and some clades were simplified to polytomies.
- Some plants (78 native/other) could not be reliably classified by native status; 19 hybrids were excluded.

## Data access and usage for environmental monitoring
- Full DBIF database and details are available at the Natural History Museum/Bioscience Centre for Ecology & Hydrology portal (DBIF homepage).
- The summarized and trait-augmented outputs enable standardized reporting of insect–plant interactions and plant trait contexts, facilitating time-series monitoring, biodiversity assessments, and policy performance evaluations.

## Limitations and caveats
- Subset is species-level and GB-focused, which may limit broader regional generalizations.
- Exclusions due to native-status uncertainty and incomplete phylogenetic placement may affect some trait calculations.
- Reliance on historical records and literature sources; potential biases in source availability and reporting across taxa and plant groups.