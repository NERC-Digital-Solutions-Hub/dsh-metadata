# DBIF - Database of British Insects and their Food Plants

## Overview
- Presents a subset of the national-scale DBIF, containing 13,277 verified interactions at species level for Great Britain.
- Data are provided in two CSV formats:
  - DBIFInteractionFrequencies.csv: interaction frequencies by insect species x plant species and source.
  - DBIFSummaryWithPlantTraits.csv: summary for each plant species, including native status and plant/phylogeny traits.
- Includes plant native statuses, phylogenetic isolation metrics, plant distribution size, time since introduction for non-natives, and a measure of insect community distinctiveness for non-native hosts with sufficient sampling.

## Data Content and Structure
- Interaction frequencies (DBIFInteractionFrequencies.csv):
  - Plant Species Name
  - Insect Species Name
  - DBIF Source
  - Interaction Frequency (how often the interaction is reported by the source)
  - References
- Summary with plant traits (DBIFSummaryWithPlantTraits.csv):
  - Plant Species Name
  - Associated Insect Richness
  - Native Status (N = native; ARCH = archaeophyte; NEO = neophyte)
  - PI (mean phylogenetic isolation from all plants)
  - NPN (nearest phylogenetic neighbour distance)
  - PIN (mean distance from non-native to native plants)
  - NPNN (nearest native neighbour distance from non-native plant)
  - Hectads (GB 1987–1999 distribution size)
  - Years Since Plant Introduction (as of 2018)
  - Sources (number of articles reporting on the plant)
  - Distinctiveness (Chao-Sørensen dissimilarity vs. native plant insect pools; included only with insect richness ≥ 10)

## Dataset Provenance and Cleaning
- DBIF foundation: compiled from British herbivorous invertebrate fauna with literature sources (books, checklists, journals, correspondence) and older checklists; GB records prioritized; some nomenclature may be pre-1990.
- Taxonomy and data resolution:
  - Only higher plants (seed plants and ferns) with reliable expert verification.
  - Records converted to species-level resolution; subspecies/cultivar/variety elevated to species level.
  - Synonyms harmonized using BSBI, Stace’s flora, UKSI, Fauna Europaea, EPPO.
- Native status and introduction dates:
  - Native, archaeophyte (pre-1500 non-native), neophyte (post-1500 non-native) statuses assigned across multiple data sources (PlantAtt, Stace sources, etc.).
  - 78 plant species excluded due to unreliable native status; 19 hybrids excluded.
- Distribution data:
  - Distribution size measured as hectads (10x10 km) in 1987–1999 for Great Britain including the Isle of Man.
  - Plants with no distribution data assigned a size of zero.
- Phylogenetic isolation:
  - Built a custom plant phylogeny using Qian & Jin (2016) megaphylogeny via the pez R package.
  - Four measures calculated:
    - Mean phylogenetic isolation (average divergence time to all other plants)
    - Nearest phylogenetic neighbour distance
    - Mean isolation from natives (non-native to all native plants)
    - Nearest native phylogenetic neighbour distance
  - 17% of species could not be placed in the megaphylogeny; 11 species excluded from this step.
- Insect community distinctiveness:
  - Defined as Chao-Sørensen abundance-based dissimilarity between insect communities on a non-native host versus native-host insect pools.
  - Included only non-native hosts hosting at least 10 insect species (206 native, 30 archaeophyte, 26 neophyte plant species).

## Data Sources and References
- Data sources trimmed to article level (excluding page numbers); variable source counts vary (mean around 6, median 3 per plant).
- Core references include foundational DBIF publications (Ward et al., 1988–2019), plant trait and native-status resources (PlantAtt; Stace; UKSI; Fauna Europaea; EPPO; Qian & Jin; Pearse et al.; Hill et al.; Pescott et al.).

## Data Use and Applications
- Enables self-service data exploration through two main outputs: interaction frequencies and plant-level trait summaries.
- Supports analyses across multiple dimensions:
  - Plant-insect interaction patterns at species level
  - Cross-plant comparisons using native status, distribution, and phylogenetic context
  - Insect community distinctiveness for non-native plants relative to natives
- Useful for dashboards, reports, and data products aimed at policy, biodiversity assessment, or ecological research.

## Practical Considerations and Limitations
- Coverage limitations due to patchy data and reliance on literature sources.
- Some taxa could not be placed in the phylogeny; results for those taxa are incomplete.
- Native status assignment depends on several sources and may carry uncertainties for certain taxa.
- Years Since Plant Introduction uses a fixed reference year (2018); interpret with this context.
- Data availability limited to GB (Great Britain) context and to higher taxonomic resolution for plants.

## Access
- Full DBIF data and documentation at the Database of British Insects and their Food Plants (DBIF) homepage: http://www.brc.ac.uk/dbif/homepage.aspx

## Summary of Final Dataset
- Insect species: 4,397
- Plant species: 679 native, 120 archaeophyte, 234 neophyte
- Interaction subset: 13,277 interactions
- Files:
  - DBIFInteractionFrequencies.csv
  - DBIFSummaryWithPlantTraits.csv