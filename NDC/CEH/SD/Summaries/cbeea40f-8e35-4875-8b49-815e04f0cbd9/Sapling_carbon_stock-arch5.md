# DATA HEADER information for Sapling_carbon_stock.csv

## Overview
- Dataset records the carbon stock of regenerating tree clusters.
- Related materials: Manual 1_Classical_Survey.
- Funding and project context: ESPA programme; Project P4GES.
- Acknowledgement: Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.
- DOI reference provided for provenance.

## Data structure and key fields
- site_ID
  - Information: P4GES site code
  - Type: Text string
  - Unit: not specified
- Number_saplings
  - Information: number of trees with diameter < 5 cm and height > 1.3 m within a 2 m radius circle
  - Type: Numeric
  - Unit: not specified
- Number_collected_saplings
  - Information: number of saplings collected among the population inside the 2 m radius circle
  - Type: Numeric
  - Unit: not specified
- Fresh_weight_total
  - Information: total weight of all collected saplings
  - Type: Numeric
  - Unit: grams
- Fresh_weight_sample
  - Information: weight of the sample(s) collected for biomass analysis (weighed in the field)
  - Type: Numeric
  - Unit: grams
- Dry_weight_sample
  - Information: weight of subsample after oven drying (stabilized dry weight)
  - Type: Numeric
  - Unit: grams
- Dry_weight_collected_saplings
  - Information: weight of all collected saplings after oven drying (stabilized dry weight)
  - Type: Numeric
  - Unit: grams (note: documentation shows inconsistent entry "decameter" in one field)
- Biomass
  - Information: biomass stock of saplings
  - Type: Numeric
  - Unit: indicated as milligrams per hectare (Mg.ha-1) with conflicting labeling
- Stock_C
  - Information: carbon stock of saplings
  - Type: Numeric
  - Unit: indicated as milligrams per hectare (Mg.ha-1) with conflicting labeling
- Notes
  - "means no data" indicator present

## Provenance, rights, and references
- Data origin: Sapling carbon stock measurements as part of the P4GES ESPA project.
- DOI provided for dataset.
- Acknowledgement requirement for products derived from these data (Laboratoire des Radio Isotopes, Université d'Antananarivo).

## Metadata quality and inconsistencies (Data Steward focus)
- Unit inconsistencies and ambiguities:
  - site_ID unit not specified.
  - Dry_weight_collected_saplings entry shows an out-of-place unit (decameter) suggesting a metadata error.
  Biomass and Stock_C units are described inconsistently (mg/ha vs Mg/ha), leading to potential misinterpretation.
- Incomplete field metadata:
  - Some fields list units as "." or blank; field and materials resources are often empty.
- Data representation:
  - The note “means no data” implies a placeholder convention that should be clearly defined in the metadata.
- Action: verify and standardize units with data creators; correct unit definitions to Mg/ha for biomass and carbon stock or convert to a consistent like Mg.ha-1; fill missing units and field/resource metadata; remove or document the decameter anomaly.

## Data governance and stewardship recommendations
- Clarify and standardize units:
  - Decide on a single, standard unit for biomass (e.g., Mg ha-1) and carbon stock (Mg ha-1) and ensure all fields reflect it.
- metadata completion:
  - Populate site_ID units, field resources, and any other missing metadata.
- data provenance and methods:
  - Link to methodological details in the Manual 1_Classical_Survey and ensure methods (sampling within 2 m radius, criteria for saplings, drying protocols) are documented in metadata.
- data quality checks:
  - Implement validation rules to detect unit mismatches and obvious typographical errors (e.g., decameter in weight field).
- data sharing and updates:
  - Establish a clear data sharing policy, versioning, and update cadence; capture data availability status (including notes on missing data).
- data capture guidance for producers:
  - Provide explicit guidance to data creators on required fields, units, and data formatting to minimize future inconsistencies.
- ensure proper attribution:
  - Maintain the required acknowledgment to LRI and include DOI references in dataset metadata and distribution.

## Implications for data consumers
- Temperature, time, and location context are not specified in this header; refer to the Manual and accompanying metadata for sampling dates, coordinates, and habitat context.
- Interpret biomass and carbon stock values with the clarified units (once standardized) to enable comparability across sites and time.
- Treat the “means no data” note as a data availability indicator and check associated data files or records for missing values.