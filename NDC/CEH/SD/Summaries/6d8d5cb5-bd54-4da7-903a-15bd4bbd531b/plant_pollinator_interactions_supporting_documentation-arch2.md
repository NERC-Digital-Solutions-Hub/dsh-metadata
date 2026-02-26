# Plant pollinator interactions for potential networks 2018

## Overview
- A dataset of pairwise plant-pollinator interactions for bees, hoverflies, and butterflies across Great Britain, intended to support constructing potential plant-pollinator networks alongside species occurrence data.
- Contains 16,712 unique interactions involving 499 plant and 485 pollinator species (206 bees, 56 butterflies, 223 hoverflies) from 1985–2015.
- Primarily derived from biological recording data; some interactions come from unpublished experiments and published sources.

## Data sources and collection
- Primary sources: Bees, Wasps and Ants Recording Society (BWARS); Butterflies for the Millennium (BNM); Hoverfly Recording Scheme (HRS); UK Butterfly Monitoring Scheme.
- Interactions recorded as incidental metadata with occurrence records; interactions inferred via automated text matching to valid plant names and subsequently cleaned.
- To avoid non-ecologically valid matches, screening focuses on plants with flowers known to be visited by insects and capable of meaningful pollen transfer (entomophily). Excludes many trees, grasses, and habitat-descriptive matches.
- Some genus-level matches were accepted when a genus contains multiple species with similar floral visitors; about 7% of interactions arise from genus-level inferences.

## Data processing and quality control
- Initial screening by text matching and pollen vector, with manual validation by experts (CEH, BWARS) for keywords indicating flower visitation (e.g., nectar, feeding at).
- Acknowledges potential for spurious records without per-record manual checks.
- Limitations noted: dataset does not cover all GB plant-pollinator interactions; incomplete species coverage across bees, butterflies, hoverflies, and pollinator-plant links; interactions reflect visitation rather than validated pollination; assumes interactions are spatially consistent.

## Data structure and storage
- File: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns: POLLINATOR_NAME (pollinator species name as used by monitoring schemes), PLANT_NAME (plant species name as in PLANTATT), Group (Bees, Hoverflies, or Butterflies). Each entry may include corresponding Description fields for nomenclature.
- Designed to enable creation of large numbers of replicate networks; where possible, should be supplemented with observational or molecular data to validate interactions.

## Use and applicability
- Suitable for analyzing network structure and environmental health indicator patterns across replicated networks, despite data limitations.
- Encouraged to combine with other data sources and to provide access to underlying data to enhance transparency and reuse.
- Recognizes that some matches are genus-level or habitat-descriptive, requiring careful interpretation in analyses.

## Limitations and caveats
- Not a complete GB network map; substantial gaps in species and interaction coverage.
- Interactions represent visitation, not confirmed pollination; assumes consistency across space where co-occurrence occurs.
- Genus-level inferences and habitat-descriptive matches introduce uncertainty that should be accounted for in analyses.

## References
- Adams, Perkins & Estes (1981); Asher (1997); Clifford (1964); Hill, Preston & Roy (2004) PLANTATT attributes.