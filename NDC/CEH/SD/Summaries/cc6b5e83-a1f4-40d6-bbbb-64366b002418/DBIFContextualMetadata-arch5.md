# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF]

## Overview for Data Stewards
- Purpose: Provides a subset of the DBIF with 13,277 validated insect-plant interactions (species-level, Great Britain only) for analysis of insect richness and interactions.
- Availability: Data accessible via the DOI link and cited in the referenced publication.
- File outputs: Two CSV files prepared for reuse:
  - DBIFInteractionFrequencies.csv: interaction frequencies between insect species and plant species, with source attribution.
  - DBIFSummaryWithPlantTraits.csv: summary of insect richness per plant species plus plant trait data.

## Data content and scope
- Interaction data: Frequencies captured as the number of times a specific insect-plant interaction was reported by each source.
- Summary data: For each plant species, total insect richness reported across sources; includes derived plant traits and native status.
- Scope details:
  - 13,277 interactions (Great Britain, species-level, expertly verified).
  - Related broader DBIF dataset includes ~60,000 interactions; the summary here represents a curated subset.
  - Associated plant traits in the summary include native status, phylogenetic isolation metrics, distribution size, introduction time, and a measure of insect community distinctiveness for non-native hosts with sufficient sampling (insect richness ≥ 10).

## Data curation and plant trait assignment
- Dataset assembly: Performed by Padovani R.; final curated dataset includes:
  - 4,397 insect species
  - 679 native plant species
  - 120 archaeophyte plant species
  - 223 neophyte plant species
- Data processing objectives: Ensure species-level resolution, reliable records, and GB occurrence. Non-GB or captive-bred records are excluded to maintain GB relevance and veracity.

## Taxonomy and plant records
- Plant scope: Higher plants (seed plants and ferns) with expert verification.
- Resolution and standardization: All records upgraded to species level; synonyms reconciled using major taxonomic sources.
- Exclusion criteria: Records not reliably assigned to native/archaeophyte/neophyte status, or hybrids (78 excluded due to uncertain native status; 19 hybrids excluded).
- Synonym reconciliation sources: BSBI, Stace (New Flora of the British Isles), UKSI, Fauna Europaea, EPPO Global Database.

## Native status, introduction date, and distribution
- Native status categories:
  - N (native, primarily Holocene colonists)
  - ARCH (archaeophyte, non-native arrived pre-1500)
  - NEO (neophyte, non-native arrived post-1500)
- Introduction timing data: Years since introduction for neophytes (Years Since Plant Introduction).
- Distribution size: Measured as number of hectads (10 x 10 km grid squares) in GB between 1987–1999 (Isle of Man included). Missing values assigned zero for species lacking data.
- Data sources for native status: Stace & Crawley (Alien Plants 2015), PlantAtt (Hill et al. 2004), Stace (New Flora of the British Isles), Stace & others to confirm native status where uncertain.
- Exclusions: 78 species with unreliable native/archaeophyte/neophyte classification and 19 hybrids removed from the dataset.

## Phylogenetic isolation and plant traits
- Phylogeny: Plants placed using a global vascular plant megaphylogeny (Qian & Jin 2016) with the pez package.
- Handling of missing phylogeny data: 17% of species were placed into a polytomy when not found in the phylogeny; 11 species could not be assigned and were excluded.
- Phylogenetic isolation metrics (4 measures):
  1) Mean phylogenetic isolation (mean divergence time to all other plants)
  2) Nearest phylogenetic neighbour distance (to closest relative)
  3) Mean phylogenetic isolation from natives (non-native to native plant comparisons)
  4) Nearest native phylogenetic neighbour distance (non-native to closest native relative)
- Distinctiveness (insect community): Chao-Sorensen abundance-based dissimilarity between insect community on a given non-native host and the insect pool on native plants. Calculated only for plants with insect richness ≥ 10 (206 native, 30 archaeophyte, 26 neophyte taxa).

## Data sources and provenance
- Data source scope: DBIF sources trimmed to article level; page numbers removed to standardize provenance.
- Source diversity per plant: Varied across species (1–64 sources); mean = 6, median = 3.
- Reference framework: Key data sources and methods cited include foundational DBIF publications and methodological references for phylogenetics, dissimilarity metrics, and plant trait databases (e.g., PlantAtt, Stace, Fauna Europaea, EPPO, Qian & Jin megaphylogeny, Chao et al., etc.).

## Data access, usage, and citation
- Access: Data available via the provided DOI URL.
- Citation requirement: Users must cite Padovani et al. (2019) for the DBIF subset:
  Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Practical notes for Data Stewards
- Metadata considerations: Ensure documentation includes data scope (Great Britain, species-level, verified), file definitions (interaction frequencies vs. summary traits), and clear notes on exclusions.
- Quality and governance: Acknowledge the filtering steps (species-level resolution, native status assignment, distribution data period) and potential biases due to data sources and sampling effort (0–64 sources per plant; natives vs. non-natives sampling depth).
- Update and maintenance: Any update would require re-derivation of trait metrics (phylogenetic isolation, distinctiveness) if new phylogenetic or distribution data become available.
- Interoperability: Harmonize plant and insect species nomenclature with current taxonomic standards; maintain provenance linkage to the original DBIF dataset and cited sources.