# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview
- Two CSV datasets describing forest inventory in the Ankasa Conservation Area, Ghana, over 2018–2021 (with a COVID-19 related interruption in 2019).
- Scope: 50 consecutive 1-hectare forest plots within a 50-ha area; targeted trees and lianas with stem diameter at breast height (DBH) ≥ 25 cm.
- Data capture includes: tree and liana measurements, live/dead status, and lightning strike events with subsequent observations.
- Datasets:
  - Forest_inventory_AnkasaGhana_2018_2021.csv: measurements for 2,589 trees and 32 lianas across 50 plots.
  - Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of trees struck by lightning, including species, diameter, post-strike status, fuse status, and follow-up observations.
- Project provenance: part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).

## Data structure and contents
- Forest_inventory_AnkasaGhana_2018_2021.csv
  - Key columns: Tree_id, census_date, POM (Point of Measurement in cm), D (Diameter in cm at POM), Tree_status (codes for alive/dead with modifiers), and related notes on condition (e.g., hollow, uprooted, coppiced).
  - POM typically 130 cm; deviations noted to avoid buttress/deformity.
  - Tree_status codes include combinations such as A (Alive) with modifiers (e.g., AN Alive Normal, AB Alive Broken, AH Alive Hollow, AD Dead, DL Dead Lightning, etc.).
- Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
  - Key columns: Country, Site, Plot, Tree_id, Species, census_strike_date, POM_strike, D_strike, Tree_status_after, Fuse_status, Observations_after.
  - D_strike and POM_strike reflect diameter/measurement at the strike date; Tree_status_after captures post-strike condition with status codes similar to the forest inventory.
  - Fuse_status indicates fuse condition at strike date; Observations_after documents field observations post-strike.
- Codes and definitions
  - Tree_status and Tree_status_after use letter codes (A = Alive, D = Dead) with second-letter combinations indicating condition (e.g., AN, AB, AH, DL, etc.).
  - POM and D fields follow standard forestry measurement conventions, with D=0 when the tree is dead or not measured.
- Data coverage notes
  - 2,589 tree records plus 32 lianas in the inventory dataset.
  - Lightning data covers 4 strikes recorded between June 2018 and July 2021.

## Data collection methods and quality control
- Field design: 50 plots (1 ha each) within a 50-ha plot area; all trees and lianas with DBH ≥ 25 cm tagged and measured in each census.
- Measurements and status: recorded diameter at the standard measurement point (POM) and tree living status; notes on conditions (e.g., broken, hollow, uprooted, canopies affected).
- Lightning detection
  - Each measured tree equipped with a Rogowski Coil sensor to detect lightning strikes non-invasively.
  - Quick visual checks of fuse status to confirm lightning event; additional notes on tree condition and surrounding damage.
- Data quality controls
  - Checks for unit errors and ambiguous values; flagged records undergo paper field notes review or resurvey when possible.
  - Missing values exist where field records were ambiguous or not retrievable; unresolved issues are flagged for future review.
- Documentation and provenance
  - Data were collected between 2018–2021, with a pandemic-related interruption in 2019.
  - Data collection and sensor usage were part of a structured field program with standard operating procedures and retrospective quality checks.

## Data governance, provenance, and availability
- Data lineage: field measurements and lightning observations compiled from a defined 50-ha study area; linked inventory and lightning-strike datasets.
- Provenance details: project-funded data collection under the NERC grant NE/P001564/1.
- Access and hosting: two CSV files are attached to the documentation; no license or access restrictions are specified in the text. Consider establishing a data dictionary, versioning, and licensing for reuse.
- Metadata needs: explicit data dictionary for all codes (Tree_status, Tree_status_after, fuse status) and definitions of POM, D, and measurement conventions to support interoperability and re-use.

## Known issues, limitations, and challenges
- COVID-19 interruption in 2019 leading to incomplete time-series data for that year.
- Missing values and ambiguous field notes requiring potential resurvey or careful imputation guidelines.
- Diversity of data fields and codes requires careful standardization for integration with other datasets; some records may rely on bespoke field notes.
- Potential non-interoperability considerations due to bespoke Rogowski Coil sensor data and field-specific measurement conventions.

## Stewardship recommendations and actions
- Data documentation
  - Create a comprehensive data dictionary detailing all columns, units, and coded values (especially Tree_status, Tree_status_after, and fuse_status).
  - Document POM conventions, measurement rules, and handling when trees are dead or unmeasured (POM=0).
- Data quality and validation
  - Maintain and publish data quality reports summarizing missing values, flagged records, and resurvey outcomes.
  - Establish clear procedures for updating records when follow-up surveys occur; implement versioning for corrected data.
- Data governance and sharing
  - Define data licensing, access controls, and reuse terms to enable broader use while protecting sensitive field information if applicable.
  - Provide guidance on data integration with external datasets (e.g., other forest plots, lightning datasets) including variable mappings and code harmonization.
- Metadata and discoverability
  - Ensure machine-readable metadata is available (field definitions, data lineage, collection methods, instrument details).
  - Register the datasets in a data portal with unified metadata and a stable DOI or persistent identifier if feasible.
- Maintenance and updates
  - Establish a routine for updating the datasets with future census data, including changelog documentation.
  - Track data provenance changes and maintain a data steward contact for queries.