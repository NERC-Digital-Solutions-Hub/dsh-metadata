# Plant pollinator interactions for potential networks 2018

- A curated dataset of plant–pollinator interactions in Great Britain, intended to support construction of potential pollination networks using occurrence data.

## Data scope and content
- 16,712 unique interactions involving 499 plant species and 485 pollinator species (206 bees, 56 butterflies, 223 hoverflies).
- Data collected from 1985–2015 across Great Britain.
- Mostly derived from biological recording data (about 73%), with additional unpublished experimental data and published interactions.
- Interactions inferred by algorithmic text matching of pollinator records to valid plant names (or synonyms/abbreviations), followed by data cleaning.
- Purpose: to enable construction of potential plant–pollinator networks in combination with species occurrence data.

## Collection methods and processing
- Biological recording data sourced from BWARS, Butterflies for the Millennium (BNM), and Hoverfly Recording Scheme (HRS); interactions stored as incidental metadata with occurrence records.
- Automated screening for plant names; records typically reflect flower visitation but may also contain habitat notes, pollinator behavior, or sampling methods.
- Exclusions applied to avoid non-flower visits or non-entomophilous taxa (e.g., many trees, grasses).
- Only plant species with known entomophilic attraction and flowering were retained; some crop/garden species with naturalised populations included if persistent.
- Genus-level inferences: 79 genera with at least one genus-level interaction; assumed to apply to all species within those genera when species-level data were unavailable. Approximately 7% of interactions come from genus-level inferences.
- Quality checks included manual review by CEH and BWARS, with keyword checks (e.g., nectar, feeding) to validate ecological relevance.

## Data quality, limitations, and caveats
- Not a complete GB plant–pollinator record; coverage gaps across species ( bees ~76%, butterflies ~95%, hoverflies ~83%, insect-pollinated plants ~55%).
- Interactions reflect visitation, not confirmed pollen transfer; assumes interactions are conserved across space where species co-occur.
- Potential for spurious records despite manual checks.
- Recommendation to supplement with observational or molecular data where possible.
- Designed to produce many replicate networks with similar data biases for robust comparative analyses.

## Data structure and access
- File: plant_pollinator_interactions_for_potential_networks_2018.csv
- Columns:
  - POLLINATOR_NAME: Scientific name of pollinator (as used by BWARS/HRS/UK Butterfly Monitoring Scheme)
  - PLANT_NAME: Scientific name of plant (as in PLANTATT)
  - Group: Taxonomic group of pollinator (Bees, Hoverflies, Butterflies)

## Data governance and leadership implications (for Data Leaders)
- provenance: clear sourcing from multiple recording schemes; documented screening and cleaning steps.
- metadata and discoverability: standardized plant and pollinator nomenclature aligned to established references; single-file structure facilitates reuse.
- data quality management: explicit limitations, manual validation steps, and notes on genus-level inferences to inform risk assessment.
- data strategy opportunities: suitable for integrating with occurrence data across networks to study network structure; potential for cross-network collaboration and updates as new records become available.
- considerations for ongoing stewardship: maintain versioned releases, document changes in screening rules, and update coverage as additional data sources are integrated.