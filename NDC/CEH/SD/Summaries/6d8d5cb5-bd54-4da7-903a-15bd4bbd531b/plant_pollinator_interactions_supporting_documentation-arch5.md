# Plant pollinator interactions for potential networks 2018

## Overview
- A dataset of pairwise plant-pollinator interactions for bees, hoverflies, and butterflies.
- 16,712 unique interactions involving 499 plant species and 485 pollinator species (206 bees, 56 butterflies, 223 hoverflies).
- Collected from 1985–2015 across Great Britain; mostly derived from biological recording data (about 73%), with the remainder from unpublished experiments or published literature.
- Created to support construction of potential plant-pollinator networks alongside species occurrence data.

## Data collection and sources
- Biological recording data were obtained from BWARS (Bees, W asp s and Ants Recording Society), BN M (Butterflies for the Millennium), and HRS (Hoverfly Recording Scheme); interactions recorded as incidental metadata with occurrence records.
- Text-based matching used to identify valid plant names (scientific or vernacular) in records; subsequent filtering to ensure plants are entomophilous and capable of pollen transfer.
- Excluded non-flower interactions and many non-visited plants (e.g., many trees, grasses) to reduce spurious matches.
- Some records match at genus level; 79 genera with genus-level interactions were included under the assumption that the genus-level interaction implies interactions with all species within the genus.

## Data curation and provenance
- Screening and data cleaning were performed by a team including CFC, HJD, RD, SLR, JWR, THO, MJP, BAW, AJV, and RFP.
- Manual expert checks by CEH and BWARS to validate ecologically plausible interactions (e.g., keywords like nectar, feeding).

## Data quality and limitations
- Not a complete GB record; coverage gaps for species and links:
  - Bees: ~76% of GB bee species represented
  - Butterflies: ~95%
  - Hoverflies: ~83%
  - Insect-pollinated plants: ~55%
- Interactions reflect flower visitation rather than confirmed pollination; assumes interactions are consistent across space when species co-occur.
- Best used for generating large numbers of replicate networks; results should be supplemented/validated with observational or molecular data where possible.

## Data structure and access
- File: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns:
  - POLLINATOR_NAME: Scientific name as used by BWARS/HRS/UKBMS
  - PLANT_NAME: Scientific name per PLANTATT
  - Group: Taxonomic grouping (Bees, Hoverflies, or Butterflies)

## Metadata and references
- References for taxonomy and methods include Adams et al. (1981), Asher (1997), Clifford (1964), and Hill et al. (2004) (PLANTATT).
- Plant-pollinator interactions are inferred from recorded metadata and curated to reflect likely pollinator-plant associations.

## Practical considerations for data stewards
- Maintain and update taxonomic mappings and synonyms; clearly document genus-level assumptions and their implications.
- Preserve provenance, curation steps, and expert validation records for transparency.
- Communicate dataset limitations to users, emphasizing that networks are potential interactions with inherent biases and incomplete coverage.