# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Overview
- Presents a subset of the DBIF dataset: 13,277 insect–plant interactions at the species level, Great Britain only, expertly verified.
- Data are provided in two CSV files:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x plant species as reported by each source.
  - DBIFSummaryWithPlantTraits.csv: summary counts of insect species per plant species, plus plant trait information.
- Includes plant native status, phylogenetic isolation metrics, distribution size, time since introduction for non-natives, and a measure of insect-community distinctiveness for non-native plants with insect richness ≥ 10.

## Data Files
- DBIFInteractionFrequencies.csv: Plant species, Insect species, DBIF source, and interaction frequency.
- DBIFSummaryWithPlantTraits.csv: Plant species, native status, distribution size (hectads), phylogenetic isolation metrics, years since introduction, distinctiveness, and related fields.
- Both files include NA/missing value indicators where data are unavailable.

## Plant Traits and Variables
- Native status categories:
  - N = native
  - ARCH = archaeophyte (non-native, pre-1500)
  - NEO = neophyte (non-native, post-1500)
- Distribution size:
  - Measured as the number of hectads (10x10 km) where the plant was recorded in 1987–1999 (Great Britain including Isle of Man).
  - Plants with no data assigned a size of zero.
- Time since introduction:
  - Years since introduction calculated for neophytes (e.g., 2018 minus introduction year).
- Phylogenetic isolation metrics (based on a global plant megaphylogeny):
  - Mean phylogenetic isolation (Mya): average divergence time from a plant to all others.
  - Nearest phylogenetic neighbour distance (Mya): divergence time to closest relative.
  - Mean phylogenetic isolation from natives (Mya): mean divergence from a non-native plant to all native plants.
  - Nearest native phylogenetic neighbour distance (Mya): distance to closest native relative.
- Insect community distinctiveness (for non-native hosts with richness ≥ 10):
  - Based on Chao-Sørensen abundance-based dissimilarity between the insect community on the non-native host and the insect pool on native plants within DBIF.

## Data Processing and Taxonomy
- DBIF cleaning and plant-trait assignment performed by Padovani R.
- Dataset composition after cleaning:
  - 4,397 insect species
  - 679 native plant species
  - 120 archaeophytes
  - 223 neophytes
- Plant taxonomy:
  - Only higher plants (seed plants and ferns) included.
  - Records must be expert-verified and GB-recorded; captive-breeding studies excluded.
  - Species-level resolution enforced; subspecies/cultivar/variety upgraded to species level where necessary.
  - Synonyms reconciled using BSBI, Stace’s flora references, UKSI, Fauna Europaea, and EPPO.
- Native status assignment:
  - Based on Stace & Crawley (Alien Plants), PlantAtt attributes, and Stace (New Flora) for unresolved native status.
  - 78 plant species excluded due to unreliable native/archaeophyte/neophyte status; 19 hybrids excluded.
- Distribution data:
  - Sourced from O. Pescott, with distribution measured in hectads (1987–1999).
  - Some species too rare to be detected in the period receive zero in the distribution size.
- Phylogeny:
  - Derived from Qian & Jin (2016) megaphylogeny using the pez R package.
  - 17% of species replaced by a polytomy when not found in the megaphylogeny; 11 species excluded for missing placement.
- Distinctiveness calculation:
  - Limited to non-native hosts with insect richness ≥ 10, using native vs. non-native comparisons within the DBIF.

## Spatial and Distribution Information
- Spatial component centered on Great Britain (with Isle of Man considered in distribution counts).
- Distribution size (hectads) provides a coarse geographic extent suitable for mapping plant distribution intensity and potential insect-host reach.
- Phylogenetic isolation metrics offer a spatially-informed context for how plant relatedness may influence insect associations.

## Data Sources and Documentation
- Data sources trimmed to article level; number of sources per plant species ranges from 1 to 64 (mean 6, median 3).
- Supporting information and citations accompany the dataset, including methodological references for:
  - Chao–Sorensen dissimilarity
  - Fauna Europaea
  - EPPO Global Database
  - PLANTATT attributes
  - The pez phylogenetics package
  - DBIF foundational papers and homepages
- NA values are indicated for missing data across fields.

## Access and Citation
- Data accessible via the provided DOI: https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418
- Citation required:
  Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insect and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Practical Considerations for GIS Use
- Suitable for map-based visualisations of insect–plant interactions across GB, integrating species interaction data with plant traits and distribution.
- Useful for exploring spatial patterns of insect richness, native versus non-native plant associations, and the influence of phylogenetic distance on interaction structure.
- Be aware of:
  - GB-only scope and subset filter (species-level, expert-verified).
  - Variation in data sources across plant species and potential sampling bias.
  - Exclusion of certain taxa due to taxonomy/native-status uncertainties.
  - Spatial resolution limited to hectads for distribution sizing.