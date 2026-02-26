# Overview

- This dataset details the seasonal abundance of all life stages of the mosquito species Culex pipiens at the Centre for Ecology & Hydrology (CEH) Wallingford field site in 2015. Immature stages were monitored March–October 2015 (eggs, larvae, pupae), while adult counts were collected April–October 2015.

## Field site, design and sampling regime

- Location: CEH Wallingford field site (coordinates provided); adjacent weather station noted.
- Immature sampling: four 450 L circular water butts placed in close proximity (Butts 1–4) with varying exposure to sunlight and shelter.
  - Hay infusion used to stimulate larval development (hay bags placed Jan–Mar; removed end of March).
  - A HOBO water-temperature logger recorded hourly surface water temperature per butt.
  - Egg rafts counted at 10:00 on Monday, Wednesday, and Friday (sampling March–October 2015).
  - For larval/pupal sampling: 500 mL dips taken from the north, south, east, and west edges of each butt; middle of the butt excluded due to edge-dwelling larvae/pupae.
  - In cases with large counts, photographs of trays used for counting; subsequent manual counts performed in software (Microsoft Paint).
  - Monthly morphological identification of 4th instar larvae from each butt (20 larvae per butt when feasible) to species level; larvae killed before examination by boiling water.
- Adult sampling: Four John W. Hock Miniature Downdraft Blacklight (UV) traps baited with dry ice.
  - Operational period: nightly from 14 April to 2 October (with some gaps due to staff/dry ice issues).
  - Traps placed at varying locations around the site (distances from butts ~80–200 m).
  - Traps run 17:00–09:00; collected adults frozen and identified by microscopy in the lab (males not recorded).

## Data collection instruments and workflows

- Trapping and counting methods documented; identification performed using standard dissection and light microscopy.
- All data are recorded and stored with explicit linkage to date, location (butt or trap), and life-stage or species.

## Nature, units and recording of values

- Egg abundance: counts of egg rafts per butt (Egg_abundance_2015_Wallingford.csv).
- Larval and pupal abundance: counts per sampling occasion, per butt, including instar classifications (Larval_abundance_2015_Wallingford.csv; Pupal_abundance_2015_Wallingford.csv or combined larval/pupal structure as applicable).
  - Larval data include counts by corner (N, E, S, W) and instar stage (L1/2; L3/4).
- Adult abundance: counts of adult female Cx. pipiens per trap per date (Adult_abundance_2015_Wallingford.csv).
  - Additional species counts (e.g., Cs. annulata, Ae. geniculatus) recorded if identified.
  - NA values indicate occasions when traps were not run.
- Larval identification: dates and numbers of 4th instar larvae identified, including how many were Cx. pipiens and associated butt sources (Larval_identification_2015_Wallingford.csv).
- Temperature: hourly surface water temperatures per butt (Water_temperatures_2015_Wallingford.csv).
- Temperature units: degrees Celsius.

## Data quality control and validation

- Validation of larval/pupal counts: initial field counts cross-checked with counts derived from photographed tray contents; comparisons between direct counts and photo-based counts showed consistent results.

## Data structure and file contents

- Six CSV files:
  - Egg_abundance_2015_Wallingford.csv
    - Columns: Date, Butt no (1–4). Rows: daily egg-raft counts per butt.
  - Larval_abundance_2015_Wallingford.csv
    - Columns: Date, N, E, S, W (butt corners); L1/2 (first/second instars); L3/4 (third/fourth instars). Rows: counts per butt per date.
  - Pupal_abundance_2015_Wallingford.csv
    - Columns: Date, Butt-specific sections and pupal counts (structure aligned with larval data; per butt).
  - Adult_abundance_2015_Wallingford.csv
    - Columns: Date, Location (trap), Cx. pipiens (adult females), Cs. annulata, Ae. geniculatus (other species) identified; NA notes for unrun traps.
  - Larval_identification_2015_Wallingford.csv
    - Columns: Date of identification, number identified, number identified as Cx. pipiens, Butt(s) of origin.
  - Water_temperatures_2015_Wallingford.csv
    - Columns: Date, Time, Butt, Temperature (°C) per hourly measurement.

## Temporal coverage and units

- Timeframe:
  - Immature sampling: March–October 2015 (eggs, larvae, pupae).
  - Adult sampling: April–October 2015 (adult females).
- Temperature sampling: March 3 to November 2, 2015 (hourly per butt).

## Data governance considerations for Data Stewards

- Metadata needs:
  - Detailed methodological notes on sampling times, dip method, and counting rules for young instars, to ensure consistent reuse.
  - Clear linkage between egg, larval/pupal, and adult data through common dates and butt/trap identifiers.
  - Documentation of any deviations or gaps (NA entries) and their causes (staff shortages, dry ice delivery issues).
- Data quality and provenance:
  - QC performed via cross-checking photo-based counts with direct counts on initial sampling days.
  - Together with species identification steps, ensure traceability from field collection to laboratory analysis.
- Accessibility and interoperability:
  - Data are organized into six named CSV files with standardized columns per life stage, enabling programmatic access and integration with other datasets.
  - Note potential format variations across files (e.g., whether larval and pupal data are in separate files vs. combined formats) and rely on file headers to interpret columns accurately.
- Usage considerations:
  - Missing data (NA) in adult counts should be accounted for in analyses; document reasons for omissions.
  - Males not recorded; analyses focusing on females only unless otherwise specified.

## Provenance and site context

- Site-specific coordinates and proximity of temperature logger and weather station documented, providing environmental context essential for data interpretation and reuse in related studies.