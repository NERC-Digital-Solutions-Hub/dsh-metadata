# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Data access and citation
- Data are available from the provided DOI link.
- Citation required: Padovani, R.; Ward, L.; Smith, R. M.; Pocock, M. J. O.; Roy, D. B. (2019). Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF]. NERC Environmental Information Data Centre. https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Summary
- Presents a subset (13,277 interactions; species-level; Great Britain only; expertly verified) from the DBIF, originally containing ~60,000 interactions.
- Data formats:
  - DBIFInteractionFrequencies.csv: frequency of insect species x plant species interactions reported by sources.
  - DBIFSummaryWithPlantTraits.csv: total insect richness per plant species plus plant traits.
- Included with the summary data:
  - Plant native statuses (native, archaeophyte, neophyte).
  - Plant phylogenetic isolation metrics.
  - Plant distribution size.
  - Time since introduction for non-native neophytes.
  - Distinctiveness of insect communities associated with a subset of non-native plants (for those hosting insect richness ≥ 10).
- Detailed information on collection/calculation of plant traits provided.

## The Database of British Insects and their Foodplants (DBIF)
- DBIF is a systematically compiled list of British herbivorous insects and their food plants.
- Records largely derived from published literature, with sources including books, checklists, journals, and correspondence.
- Key sources include Royal Entomological Society checklists/handbooks, and consultations of slide collections for specific groups.
- The full database is accessible at the DBIF homepage.

## DBIF cleaning and plant trait assignment
- Procedures performed by Padovani R. to produce the final dataset:
  - Final dataset: 4,397 insect species, linked to 679 native plant species, 120 archaeophytes, and 223 neophytes.
- Focus on higher plants (seed plants and ferns); records must be expertly verified and GB-based; exclude captive breeding records.
- Resolution to species level: all subspecies/cultivars upgraded to species; genus- or higher-level records removed.
- Synonym harmonization: used major botanical and zoological sources to standardize names.

## Host plant native statuses
- Native status and neophyte introduction dates sourced from multiple databases.
- Classification:
  - Native: primarily Holocene colonists.
  - Archaeophyte: non-native, arrived pre-1500.
  - Neophyte: non-native, arrived post-1500.
- Non-native status and introduction dates drawn from Stace & Crawley; PlantAtt used to identify natives, with Stace (2010) confirming additional native entries.
- Exclusions: 78 plant species not reliably classifiable; 19 hybrids excluded.

## Host plant distribution sizes
- Distribution size measured as the number of hectads (10 x 10 km grid squares) recorded between 1987–1999 across Great Britain and Isle of Man.
- Period represents intensive recording (New Atlas project); plants with no data assigned a size of zero.

## Host plant phylogenetic isolation
- Phylogenetic relationships derived from a global vascular plant megaphylogeny (Qian & Jin 2016) using the pez R package.
- Handling of exclusions:
  - 17% of species replaced with a polytomy when not found in the megaphylogeny.
  - 11 species excluded due to clades not in the megaphylogeny.
- Four phylogenetic isolation metrics calculated:
  - Mean phylogenetic isolation (average divergence time to all other plants).
  - Nearest phylogenetic neighbour distance (to closest relative).
  - Mean phylogenetic isolation from natives (non-native to native plants).
  - Nearest native phylogenetic neighbour distance (to closest native plant).

## Insect community distinctiveness
- Defined as Chao-Sørensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants within DBIF.
- Calculated only for non-native plants hosting insect richness ≥ 10 (natives: 206, archaeophytes: 30, neophytes: 26).

## Data sources and structure
- DBIF sources are trimmed to article level (no page numbers); number of sources per plant varies (1–64; mean 6; median 3).
- Data columns and descriptions provided for both DBIFInteractionFrequencies.csv and DBIFSummaryWithPlantTraits.csv, including:
  - Plant species name, insect species name, interaction frequency, and source information.
  - Native status, introduction years, distribution (hectads), phylogenetic metrics, distinctiveness, and source counts.

## References
- Key methodological and data sources cited for: biodiversity foundations, plant-animal interactions, phylogenetics, distribution data, and the DBIF project itself.