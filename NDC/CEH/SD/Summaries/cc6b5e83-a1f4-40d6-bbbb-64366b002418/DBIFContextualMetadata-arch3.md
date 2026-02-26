# Supporting information for Insect species richness for each plant species and insect-plant interactions from the Database of Insects and their Food Plants [DBIF] https://doi.org/10.5285/cc6b5e83-a1f4-40d6-bbbb-64366b002418

## Overview
- Presents a subset (13,277 interactions at species level, Great Britain only, expertly verified) from the national-scale DBIF.
- Data are provided in two formats:
  - DBIFInteractionFrequencies.csv: frequency of interactions between insect species x and plant species y as reported by source z.
  - DBIFSummaryWithPlantTraits.csv: for each plant species, the total number of insect species interacting with it, plus plant traits.
- The summary data include plant native statuses, several plant phylogenetic isolation metrics, plant distribution size, time since non-native introduction, and a measure of insect-community distinctiveness for non-native plants hosting insect richness ≥ 10.

## Dataset contents
- Final cleaned DBIF dataset: 4,397 insect species associated with 679 native plant species, 120 archaeophytes, and 223 neophytes.
- DBIFSummaryWithPlantTraits.csv (summary data with traits) includes:
  - Native Status (N = native; ARCH = archaeophyte; NEO = neophyte)
  - PI (Mean phylogenetic isolation from all plants)
  - NPN (Nearest phylogenetic neighbour distance)
  - PIN (Mean isolation of non-native to native plants)
  - NPNN (Nearest native phylogenetic neighbour distance)
  - Years Since Plant Introduction
  - Hectads (distribution size)
  - Distinctiveness (Chao-Sorensen abundance-based dissimilarity vs native insect pool; computed for non-native hosts with insect richness ≥ 10)

## DBIF background and processing
- The DBIF was created from a systematically compiled list of British herbivorous invertebrates; records drawn from literature, checklists, journals, private correspondence, and museum slide collections.
- The 2007–2008 update added new records (especially for Coleoptera and Lepidoptera); nomenclature may be outdated for pre-1990 records.
- Full DBIF data were trimmed to article level (no page numbers) for this dataset.
- Final compiled subset emphasizes species-level records and reliable verifications; records linked to previously used large-scale analyses.
- Taxonomic harmonization used major references to unify synonyms and ensure comparability.

## DBIF cleaning and plant trait assignment
- Procedures conducted to ensure data quality and consistency (by Padovani R.).
- Final count: 4,397 insect species across 679 native plants, 120 archaeophytes, 223 neophytes.

## Plant taxonomy
- Included only higher plants (seed plants and ferns); records must be expertly verified and GB-native.
- Excluded captive-breeding records and non-species-level data (subspecies/varieties upgraded to species level).
- Synonym resolution used major reference sources (BSBI, Stace, UKSI, Fauna Europaea, EPPO).

## Host plant native statuses
- Classifications:
  - Native (N)
  - Archaeophyte (ARCH) – non-native, arrived before 1500
  - Neophyte (NEO) – non-native, arrived after 1500
- Native status and introduction dates sourced from Stace & Crawley (Alien Plants), PlantAtt, Stace (New Flora), UKSI, Fauna Europaea.
- 78 plant species could not be reliably classified and were excluded; 19 hybrids excluded.

## Host plant distribution sizes
- Distribution size quantified as the number of hectads (10 x 10 km grid squares) in GB between 1987–1999 (including Isle of Man; vice counties 1–112).
- Plants with no distribution data were assigned a size of zero.

## Host plant phylogenetic isolation
- Phylogenetic relationships derived from a global vascular plant megaphylogeny (Qian & Jin 2016) using the pez package.
- Four metrics calculated:
  - Mean phylogenetic isolation (average divergence time to all other plants)
  - Nearest phylogenetic neighbour distance (to closest relative)
  - Mean phylogenetic isolation from natives (non-native to native plants)
  - Nearest native phylogenetic neighbour distance (to closest native)
- Some species could not be placed in the phylogeny; 17% were replaced with a polytomy, and 11 species excluded due to missing placement.

## Insect community distinctiveness
- Distinctiveness defined as the Chao-Sorensen abundance-based dissimilarity between the insect community on a non-native host and the insect pool on native plants within DBIF.
- Calculation restricted to non-native hosts with insect richness ≥ 10.
- Sample sizes for distinctiveness calculations: natives (206 species), archaeophytes (30), neophytes (26).

## Data sources and metadata
- DBIF sources were trimmed to the article level; number of sources per plant species varied (1–64; mean ≈ 6; median 3).
- Data fields include presence/absence-related placeholders for missing values and the related trait metrics described above.

## References and data availability
- Core references underpinning DBIF and the trait calculations are cited (e.g., Chao et al. 2005; Ward et al.; Stace; Hill et al.; Pearse et al.; Pescott et al.; Qian & Jin).
- Data available via DOI; data can be cited as Padovani et al. (2019) with the DBIF dataset and supporting information.

## Implications for monitoring frameworks
- Relevance to monitoring:
  - Provides a rich, trait-informed basis for assessing insect–plant interactions across native and non-native plants.
  - Enables tracking of how phylogenetic relatedness, distribution, and introduction history relate to insect richness and community distinctiveness.
- Data governance and quality considerations:
  - Importance of provenance, expert verification, and species-level resolution for reliable monitoring.
  - Challenges include data access, metadata completeness, and maintaining up-to-date, interoperable datasets.
  - Encourages openness and data sharing while balancing attribution and source quality.
  - Requires careful data transformation, standardization, and robust data governance to support policy evaluation and future decision-making.