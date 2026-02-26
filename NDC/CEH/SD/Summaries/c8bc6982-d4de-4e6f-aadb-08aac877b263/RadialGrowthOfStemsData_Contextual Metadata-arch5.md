# Radial growth in stems in human-modified forests of Eastern Amazonia

## Overview
- Dataset name: RadialGrowthOfStemsData.csv
- Contents: Monthly radial growth measurements of stems (in mm) from 20 Amazonian forest plots collected between December 2014 and September 2018, as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Study design: Plots span a disturbance gradient prior to the 2015-16 El Niño, categorized as undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.
- Scope: Includes trees and lianas with dendrometer bands installed across five DBH size classes.
- Primary purpose: Provide data to quantify radial growth responses across disturbance histories and enable subsequent data sharing and reuse with appropriate governance.

## Data collection methods
- Plot design: 20 plots, each 250 x 10 m, stratified into five DBH size classes; at least 50 dendrometer bands per plot (10 bands per size class) plus bands on all lianas ≥10 cm DBH.
- Dendrometers: Installed 10 cm above the DBH measurement point; initial marking followed by a one-month settle period, with first growth measurement taken five months after marking, then monthly thereafter.
- Maintenance: Damaged bands replaced and re-installed; dead stems removed and replacement bands installed on another tree in the same size class.
- Growth interpretation: Negative growth values may occur due to water loss from bark and are not corrected; positive growth reflects actual tissue accretion plus water-related expansion.
- Plot coordinates: Specific latitude/longitude pairs provided for each plot (20 sets listed).

## Data structure and variables
- Core structure: A comma-separated values (CSV) dataset with columns covering catchment, plot identifiers, forest disturbance class, El Niño fire status, tree tag and code, DBH, life form (Tree A, Liana C, Palm P), and re-installation status.
- Monthly data: For each month from Dec 2014 onward, two kinds of columns are present:
  - Data-MMYY: Date of the month (e.g., Data-Dec14)
  - mm-MMYY: Radial growth in millimeters for that month (e.g., mm-Dec14)
  - OBS-MMYY: Field notes for that month
- Key columns:
  - Catchment, Transect, Plot, Rainfor, Forest, Fire_ElNino
  - Tree_tag, Tree_code, DBH, Life form, Re-installed
  - Data-Dec14, mm-Dec14, OBS-Dec14 (and analogous columns for subsequent months)
- Data units: Radial growth is recorded in millimeters; DBH measured in cm; dates are monthly timestamps.

## Provenance and governance
- Source program: NERC HMTF (Grant NE/K016431/1)
- Dataset purpose: To enable understanding of radial growth responses to disturbance and to support discovery, reuse, and integration with other datasets.
- Metadata depth: Includes plot-level disturbance history, fire status, dendrometer deployment details, measurement schedule, and monthly growth records plus field notes.
- Data stewardship implications: Clear documentation of measurement protocol, zero-setting, re-installation events, and handling of negative growth supports reproducibility and auditing of data lineage.

## Access, usage, and quality notes
- Temporal scope: December 2014 to September 2018; monthly measurements provide a time-series perspective on growth dynamics.
- Spatial scope: 20 plots across a gradient of disturbance in Eastern Amazonia, with explicit coordinates for each plot.
- Data quality considerations:
  - Growth values include negative measurements due to bark water loss; no correction applied.
  - Re-installed bands and damaged-band replacements may introduce artifacts; records of re-installations help assess data continuity.
  - Data collection relied on consistent dendrometer placement and a standardized settling period; deviations may affect comparability across plots or time.
- Recommendations for data stewards and users:
  - Maintain a complete data dictionary and data dictionary linkage for all data columns (especially monthly mm-MMYY columns).
  - Ensure versioning and provenance tracking as updates or corrections occur (e.g., re-installations, damaged bands).
  - Consider mapping to standard vocabularies and formats (e.g., DBH categories, life form codes) to facilitate interoperability.
  - Preserve field notes (OBS-MMYY) as supporting information for data quality assessments and methodological transparency.

## Dataset limitations and challenges (for governance and reuse)
- Inconsistencies in initial dataset description (litterfall vs. radial growth) require careful curation and documentation to avoid misinterpretation.
- Large, long-running time-series per plot across multiple months can pose storage and interoperability challenges; robust data management practices are essential.
- Handling of negative growth values and band re-installations requires explicit metadata to maintain data integrity and comparability across plots and time.