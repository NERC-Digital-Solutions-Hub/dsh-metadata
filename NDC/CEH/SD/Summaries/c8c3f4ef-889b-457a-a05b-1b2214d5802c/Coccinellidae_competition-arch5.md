# Coccinellidae competition

## Overview
- Studies used invasive Harmonia axyridis (IG predator) and two UK native coccinellids, Coccinella septempunctata and Adalia bipunctata (IG prey), to assess feeding preferences and competition.
- Coccinellids collected in Oxfordshire (UK) in May 2013; some Adalia bipunctata sourced from a biocontrol supplier to supplement field numbers.
- Rearing in controlled conditions (20 ± 1°C, 16 h photoperiod) for at least one laboratory generation; mixed field and lab-reared Adalia bipunctata to minimize source bias; larvae starved 24 h before trials.
- European large raspberry aphid, Amphorophora idaei, used as focal prey; maintained on raspberry plants in a controlled environment room (20 ± 1°C, 16 h photoperiod).
- Two experiments were conducted in arena setups to examine prey stage preferences and the effects of interspecific and intraspecific competition on feeding.

## Experimental setup and procedures
- Experiment 1: Predator preference by aphid nymphal stage
  - 50 A. idaei prey per trial, consisting of ten apterous adults and ten nymphs of each stage (I–IV).
  - Circular arena setup; a single coccinellid larva placed in center for 1 hour; number of aphids eaten per nymphal stage recorded.
  - 10 replicates per larval stage across three species (total 120 bioassays); conducted in 12 temporal blocks (10 assays per block).

- Experiment 2: Competition effects on shared prey
  - 25 A. idaei aphids per trial, with five apterous adults and five nymphs of each stage.
  - Aphids chilled to kill them while preserving tissue; cadavers arranged around arena to indicate stage.
  - Two coccinellid larvae (lifestage IV) placed in center in hetero- and conspecific pairings; one larva randomly marked for ID.
  - Each trial run for 1 hour; video-recorded to count aphid stages eaten by focal and competitor larvae.
  - Pairs alternated to switch focal species; 90 bioassays total, including a no-competitor control; 10 replicates per pairing.

## Data collection and structure

- Experiment1.csv
  - id: individual coccinellid identifier
  - block: temporal block
  - ladybird_stage: lifestage category
  - Coccinellid lifestage: larval stage
  - aphid_stage: aphid nymphal stage
  - aphid lifestage: aphid life stage
  - number_eaten: count of aphids consumed
  - species: coccinellid species
  - max: total number of aphids available at start

- Experiment2.csv
  - arena: arena identifier
  - metal dish / arena - unit of replication: replication unit
  - aphid_lifestage: aphid life stage
  - Aphid lifestage: aphid life stage (duplicate context for clarity)
  - focal_species: coccinellid species acting as the focal predator
  - Focal coccinellid species: repeat of focal_species
  - pred_species: competing coccinellid species
  - Competing coccinellid species: repeat of pred_species
  - eaten: number of aphid nymphs eaten by focal predator
  - painted: presence/absence of paint mark for individual ID
  - eaten_comp: number of aphids eaten by the competitor
  - total_aphid: total aphids available at start

- Analytical methods
  - Data analysis performed in R 3.0.2 using the gamm4 package.

## Data quality, provenance, and sharing
- Quality control: dataset checked manually for errors; no further quality control required.
- Provenance: experiments carefully documented with clear descriptions of rearing, experimental conditions, and observational procedures (including video analysis for Experiment 2).
- Availability: dataset documented and stored within the NERC Environmental Information Data Centre (EIDC) with a DOI link provided.

## Implications for data governance and reuse (Data Steward context)
- Metadata needs:
  - Clear definitions for all field names, life stage categorizations, and abbreviations (e.g., lifestage, aphid_stage, max).
  - Environment details (temperature, photoperiod) and rearing sources to support reproducibility.
  - Description of arena setup and replication schemes (block structure, trial timing).
  - Methods for counting (manual counts in Experiment 1; video analysis protocol in Experiment 2).
- Data formats and standardization:
  - Two CSV files with consistent variable naming and coding; consider harmonizing field names across datasets if additional experiments are added.
  - Include units for numerical fields (e.g., number_eaten, total_aphid) in metadata.
- Linkages and discoverability:
  - Ensure dataset is discoverable with proper citation, DOI, and explicit connection to the experimental design and species involved.
  - If linking to video data or raw recordings, provide metadata describing access rights, storage location, and associated identifiers.
- Reuse considerations:
  - The data support investigations of predator-prey interactions and competitive effects; documented methods enable secondary analyses, meta-analyses, or cross-study comparisons if standardized across studies.
- Potential enhancements:
  - Supplement with a data dictionary that unambiguously defines each field and coding scheme.
  - Include versioning and a changelog if updates or corrections are anticipated.