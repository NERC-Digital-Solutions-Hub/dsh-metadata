DATA HEADER information for Sapling_carbon_stock.csv

## Overview
- Purpose: Records the carbon stock of regenerating tree clusters.
- Context: ESPA Programme; Project P4GES.
- Acknowledgement: Required to acknowledge Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.
- Reference: See Manual 1_Classical_Survey; DOI provided.

## Data fields, definitions, and units
- site_ID
  - Information: P4GES site code
  - Variable type: Text String
  - Unit: (empty)
- Number_saplings
  - Information: Number of trees with diameter < 5 cm and height > 1.3 m counted in a 2 m radius circle
  - Variable type: Numeric
  - Unit: (empty)
- Number_collected_saplings
  - Information: Number of sapling trees collected among the population inside the 2 m radius circle
  - Variable type: Numeric
  - Unit: (empty)
- Fresh_weight_total
  - Information: Weight of all collected saplings
  - Variable type: Numeric
  - Unit: grams
- Fresh_weight_sample
  - Information: Weight of the sample among the collected saplings (samples weighed in the field)
  - Variable type: Numeric
  - Unit: grams
- Dry_weight_sample
  - Information: Weight of subsample after oven drying (stabilized dry weight)
  - Variable type: Numeric
  - Unit: grams
- Dry_weight_collected_saplings
  - Information: Weight of all collected saplings after oven drying (stabilized dry weight)
  - Variable type: Numeric
  - Unit: grams
- Biomass
  - Information: Biomass stock of sapling
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- Stock_C
  - Information: Carbon stock of sapling
  - Variable type: Numeric
  - Unit: milligrams per hectare (Mg.ha-1)
- Notes on data fields
  - Some fields show missing units or placeholders (represented by ".")
  - Notes indicate “means no data” for certain entries

## Data provenance and access
- Data origin: Sapling carbon stock measurements linked to ESPA and P4GES projects
- DOI: https://doi.org/10.5285/cbeea40f-8e35-4875-8b49-815e04f0cbd9
- Documentation: Refer to Manual 1_Classical_Survey for methodology and context

## Data quality and considerations for Data Leaders
- Data completeness: Several fields indicate missing data/units; plan for metadata completion and standardization
- Units consistency: Biomass and Stock_C reported as milligrams per hectare (Mg.ha-1); verify unit conventions (potential mismatch with common Mg/ha notation)
- Data discoverability: Clear field definitions exist, aiding data discovery and reuse; ensure metadata capture for discoverability
- Data provenance and attribution: Clear program/project lineage and required acknowledgment; important for cross-organization data sharing
- Risk areas: Potential data gaps at fine granularity; notes explicitly indicate “no data” in some cases; address in data strategy and planning
- Collaboration implications: Align with wider data community efforts for consistency in methodology and reporting across sites

## Practical implications for use
- Suitable for estimating sapling-level carbon stock and biomass within 2 m radius plots
- Enables cross-site comparison of sapling biomass and carbon stock (subject to unit consistency)
- Useful to identify data gaps and inform future data collection and standardization efforts
- Supports the development of data products with user-centered iteration and clear metadata for discoverability and reuse