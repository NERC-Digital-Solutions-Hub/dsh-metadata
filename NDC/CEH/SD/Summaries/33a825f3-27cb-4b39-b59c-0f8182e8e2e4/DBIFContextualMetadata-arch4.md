# Summary

- A subset of the Database of Insect and their Food Plants (DBIF) is presented: 13,277 interactions at species level, Great Britain only, expertly verified.
- Data are provided in two formats:
  - DBIFInteractionFrequencies.csv: interaction frequencies between insect species x plant species as reported by sources.
  - DBIFSummaryWithPlantTraits.csv: summary of insect-plant interactions plus plant trait data.
- Included plant trait data with the summary file:
  - Native statuses: native, archaeophyte (pre-1500 non-native), neophyte (post-1500 non-native)
  - Phylogenetic isolation metrics
  - Plant distribution size (hectads, 1987–1999)
  - Time since non-native introduction
  - Insect community distinctiveness for non-native plants (for those hosting ≥10 insect species)
- Additional details on collection and calculation of plant traits are provided.

## What the DBIF is

- The DBIF aggregates records of British herbivorous invertebrates and their food plants from published literature and expert sources.
- Its historical development includes updates to invertebrate checklists and integration with major taxonomic resources (BSBI, Stace, UKSI, Fauna Europaea, EPPO, etc.).
- The full database is accessible online (DBIF homepage).

## Cleaning, curation, and plant trait assignment

- Procedures performed by Padovani R. to ensure GB-level, higher-plant (seed plants and ferns) data, with expert verification.
- Records upgraded to species level; subspecies/cultivar/variety mapped to species; synonyms reconciled across major taxonomic references.
- Native status and introduction dates sourced from multiple references; plants classified as native, archaeophyte, or neophyte, with some exclusions.
- Plant distribution size measured as the number of hectads in Great Britain (1987–1999 period).
- Phylogenetic isolation metrics derived from a global plant megaphylogeny (Qian & Jin 2016) using the pez R package; several adaptations made for missing data and clades.
- Insect community distinctiveness quantified as Chao-Sorensen abundance-based dissimilarity between insect communities on non-native hosts and those on native plants; calculations restricted to non-native hosts with insect richness ≥10.

## Key variables and data structure

- DBIFSummaryWithPlantTraits.csv
  - Plant Species Name
  - Associated Insect Richness
  - Native Status (N, ARCH, NEO)
  - PI (mean phylogenetic isolation vs all plants)
  - NPN (nearest plant phylogenetic neighbor distance)
  - PIN (mean divergence from non-native to native plants)
  - NPNN (nearest native neighbor distance for non-natives)
  - Hectads (GB distribution)
  - Years Since Plant Introduction
  - Sources (number of articles reporting on the plant)
  - Distinctiveness (Chao-Sorensen dissimilarity for non-native vs native insect communities)
- DBIFInteractionFrequencies.csv
  - Plant Species Name
  - Insect Species Name
  - DBIF Source (data source for the interaction)
  - Interaction Frequency (number of times the interaction was reported by each source)

## Dataset scope and final composition

- Final dataset features:
  - 4,397 insect species
  - 679 native plant species
  - 120 archaeophytes
  - 234 neophytes
- Filtering decisions:
  - Only higher plants included; records from GB and expert-verified
  - Subspecies/cultivar data upgraded to species level
  - 78 plant species with unreliable native status excluded; 19 hybrids excluded
  - 11 plant species unassignable in the phylogeny excluded
- Dataset limit: GB-centric, literature-derived interactions with explicit provenance and metadata.

## Data provenance and quality considerations

- Data sources trimmed to article level (no page numbers); source counts per plant vary widely (mean ~6, median ~3).
- Taxonomic harmonization across major UK and European references to ensure consistency.
- Native status and introduction dates compiled from several sources; transparent criteria for classifying plants as native/archaeophyte/neophyte.
- Phylogenetic metrics and distinctiveness measures computed with established methods and curated phylogenies.
- Explicit metadata on data cleaning and transformation processes to support reproducibility.

## How this supports data leadership aims

- System-wide view: linkage between insect-plant interactions and plant traits/phylogeny enables higher-level analyses of data ecosystems.
- User-centric design: provides summary metrics that can inform policy colleagues and other stakeholders about interaction richness and plant invasion context.
- Data discoverability and quality: clearly defined variables, provenance (sources), and standardized trait calculations enhance discoverability and reliability.
- Governance and collaboration: standardized, expert-verified data with documented methods support cross-team use and potential collaboration on expanding or updating the dataset.
- Practical applications: enables network analyses, invasion biology studies, phylogenetic community structure assessments, and trait-based investigations across native and non-native plant hosts.

## Limitations and caveats

- Geographic scope limited to Great Britain; may not generalize to other regions without adaptation.
- Reliance on published literature and expert sources; potential publication bias and uneven sampling across plant species.
- Some plant taxa excluded due to unresolved native status or phylogenetic placement; not all plants have complete trait data.
- Introduction dates and distribution sizes depend on historical records and may require updates as new data emerge.

## Access and references

- Data can be accessed via the DBIF platform (Database of British Insects and their Food Plants) and associated publications.
- Key references include Smith & Roy (2008), Ward et al. (various years), and the 2019 DBIF update.