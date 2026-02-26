# A brief description/overview of the data being described

- PULA water quality data folder contains 25 CSV files, each for a different water quality indicator.
- Indicators include Total Organic Carbon (TOC), Cl, F, Br, SO4, K, Al, Ca, Fe, Mg, Na, P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb, and stable isotopes δD and δ18O.
- Data collection period: February 2017 – May 2018.
- Collected by the Botswana Department of Water Affairs with scientists/students from BIUST and the University of Aberdeen.

## Experimental design and sampling regime

- Sample types: groundwater (GW) and surface water (SW) from the Gaborone Reservoir catchment area, SW streams and reservoir water; GW involve pumped grab samples after flushing wells.
- Total sampling occasions: 287 across 41 days, concentrated around ~15 campaigns tied to flood-drought-flood cycles.
- Spatial coverage aimed to capture variability in geology and land use; practical accessibility considerations influenced site selection.
- Sampling campaigns produced heterogeneous spatial/temporal coverage.

## Collection, generation, and transformation methods

- For each occasion, three analysis types used:
  - P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb: two 30 mL bottles (acidified in the field with 5% HNO3).
  - TOC: two 15 mL bottles.
  - Al, Ca, Fe, K, Mg, Na: two 10 mL bottles.
- Two samples per analysis type were collected for initial analysis and re-runs if needed.
- Field labeling with sampling name/date; a data collection log recorded local sampling conditions.
- Samples refrigerated and shipped to the University of Aberdeen in four batches for analysis.
- Analyses timeline:
  - Data collected up to May 2017 analyzed in June–July 2017.
  - Re-runs for certain metals completed in July 2018.
  - Data collected Jun 2017–Jul 2017 analyzed Aug 2017; Aug 2017–Jul 2018 analyzed Dec 2017; Jan–May 2018 analyzed July 2018.

## Fieldwork and laboratory instrumentation

- P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb analyses: Agilent 7900 ICP-MS (University of Aberdeen, Chemistry).
- Al, Ca, Fe, K, Mg, Na analyses: MP-AES (University of Aberdeen, School of Biological Sciences).
- TOC analyses: LABTOC (University of Aberdeen, School of Biological Sciences).
- Stable isotopes (δD, δ18O): TWIA-45-EP LGR (University of Aberdeen, School of Geosciences).

## Calibration, data structure, and units

- Parameters and units:
  - TOC: mg/L; Cl: mg/L; F: mg/L; Br: mg/L; SO4: mg/L; K, Al, Ca, Fe, Mg, Na: mg/L; P: ug/L; Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb: ug/L; δD and δ18O: ‰VSMOW.
- Calibration and detection:
  - LoD values provided for data up to Nov 2017; some data beyond calibration range flagged; Pb data largely incomplete due to method suitability.
  - Several elements show >1/3 of samples below LoD (Cu, Zn, Cd, Pb, Al, Fe, F, Br) in the reported data subset.
- Data files and structure:
  - Each of the 25 CSV files begins with a header row describing columns.
  - Columns include: water type (SW or GW), sampling location name (Botswana DWA nomenclature), longitude, latitude, elevation (m), followed by sampling dates.
  - Coordinates are in UTM; latitude/longitude in decimal degrees; blanks indicate missing values.
  - Sampling date format: dd/mm/yy.

## Data provenance, quality, and intended use

- Data provenance: collected as part of the NERC-funded PULA project to evaluate impacts of extreme rainfall and flooding on water quality across surface and groundwater with varied physiography.
- Quality notes important for analysts:
  - Some measurements exceed calibration range; interpret with caution.
  - Multiple analytes have substantial portions of values below detection limits; consider censoring or imputation strategies.
  - Pb data incomplete; data for some elements may be missing or flagged as <LOD.
- Availability and context:
  - 25 indicator-specific CSVs plus separate data collection logs (not included here) provide context on sampling conditions.
  - Dataset designed to support correlation analyses, pattern detection across water types and locations, and development of predictive models related to flood/drought impacts on water quality.
- Practical considerations for analysts:
  - Two-sample replication per analysis aids quality assurance but may influence missingness if re-runs occurred.
  - Spatial coverage focused on catchment variability; results may be best generalized within similar geographies and hydrological regimes.
  - Data can be linked to sampling metadata (dates, locations, coordinates, elevations) for geospatial analyses and temporal trend assessments.