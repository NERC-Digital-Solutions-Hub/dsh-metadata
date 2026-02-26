# Sampling regime and collection methods

## Overview
- Long-term study of wild banded mongooses (Mungos mungo) on Mweya Peninsula, Queen Elizabeth National Park, Uganda.
- Population typically 10–12 social groups; groups ~20 adults plus offspring.
- Individuals uniquely marked; regular trapping every two months; 1–2 individuals per group equipped with radio collars.
- Data collected on group composition, life history, reproductive behavior, and intergroup interactions (IGIs).

## Study population and sampling regime
- Groups are habituated; most activities conducted with observers within 5 meters.
- Field visits every 1–3 days for at least 20 minutes; daily checks during pregnancy to record birth dates.
- Pups tracked from ~30 days old; pups marked and tail-tip tissue samples taken for genetic analyses (2 mm).
- Genetic analyses use a microsatellite panel (43 markers standard; 35 markers for subset).

## Fieldwork instrumentation and data capture
- Data recording: Psion II data loggers (until 2014) and a bespoke Mongoose 2000 app on Samsung Galaxy tablets.
- Data imported into an MS Access database.
- Instrumentation includes radio collars (~30 g) with 20 cm antennas.
- Field instruments calibrated to factory settings.

## Analytical methods and data products
- Mortality from intergroup conflict (2000–2015): identify adult deaths due to intergroup fighting; calculate exposure in mongoose-years and mortality rates by sex and group.
- Fitness benefits from intergroup conflict (2000–2019): metrics include lifetime extra-group offspring (LEGO) and lifetime reproductive success (LRS); pedigree-based maternity/paternity assignments with assignment probabilities of 90% (full 43-marker panel) or 95% (subset 35-marker panel); total IGIs experienced and age at death tracked.
- Frequency of IGIs relative to female estrus (2000–2019): classify IGIs by focal vs. rival group estrus states; analyze 539 IGIs with known estrus states; compute counts and days in each estrus state.

## Quality control and data validation
- Mongoose 2000 app includes internal validation checks (e.g., presence required to collect further data).
- Data quality checks performed with MS Access queries and bespoke R code to detect inconsistencies (e.g., multiple death records for an individual).

## Data structure and metadata
- Data stored as three CSV files with explicit content descriptions and column schemas.

1) Mortality rates from intergroup conflict (2000–2015)
   - Columns: group.id, sex, death, exposure, mortality.rate, etc.
   - Metrics: deaths due to intergroup conflict by group and sex; mortality rate per year.

2) Fitness benefits from intergroup conflict (2000–2019)
   - Columns: sex, lego (lifetime extra-group pups), lrs (lifetime reproductive success), number.igis, age.at.death.
   - Metrics: LEGO and LRS by individual; lifetime intergroup interactions; age at death.

3) Frequency of IGIs by estrus state (2000–2019)
   - Columns: focal.group.id, rival.group.id, focal.rival.estrus.state, number.igis, days.in.estrus.state, olre, unique observation identity (olre).
   - States: FE RE, FE RNE, FNE RE, FNE RNE; counts and observation duration.

## Data governance and stewardship implications
- Documentation and provenance: clear lineage from field collection to MS Access to CSV outputs; include pedigree and microsatellite data lineage.
- Standards and metadata: ensure consistent variable definitions (e.g., estrus states, exposure in mongoose-years, assignment probabilities) and provide a detailed data dictionary.
- Formats and interoperability: CSV files provide broad accessibility; consider formal metadata schemas for cataloging and discoverability.
- Data storage and updates: long-running study with periodic updates; maintain versioning, archival copies of MS Access and the Mongoose app, and update the CSV data products as new data become available.
- Data quality and reproducibility: preserve QC procedures (internal app checks, QC queries, R scripts) and ensure reproducible analysis pipelines.
- Access and collaboration considerations: document data access licenses, usage restrictions, and proper attribution for researchers reusing the data; ensure metadata supports data discovery for external users.