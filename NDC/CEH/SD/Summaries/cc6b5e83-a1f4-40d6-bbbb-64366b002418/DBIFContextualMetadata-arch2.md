# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Data scope and formats
- Subset scope: 13,277 interactions at species level, Great Britain only, expertly verified
- Data formats provided:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z
  - DBIFSummaryWithPlantTraits.csv: total number of insect species interacting with each plant species, plus plant traits
- Summary data includes:
  - Plant native statuses (native, archaeophyte, neophyte)
  - Plant phylogenetic isolation metrics
  - Plant distribution size
  - Time since non-native plant introduction
  - Distinctiveness of the insect communities on non-native plants (for a subset with insect richness ≥ 10)

## Plant and insect data included
- Final dataset composition (cleaned): 4,397 insect species linked to
  - 679 native plant species
  - 120 archaeophytes
  - 223 neophytes
- Taxonomic and records handling:
  - Only higher plants (seed plants and ferns)
  - Records expertly verified and constrained to Great Britain
  - Sub-species/cultivar/variety information upgraded to species level
  - Synonyms reconciled using BSBI, Stace, UKSI, Fauna Europaea, EPPO databases
  - Captive breeding records excluded

## Native status and introduction timing
- Native status assignment sources: PlantAtt (Hill et al. 2004), Stace & Crawley (alien plants), Stace (2010), plus Stace confirmations
- Exclusions due to status uncertainty: 78 species excluded; 19 hybrids excluded
- Introduction timing: years since introduction for neophytes (post-1500) used to compute “Years Since Plant Introduction”

## Plant distribution and phylogenetic measures
- Distribution size: number of hectads (10 x 10 km grid squares) recorded 1987–1999 (Great Britain including Isle of Man)
  - Plants with missing distribution size assigned zero
- Phylogenetic isolation measures (from Qian & Jin megaphylogeny; computed with pez):
  - Mean phylogenetic isolation (mean divergence time to all other plants)
  - Nearest phylogenetic neighbour distance (to closest relative)
  - Mean isolation of natives from non-native plants (mean divergence to native plants)
  - Nearest native phylogenetic neighbour distance (to closest native)

## Insect community distinctiveness
- Defined as Chao-Sorensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants
- Calculated for non-native hosts with insect richness ≥ 10
  - Included: natives (206), archaeophytes (30), neophytes (26)

## Data sources and provenance
- DBIF data originate from literature and checklists; sources range 1–64 per plant, mean 6, median 3
- Major references include Ward 1988; Ward & Spalding 1993; Ward et al. (1995, 2003); Smith & Roy (2008); Ward et al. (2019)
- Data were trimmed to article level (page numbers removed) for dataset preparation
- Supporting materials acknowledge additional datasets (e.g., distribution records, phylogenies)

## Data access and citation
- Data available via DOI: https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418
- Required citation: Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insect and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Relevance for environmental monitoring
- Provides standardized, verifiable measures of insect-plant interactions suitable for long-term monitoring and policy evaluation
- Enables analyses of how native status, phylogenetic relatedness, and plant distribution relate to insect richness and community composition
- Datasets can be integrated with other environmental data portals to enhance monitoring value and facilitate data reuse

## Considerations and limitations
- GB-centric subset; may not capture global patterns
- Focuses on higher plants; does not include non-vascular plants or captive-bred records
- Some phylogenetic and native-status assignments rely on specific sources; 78 species could not be reliably classified and were excluded
- Distribution data reflect 1987–1999 hectad records; may not reflect more recent changes