# A brief description/overview of the data being described

## Scope and contents
- PULA water quality data folder comprises 25 CSV files, one per indicator, covering: Total Organic Carbon (TOC), Chloride, Fluoride, Bromine, Sulfate, Potassium, Aluminium, Calcium, Iron, Magnesium, Sodium, Phosphorus, Chromium, Manganese, Cobalt, Nickel, Copper, Zinc, Arsenic, Selenium, Molybdenum, Cadmium, Lead, and stable isotopes δD and δ18O.
- Data collection period: February 2017 – May 2018.
- Collaborators: Botswana Department of Water Affairs, Botswana International University of Science and Technology, University of Aberdeen.

## Sampling design and regime
- Sample types: groundwater (GW) and surface water (SW) across the Gaborone Reservoir catchment, south-west Botswana.
- Total sampling occasions: 287, across 41 days and about 15 campaigns, aligned with flood-drought-flood cycles.
- Spatial coverage aimed to capture regional variability and practical accessibility constraints.
- Surface water: grab samples from reservoirs and streams; groundwater: pumped grab samples after flushing wells.
- Documentation: sampling locations named per Botswana DoWA; sampling dates captured; field sampling conditions logged.

## Collection, generation, and transformation
- For each occasion:
  - 2 × 30 mL bottles for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb (acidified with 5% HNO3 in the field).
  - 2 × 15 mL bottles for TOC analyses.
  - 2 × 10 mL bottles for stable isotopes and for Al, Ca, Fe, K, Mg, Na.
  - Duplicates: one bottle analyzed, the other reserved for re-runs.
- Field labeling with sampling name and date; data collection logs maintained separately.
- Samples refrigerated and shipped to University of Aberdeen in four batches; analyses conducted upon arrival.

## Analytical methods and instrumentation
- P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb: Agilent 7900 ICP-MS (University of Aberdeen, Chemistry).
- Al, Ca, Fe, K, Mg, Na: MP-AES (University of Aberdeen, Biological Sciences).
- TOC: LABTOC instrument (University of Aberdeen, Biological Sciences).
- δD and δ18O: TWIA-45-EP LGR instrument (University of Aberdeen, Geosciences).
- Analyses performed following standard instrument-specific procedures.

## Calibration, limits, and data quality
- Recorded calibration and detection details vary by analyte and campaign period.
- Notable issues:
  - Some results exceed maximum calibration range; interpretation requires caution.
  - Pb data largely problematic; methodology deemed unsuitable, resulting in incomplete Pb data.
  - Many concentrations for several elements fall below detection limits; CSVs mark these as <LOD.
  - Detection limits and calibration ranges differ before and after Nov 2017 and Dec 2017, and for some elements across periods.
- Data structure notes: top row in each CSV defines column metadata; unit conventions and blank cells indicate missing values.

## Data structure and metadata
- Each CSV file begins with a header row detailing columns.
- Columns, in order: sample type (SW or GW), sampling location name ( Botswana DoWA nomenclature), longitude, latitude, elevation (m, when available), followed by sampling dates.
- Coordinates are provided in the UTM system; latitude/longitude given in decimal degrees; elevation in metres.
- Dates use the dd/mm/yy format.
- Blank cells denote missing values; multiple sampling dates per file correspond to different campaigns.

## Data provenance, collaboration, and governance
- Data generated through multi-institution collaboration (DoWA, BIUST, University of Aberdeen) as part of the NERC-funded PULA project.
- Field and laboratory workflows, sample labeling, and logs are documented; some data processing steps (e.g., re-runs) reflected in sampling and analysis timing.
- Data are organized by indicator, with separate files per analyte to enable targeted analyses.

## Accessibility, caveats, and potential uses
- Caution advised when using data due to calibration range limitations and detection-limit issues, especially for Pb and several metals.
- Useful for:
  - Assessing spatial and temporal patterns in groundwater and surface water quality within the Gaborone catchment.
  - Evaluating impacts of extreme rainfall and flooding on water quality across heterogeneous physiographic settings (geology, land use).
  - Supporting metadata-driven data discoverability and cross-study integration, given explicit recording of sampling conditions, locations, and units.
- Limitations to consider in analyses: incomplete Pb data, many <LOD values, variable calibration ranges across campaigns, and potential gaps in metadata alignment across files.