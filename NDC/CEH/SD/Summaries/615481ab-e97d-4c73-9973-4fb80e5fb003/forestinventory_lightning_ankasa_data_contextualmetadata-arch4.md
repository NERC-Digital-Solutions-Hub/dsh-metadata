# Forest inventory and lightning strikes data from Ankasa Conservation area, Ghana, from 2018-2021

## Overview of data
- Two CSV datasets are provided:
  - Forest_inventory_AnkasaGhana_2018_2021.csv: measurements for trees and lianas across 50 consecutive 1-ha forest plots in Ankasa Conservation Area; includes 2589 individual trees and 32 lianas with diameter at breast height and living status (alive or dead, plus detailed sub-codes).
  - Lightning_strikes_Datasummary_Ankasa_2018_2021.csv: subset of the forest inventory trees that were struck by lightning; includes species, diameter, status after strike, fuse status, and post-strike observations.
- Timeframe and study context:
  - Data collected from June 2018 to July 2021; the 2019 census was interrupted by the COVID-19 pandemic.
  - Part of the NERC project “Lightning: An invisible driver of tree mortality in the tropics?” (Grant NE/P001564/1).
- Scope:
  - Site: Ankasa Conservation Area, southwestern Ghana; forest type is wet/moist evergreen with high diversity.

## Data collection methods
- Plot and measurement design:
  - 50 ha area divided into 50 one-hectare plots; all trees and lianas with DBH ≥ 25 cm tagged and measured each census.
  - Variables recorded include stem diameter at 1.3 m (POM) or adjusted when buttressed/deformed; tree status notes (e.g., alive, broken, hollow) and death mode (e.g., uprooted, standing).
- Quality controls:
  - Checks for unit inconsistencies and ambiguous values; where possible, field notes are consulted or resurveyed; unresolved issues flagged for future checks.
- Lightning detection:
  - Each measured tree fitted with a custom Rogowski Coil sensor to detect lightning strikes non-invasively; visual checks of fuse and electrical conductivity recorded.
  - For struck trees, damage details documented at species level and in the surrounding area (e.g., canopy gaps, sapling mortality).

## Details of data structure

### Forest_inventory_AnkasaGhana_2018_2021.csv
- Key columns and definitions:
  - Tree_id: original field tag for the stem.
  - Census_date: date of measurement (day/month/year).
  - POM: Point of measurement for diameter (usually 130 cm; adjusted to avoid buttress/deformity; 0 if dead and not measured).
  - D: Diameter (cm) at the POM; 0 if dead and not measured.
  - Tree_status: code for tree status (e.g., A = alive, D = dead) with subcodes (e.g., AN = Alive Normal, AB = Alive Broken, AH = Alive Hollow, DL = Dead by lightning, etc.).
- Notes:
  - The dataset includes status codes that combine multiple conditions (e.g., AUP = Alive uprooted, AL = Alive partially burned).
  - Missing values may occur where field records were ambiguous or missing.

### Lightning_strikes_Datasummary_Ankasa_2018_2021.csv
- Key columns and definitions:
  - Country, Site, Plot: geographic and plot identifiers.
  - Tree_id: original field tag for the stem.
  - Species: taxonomic identification.
  - census_strike_date: date of census when lightning marks were observed (month/year).
  - POM_strike: diameter measurement point for the strike census (cm; typically 130 cm; 0 if not measured).
  - D_strike: diameter (cm) at current POM for the strike census (0 if not measured).
  - Tree_status_after: status after strike using the same code system as Forest_inventory (e.g., A = alive, D = dead; with subcodes).
  - Fuse_status: fuse condition at strike date.
  - Observations_after: notes on observations after the strike (field observations).
- Notes:
  - Records cover 4 lightning strike events; provides linkage to the broader inventory dataset.

## Data quality, limitations, and considerations
- Missing data:
  - Missing values exist where field records were ambiguous; some diameters or POMs may be zero when not measured due to tree death or accessibility.
- Interruption:
  - COVID-19 disrupted 2019 census activities, affecting continuity of data.
- Metadata and standards:
  - Detailed column definitions and status codes are provided to support interpretation and harmonization with the broader dataset.
- Data provenance:
  - Measurements include a standardized measurement protocol (POM, diameter, status coding) and quality checks to flag potential issues for resurvey or future verification.

## Context for data strategy and reuse
- Purpose and potential analyses:
  - Enables investigation of lightning as a driver of tree mortality in tropical forests, in relation to tree diameter, species, and surrounding stand structure.
  - Facilitates cross-cutting analyses between general forest inventory data and lightning-specific outcomes (e.g., post-strike mortality, damage patterns).
- Governance and stewardship implications for Data Leaders:
  - Clear linkage between inventory data and event-specific data (lightning strikes) supports integrated data products and potential co-ownership across teams.
  - Rich metadata and explicit status codes aid discoverability, interoperability, and reuse across partners and networks.
- Community and collaboration considerations:
  - Data collected under a multi-partner framework (NERC project) with explicit documentation supports wider community use and potential alignment with other tropical forest mortality studies.

## Takeaways for applying the data
- Use the Forest_inventory dataset to analyze baseline structure, live/dead status, and diameter distributions across the 50 plots.
- Use the Lightning_strikes dataset to assess the immediate and near-term effects of lightning on individual trees, aligned by Tree_id and census dates.
- Leverage the detailed status codes and POM adjustments to ensure consistent interpretation of historical measurements and to enable robust quality checks.
- Consider data gaps (e.g., 2019 disruption) when modeling mortality drivers and plan for targeted imputation or sensitivity analyses where appropriate.
- Ensure metadata, data standards, and discoverability are maintained to support cross-institution collaboration and reuse.