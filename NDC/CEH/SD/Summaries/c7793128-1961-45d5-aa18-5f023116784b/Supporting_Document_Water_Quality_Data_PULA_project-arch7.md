# PULA water quality data folder

## Overview
- A dataset comprising 25 CSV files, each corresponding to one water quality indicator.
- Indicators cover major inorganic constituents, trace metals, phosphorus, and stable water isotopes (δD and δ18O).
- Temporal scope: samples collected February 2017 – May 2018.
- Collaboration between Botswana Department of Water Affairs, Botswana International University of Science and Technology, and the University of Aberdeen.
- Part of the NERC-funded PULA project evaluating impacts of extreme rainfall and flooding on surface and groundwater.

## Content and indicators
- 25 CSV files, each containing data for a single indicator:
  - Major elements and compounds (e.g., Total Organic Carbon, Chloride, Fluoride, Bromine, Sulfate, Potassium, Aluminium, Calcium, Iron, Magnesium, Sodium, Phosphorus, Chromium, Manganese, Cobalt, Nickel, Copper, Zinc, Arsenic, Selenium, Molybdenum, Cadmium, Lead)
  - Stable water isotopes (δD, δ18O)
- Each file includes data for one analysis type per sampling occasion.

## Study area and sampling design
- Groundwater (GW) and surface water (SW) samples collected around the Gaborone Reservoir catchment, SW Botswana.
- 287 sampling occasions across 41 days, conducted in ~15 campaigns aligned with flood-drought-flood cycles.
- Sampling locations chosen to capture spatial variability in geology and land use, with practicality/accessibility considerations.
- Sampling type: SW grab samples from reservoirs/streams; GW pumped grab samples after flushing wells.

## Sampling and collection methods
- For each occasion:
  - Two bottles per analysis type:
    - 2 x 30 mL for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb (acidified with 3 drops of 5% HNO3)
    - 2 x 15 mL for TOC analyses
    - 2 x 10 mL for Al, Ca, Fe, K, Mg, Na
  - One sample analysed; the other reserved for re-runs.
- Field labeling includes sampling name and collection date.
- Field data log maintained with local sampling conditions (provided separately).

## Laboratory analysis and instrumentation
- Sample handling: refrigerated in Botswana; shipped to University of Aberdeen in 4 batches.
- Analyses:
  - ICP-MS (Agilent 7900) for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb
  - MP-AES for Al, Ca, Fe, K, Mg, Na
  - TOC analyses with LABTOC
  - Stable isotopes δD and δ18O with TWIA-45-EP LGR
- Calibration and quality control:
  - Standard procedures for each instrument
  - Some results exceed calibration range; caution advised in interpretation
  - Many samples reported as below detection limit (<LOD) for several elements
  - Pb data largely incomplete due to calibration issues; data considered unsuitable for analyses

## Data structure and units
- Each CSV file:
  - Top row contains column headers in the following order: water sample type (SW/GW), sampling location name, longitude, latitude, elevation (m), then sampling dates (dd/mm/yy)
  - Location names correspond to Botswana Department of Water Affairs designations
  - Coordinates provided in UTM; latitude/longitude in decimal degrees; elevation in metres
  - Blank cells indicate missing values
- Units:
  - Most constituents: mg/L
  - Trace metals: µg/L
  - Phosphorus: µg/L
  - Isotopes: ‰VSMOW
- Dates:
  - Multiple sampling dates per location, format dd/mm/yy

## GIS and spatial considerations
- Spatial reference information included via coordinates (UTM and decimal degrees).
- Data suitable for map-based visualization of spatial patterns in water quality across the catchment.
- Be mindful of data gaps and detection-limit handling (many <LOD entries) when creating maps or performing analyses.
- Pb data incomplete; treat as missing in any spatial analyses.

## Data quality, limitations, and provenance
- Calibration range issues: some samples exceed max calibration, affecting reliability.
- Detection limits: many values reported as <LOD; interpretations should account for censored data.
- Pb data largely incomplete; methodology deemed unsuitable for complete Pb analyses.
- Temporal and spatial coverage: variable across dates and locations; not all sites sampled on every campaign.
- Data collection log and sampling protocol details exist separately from the 25 CSV files.

## Provenance and timeline
- Fieldwork and laboratory work conducted February 2017 – May 2018.
- Analyses split into four batches corresponding to data collection periods; reporting and analysis completed across 2017 and 2018.
- Project supported by NERC via the PULA initiative.