# DBIF - Database of British Insects and their Food Plants (DBIF)

## Overview
- Presents a subset of the DBIF: 13,277 interactions (species level, Great Britain only, expertly verified).
- Data provided as two files:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z.
  - DBIFSummaryWithPlantTraits.csv: summary per plant species (total insect species interacting with the plant).
- Includes plant traits and metrics to support GIS-based analyses:
  - native statuses, phylogenetic isolation metrics, plant distribution size, time since introduction for non-native neophytes, and a distinctiveness measure of insect communities on certain non-native plants.

## Data Files and Key Variables
- DBIFSummaryWithPlantTraits.csv
  - Plant Species Name
  - Associated Insect Richness
  - Native Status: N (native), ARCH (archaeophyte), NEO (neophyte)
  - PI: mean phylogenetic distance to all other plants
  - NPN: nearest phylogenetic neighbor distance
  - PIN: mean distance from non-native plant to all native plants
  - NPNN: distance from non-native plant to nearest native neighbor
  - Hectads: number of 10x10 km grid squares (1987–1999)
  - Years Since Plant Introduction: for neophytes (as of 2018)
  - Sources: number of articles reporting the plant
  - Distinctiveness: Chao-Sorensen dissimilarity between insect community on the non-native host and the native plant insect pool (only plants with insect richness ≥ 10)
- DBIFInteractionFrequencies.csv
  - Plant Species Name
  - Insect Species Name
  - DBIF Source
  - Interaction Frequency: how often the interaction was reported by the source
  - References: bibliographic sources (summarized to article level)

## Collection, Cleaning and Curation
- DBIF foundations:
  - Based on a systematically compiled list of British herbivorous invertebrates; sources include Royal Entomological Society checklists, journals, books, and private correspondence.
  - Literature-informed coverage with updates to some families (Coleoptera, Lepidoptera) in the 2007–2008 update.
  - Nomenclature may not be fully updated for pre-1990 entries; full DBIF available online.
- Data cleaning ( led by Padovani R. ):
  - Final dataset: 4,397 insect species associated with 679 native plants, 120 archaeophytes, 234 neophytes.
  - Species-level resolution: records upgraded to species level; records from captive breeding excluded.
  - Taxonomic harmonization:
    - Synonyms reconciled using BSBI, Stace (2010), UKSI, Fauna Europaea, EPPO Global Database.
- Plant native status and introduction dates:
  - Plants classified as native, archaeophyte (pre-1500 non-native), or neophyte (post-1500 non-native).
  - Introduction dates and native status sourced from PlantAtt, Stace & Crawley (2015), Stace (2010), and UK resources.
  - 78 plant species excluded due to unreliable native status; 19 hybrids excluded.
- Distribution and phylogeny:
  - Distribution size: hectads (1987–1999) across GB (incl. Isle of Man).
  - Phylogenetic isolation: derived from a global vascular plant megaphylogeny (Qian & Jin 2016) using pez (Pearse et al. 2015).
  - Some adjustments: 17% of species replaced with a polytomy; 11 species could not be placed in the phylogeny and were excluded.

## Insect Community Distinctiveness and Plant Traits
- Distinctiveness metric:
  - Calculated as Chao-Sorensen abundance-based dissimilarity between the insect community on a given non-native host and the insect pool on native plants.
  - Only non-native plants hosting insect richness ≥ 10 were included (206 native, 30 archaeophyte, 26 neophyte hosts used for distinctiveness calculations).
- Data sources:
  - Sources trimmed to article level (no page numbers); mean sources per plant ~6 (range up to 164).

## Final Dataset Scope and Suitability for GIS
- Scope:
  - 4,397 insect species; 679 native plants; 120 archaeophytes; 234 neophytes.
  - 13,277 interactions (GB, species-level, expert-verified).
- GIS relevance:
  - Provides spatial distribution proxies (hectad-based) and plant native status, introduction times, and phylogenetic context for mapping insect-plant interactions.
  - Enables mapping of native vs non-native interactions and assessment of community distinctiveness across GB.
- Limitations and caveats:
  - Phylogeny coverage is incomplete for some taxa; 17% of plants were placed in polytomies or excluded due to phylogeny limitations.
  - Native status assignment uncertainties for a subset of species; some plants/habitat records are excluded (hybrids, uncertain natives).
  - Interaction frequencies reflect multiple sources with variable coverage and reporting biases.
  - Data limited to Great Britain (with Isle of Man included in distribution size).

## References and Data Provenance
- Core DBIF references include Smith & Roy (2008), Ward et al. (various years), Ward et al. (2019), and related taxonomic and phylogenetic sources.
- Trait and distribution data sourced from PlantAtt (Hill et al. 2004), Stace (2010), Stace & Crawley (2015), UKSI, Fauna Europaea, EPPO Global Database, and Pescott et al. (2018).
- Phylogeny and methodological references: Qian & Jin (2016), Pearse et al. (2015).