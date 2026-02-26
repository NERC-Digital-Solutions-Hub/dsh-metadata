# Stem respiration in human-modified forests of Eastern Amazonia

## Overview
- Dataset: StemRespirationData.csv containing stem respiration measurements from trees in 20 Amazonian forest plots.
- Disturbance gradient: undisturbed primary (n=5), logged primary (n=5), logged-and-burned primary (n=5), and secondary forests (n=5).
- Temporal coverage: June 2015 to July 2018.
- Project context: part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Data collection methods
- Collars installed on at least 13 trees per plot, 20 cm above dendrometers, across five DBH classes.
- PVC collars (~5 cm high, 10 cm diameter) connected to an infrared gas analyser (EGM5) to measure stem CO2 efflux.
- Measurements taken every 3 months; when a tree died, collar removed and replaced in the same size class if possible.
- N/A entries denote missing measurements; reasons recorded in the notes column.

## Data structure and fields
- File: StemRespirationData.csv
- Key columns:
  - Date: date of data collection
  - Catchment: microcatchment (~5,000 ha)
  - Transect: plot number within catchment
  - Plot code: unique code combining catchment and transect
  - Forest: disturbance class before the 2015–16 El Niño
  - Fire: whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire)
  - Tree TAG: identifier for the individual with the collar
  - Time: exact sampling time
  - Collar height: height at collar
  - CO2 initial: CO2 concentration at start of measurement
  - CO final: CO2 concentration at end of measurement
  - Flux: measured stem CO2 efflux
  - Field notes: field processing notes
- Missing data handling: N/A entries present; reasons documented in the notes column.

## Geolocation information
- Coordinates for plots are provided (lat/long) for multiple plot codes (e.g., 112_12, 112_8, 129_10, etc.), enabling spatial analyses and mapping of study plots.

## Provenance and accessibility
- Authors: Berenguer E.; Rossi L. C.; Seixas, M. M. M.; Barlow J.
- Data collection supported by the NERC HMTF program; dataset is described as part of the project outputs and attached as StemRespirationData.csv.

## Governance and stewardship considerations
- Metadata completeness: ensure clear definitions, units (where applicable), and time formats; explicitly document measurement protocols and any deviations.
- Data quality: capture QA details from field notes; document collar replacements and any data exclusions.
- Interoperability: maintain consistent plot coding (Plot code) and harmonize coordinates with other datasets if integrated.
- Access and licensing: verify data sharing permissions and licensing terms beyond what is described; include citation information (authors and grant).
- Update process: outline how new measurements would be added and how versioning is handled, given measurements occurred quarterly.
- Documentation: provide a data dictionary and processing steps to support reuse and reproducibility.