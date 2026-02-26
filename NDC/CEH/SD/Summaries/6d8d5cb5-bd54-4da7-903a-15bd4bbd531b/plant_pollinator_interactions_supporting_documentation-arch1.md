# Plant pollinator interactions for potential networks 2018

## Overview
- A dataset of pairwise plant-pollinator interactions for bees, hoverflies, and butterflies.
- Contains 16,712 unique interactions involving 499 plant species and 485 pollinator species (206 bees + 56 butterflies + 223 hoverflies).
- Collected from 1985–2015 across Great Britain.
- Interactions are predominantly inferred from biological recording data (73%), with the remainder from unpublished experimental data and published interactions.
- Aimed at constructing potential plant-pollinator networks alongside species occurrence data.

## Collection sources and data preparation
- Biological recording data from BWARS, Butterflies for the New Millennium (BNM), and Hoverfly Recording Scheme (HRS).
- Interactions recorded as incidental metadata accompanying occurrence records.
- Text-mmatching approach used to identify valid plant names (or synonyms/abbreviations) in the comments, followed by automated and manual cleaning.
- Exclusion criteria applied to remove non-entomophilous plants and those unlikely to transfer pollen effectively (e.g., many trees and grasses, habitat descriptions, or non-flower visitors).
- Some crop/garden species with persistent naturalised populations are included.
- Genus-level data: 79 genera had at least one genus-level interaction; assumed to represent interactions with all recorded species within that genus when species-level data were lacking. Approximately 7% of interactions derive from genus-level assumptions.

## Quality control and limitations
- Manual checks by CEH and BWARS researchers to confirm ecologically valid flower visitation (e.g., terms like "nectaring" or "feeding at").
- Acknowledgement of potential spurious records since not every record was manually verified.
- Not a complete GB record of plant-pollinator interactions; gaps exist in species coverage ( bees 76%, butterflies 95%, hoverflies 83%, insect-pollinated plants 55%) and in the links between them.
- Interactions describe visitation rather than confirmed pollination, and are assumed to be consistent across space where species co-occur.
- Where possible, users should supplement with observational or molecular data; the dataset is best suited for generating many replicate networks with similar data limitations to compare patterns.

## Data structure
- Single CSV file: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns:
  - POLLINATOR_NAME: Scientific name of the pollinator (as used by BWARS/HRS/UKBMS)
  - PLANT_NAME: Scientific name of the plant (as in PLANTATT)
  - Group: Pollinator group (Bees, Hoverflies, or Butterflies)
- Additional Description fields provide nomenclature context for both plant and pollinator names.

## Considerations for analysis and use
- Designed to produce large numbers of replicate networks to analyze structural patterns across networks with similar data limitations.
- Useful for identifying correlations and informing predictive models when combined with species occurrence data.
- Analysts should account for incomplete coverage, genus-level assumptions, and the distinction between visitation and true pollination.
- Appropriate to integrate with additional field-derived or molecular interaction data for validation and to refine network inferences.

## References and provenance
- Data sources and methodology described through the Bees, Wasps and Ants Recording Society (BWARS), Butterflies for the New Millennium (BNM), and Hoverfly Recording Scheme (HRS).
- Supporting notes and justifications for genus-level assumptions and data cleaning referenced in the project documentation.