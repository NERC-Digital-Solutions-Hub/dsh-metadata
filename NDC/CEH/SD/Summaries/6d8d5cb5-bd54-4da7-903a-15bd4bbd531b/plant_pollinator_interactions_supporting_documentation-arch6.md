# Plant pollinator interactions for potential networks 2018

## Overview
- A consolidated dataset of plant-pollinator interactions suitable for constructing potential networks.
- 16,712 unique interactions involving 499 plant species and 485 pollinator species (206 bees, 56 butterflies, 223 hoverflies).
- Interactions cover Great Britain and span 1985–2015; primarily derived from biological recording data, with some unpublished experimental data and published sources.
- Interactions are used alongside species occurrence data to build potential networks for analysis.

## Data sources and collection methods
- Collected from biological recording schemes: Bees, Wasps and Ants Recording Society (BWARS); Butterflies for the Millennium (BNM); Hoverfly Recording Scheme (HRS).
- Interactions were inferred by algorithmically screening pollinator records for text matches to valid plant names (or common synonyms/abbreviations), followed by automated and manual cleaning.
- To ensure ecological relevance, matches were filtered to exclude unvisited or non-entomophilous plants (e.g., many trees, grasses); some crop/garden species with persistent naturalised populations are included.
- In 79 genera where only genus-level matches existed, an interaction with the genus was assumed to apply to all recorded species within that genus (approx. 7% of interactions rely on genus-level data).

## Data processing and quality control
- Manual expert review by CEH and BWARS for key terms indicating flower visitation (e.g., nectaring, feeding).
- Recognizes potential for spurious records since not every record is checked individually.
- Limitations acknowledged: dataset does not represent a complete GB record of plant-pollinator interactions; coverage gaps exist for pollinator and plant species; interactions reflect visitation rather than confirmed pollination and assume spatial consistency where co-occurrence occurs.
- Where possible, outputs should be supplemented with observational or molecular validation.

## Data structure and content
- File: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns:
  - POLLINATOR_NAME: Scientific name of pollinator species (as used by BWARS, HRS, and UK Butterfly Monitoring Scheme)
  - PLANT_NAME: Scientific name of plant species (as in PLANTATT)
  - Group: Taxonomic grouping of pollinators (Bees, Hoverflies, Butterflies)

## Limitations and interpretation
- Coverage estimates: ~76% of GB bee species, 95% of GB butterfly species, 83% of GB hoverfly species, and 55% of insect-pollinated plants.
- Interactions denote flower visitation, not guaranteed pollination; assumes interaction persistence across space when co-occurrence occurs.
- Results are best used to generate large numbers of replicate networks for comparative analyses; should be interpreted with awareness of data gaps and assumptions.

## Practical applications for Data Support
- Create self-service networks and dashboards enabling exploration of potential plant-pollinator interactions.
- Combine with species occurrence data to analyze network structure and patterns across replicates.
- Promote outputs and gather feedback to refine networks; advocate for improved data creation and continued data integration.

## References
- Adams D.E., Perkins W.E. & Estes J.R. (1981). Pollination Systems in Paspalum dilatatum Poir. (Poaceae): An Example of Insect Pollination in a Temperate Grass. American Journal of Botany, 68, 389-394.
- Asher J. (1997). Butterflies for the New Millennium - project and programme. ITE Monks Wood, Huntingdon.
- Clifford H.T. (1964). Insect pollination of grasses. Australian Journal of Entomology, 3, 74-74.
- Hill M.O., Preston C.D. & Roy D. (2004). PLANTATT-attributes of British and Irish plants: status, size, life history, geography and habitats. Centre for Ecology & Hydrology.