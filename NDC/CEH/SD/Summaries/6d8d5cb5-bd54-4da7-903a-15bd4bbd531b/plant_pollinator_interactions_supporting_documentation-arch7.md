# Plant pollinator interactions for potential networks 2018

## Overview
- A GB-wide dataset of pairwise plant-pollinator interactions for bees, hoverflies and butterflies.
- 16,712 unique interactions involving 499 plant and 485 pollinator species (206 bees, 56 butterflies, 223 hoverflies).
- Data span: 1985–2015; mostly derived from biological recording data (≈73%), with some unpublished experimental data and published sources.
- Interactions are inferred from text matching of plant names in biological recording metadata, followed by automated and manual cleaning.
- Designed to support construction of potential plant–pollinator networks alongside species occurrence data.

## Dataset scope and contents
- Primary purpose: to enable the construction of potential networks when combined with occurrence data.
- Data sources: Bees, Wasps and Ants Recording Society (BWARS); Butterflies for the New Millennium (BNM); Hoverfly Recording Scheme (HRS).
- Interactions captured as incidental metadata alongside occurrence records; most matches reflect flower visitation, not confirmed pollination.

## Collection, processing, and quality control
- Processing steps:
  - Algorithmic screening for matches to valid plant names (or common synonyms/abbreviations).
  - Automated and manual data cleaning.
  - Manual expert checks by CEH and BWARS; screening for words indicating flower visitation (e.g., nectaring, feeding at).
- Genus-level simplifications:
  - 79 plant genera were represented at genus level when species-level data were unavailable; an interaction with a genus implies interactions with all recorded species within that genus (7% of interactions rely on genus-level data).
- Limitations and potential inaccuracies:
  - Not a complete GB record of plant–pollinator interactions; coverage gaps across species (bees ~76%, butterflies ~95%, hoverflies ~83%, insect-pollinated plants ~55%).
  - Some matches may reflect habitat descriptions or sampling methods rather than true flower visitation.
  - Interactions represent visitation, not verified pollination, and are assumed to be consistent across space where co-occurrence occurs.
  - Some records may be spurious without full manual verification.

## Data structure
- File: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns:
  - POLLINATOR_NAME: Scientific name of pollinator (as used by BWARS, HRS, UKBMS)
  - PLANT_NAME: Scientific name of plant (as in PLANTATT)
  - Group: Beeses, Hoverflies, or Butterflies

## Limitations and considerations for GIS use
- Suitable for generating large sets of replicate networks to study structural patterns, rather than precise, location-specific interaction maps.
- Requires linking with separate species occurrence data to create spatially explicit networks or maps.
- Be mindful of genus-level assumptions and incomplete coverage when interpreting results at finer taxonomic or spatial scales.
- Consider supplementing with observational or molecular data for validation when high-resolution, location-specific networks are needed.

## Potential GIS applications
- Map-based visualization of potential plant–pollinator networks across GB.
- Spatial analysis of network structure variability by region, habitat type, or time period when combined with occurrence data.
- Integrative GIS products that explore pollination potential under different scenarios (e.g., species distributions, land-use changes).

## References
- Adams D.E., Perkins W.E. & Estes J.R. (1981). Pollination Systems in Paspalum dilatatum Poir. (Poaceae): An Example of Insect Pollination in a Temperate Grass. American Journal of Botany, 68, 389-394.
- Asher J. (1997). Butterflies for the New Millennium - project and programme. ITE Monks Wood, Huntingdon.
- Clifford H.T. (1964). Insect pollination of grasses. Australian Journal of Entomology, 3, 74-74.
- Hill M.O., Preston C.D. & Roy D. (2004). PLANTATT-attributes of British and Irish plants: status, size, life history, geography and habitats. Centre for Ecology & Hydrology.