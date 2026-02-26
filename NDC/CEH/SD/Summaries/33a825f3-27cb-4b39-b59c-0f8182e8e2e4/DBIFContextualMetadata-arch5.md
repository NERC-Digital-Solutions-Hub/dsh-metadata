# DBIF - Database of British Insects and their Food Plants

## Overview
- A subset of the national-scale Database of Insect and their Food Plants (DBIF): 13,277 expert-verified interactions at species level, GB-only.
- Data products include both interaction frequencies and plant-trait summaries to support usability and discovery.

## Data Products
- DBIFInteractionFrequencies.csv: frequency of interactions between each insect species x plant species as reported by each source.
- DBIFSummaryWithPlantTraits.csv: per-plant summary including total insect species interacting, plus plant traits (native status, phylogenetic isolation metrics, distribution size, introduction timing, and insect-community distinctiveness for non-native hosts with insect richness ≥ 10).

## Data Cleaning and Trait Assignment
- Cleaning performed to ensure species-level resolution and reliable records:
  - Excluded genus- and lower-resolution records; upgraded subspecies/cultivars to species level.
  - Only higher plants (seed plants and ferns) and records confident to occur in Great Britain; captive-breeding records removed.
  - Taxonomy harmonized against BSBI, Stace, UKSI, Fauna Europaea, EPPO, and other sources to consolidate synonyms.
- Native statuses and introduction dates collated from Stace & Crawley and PlantAtt, with additional verification from Stace (2010) and related sources.
- Excluded 78 plant species due to unreliable native status classification and 19 hybrids.

## Plant Traits and Phylogenetic Metrics
- Native status categories:
  - N: Native (Holocene colonists)
  - ARCH: Archaeophyte (arrived pre-1500, non-native)
  - NEO: Neophyte (arrived post-1500, non-native)
- Distribution sizes:
  - Measured as hectads (10 x 10 km grid squares) in 1987–1999 (Great Britain incl. Isle of Man).
  - Plants with no data assigned a size of zero (12 species had no recorded distribution size).
- Introduction timing:
  - Years since introduction for neophytes (as of 2018).
- Phylogenetic isolation (based on a global plant megaphylogeny):
  - Mean phylogenetic isolation (average divergence time to all other plants).
  - Nearest phylogenetic neighbour distance (divergence time to closest relative).
  - Mean isolation of natives from non-natives.
  - Nearest native phylogenetic neighbour distance to non-natives.
- Insect community distinctiveness (for non-native hosts with insect richness ≥ 10):
  - Measured using Chao-Sorensen abundance-based dissimilarity between the non-native host’s insect community and the pool on native plants.

## Insect Community Distinctiveness
- Defined as the dissimilarity between insects on a non-native host and the insect pool on native hosts within DBIF.
- Included only non-native hosts hosting at least 10 insect species; sample sizes: natives (206 species), archaeophytes (30), neophytes (26).

## Data Sources and Provenance
- All DBIF data sources trimmed to article level (no page numbers) to simplify provenance tracking.
- Total sources per plant species varied (mean ≈ 6, median ≈ 3; up to 164 sources for some species).
- Full DBIF previously described in multiple foundational publications; current subset builds on extensive literature and museum records.

## Variable Definitions (Key Fields)
- DBIFSummaryWithPlantTraits.csv:
  - Plant Species Name
  - Associated Insect Richness
  - Native Status (N, ARCH, NEO)
  - PI (Mean phylogenetic isolation from all plants)
  - NPN (Nearest phylogenetic neighbor distance to any plant)
  - PIN (Mean phylogenetic isolation from non-native plants to natives)
  - NPNN (Nearest native phylogenetic neighbor distance from non-natives)
  - Hectads
  - Years Since Plant Introduction
  - Sources
  - Distinctiveness (Chao-Sorensen dissimilarity)
- DBIFInteractionFrequencies.csv:
  - Plant Species Name
  - Insect Species Name
  - DBIF Source
  - Interaction Frequency
  - References (citation details)

## Dataset Scope and Content
- Final dataset composition (GB-focused):
  - 4,397 insect species
  - 679 native plant species
  - 120 archaeophytes
  - 234 neophytes
- Data products enable both interaction-level analysis (frequencies) and plant-centric summaries with trait context.

## Data Quality, Limitations, and Challenges
- Incomplete user-need picture and potential delays in data provision acknowledged as typical data stewardship challenges.
- Limitations due to:
  - GB-only focus; historical records with nomenclature changes; potential inconsistencies across sources.
  - Some plant species unclassifiable by native status (excluded) and 19 hybrids excluded.
  - Phylogenetic placement gaps: 17% of species not assignable in the megaphylogeny; some clades replaced with polytomies or excluded.
  - Variation in data richness across plants (fewer sources for some species).

## Governance, Access, and Stewardship Implications
- Clear provenance: documented data sources, harmonization rules, and versioned data products.
- Metadata richness supports discoverability and reusability (species-level interactions, plant traits, and phylogenetic context).
- Update and sharing considerations:
  - Data can be uploaded to appropriate portals and catalogues; future updates should maintain taxonomic harmonization and provenance.
  - Documented limitations guide responsible use and interpretation, especially regarding native status, phylogenetic placement, and data completeness.
- Practical use for data stewards:
  - Maintain rigorous taxonomy alignment, track source-level changes, and manage updates to plant native statuses and introduction dates.
  - Ensure consistent calculation and documentation of phylogenetic and distinctiveness metrics.
  - Provide user guidance on data scope (GB only, species-level records) and caveats related to data completeness and geographic/temporal coverage.