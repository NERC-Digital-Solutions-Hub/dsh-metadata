# Brief description of the dataset

- The dataset contains weekly water quality monitoring data for eight sites along the River Thames and sixteen major tributaries, spanning March 2009 to December 2023.
- Parameters include nutrients and ions, pigments, physico-chemical properties, and metals:
  - Nutrients: total phosphorus (TP), total dissolved phosphorus (TDP), soluble reactive phosphorus (SRP), dissolved and total nitrogen, chlorophyll a.
  - Nitrogen species, silicon, temperature, pH, Gran alkalinity, suspended solids, dissolved organic carbon.
  - Major dissolved anions: fluoride, chloride, bromide, sulfate; major dissolved cations: sodium, potassium, calcium, magnesium, boron.
  - Metals: dissolved and total iron, manganese, zinc, copper (measured 2010–2013 for certain elements; later measurements may vary by element).
- Most sites are near Environment Agency gauging stations; daily river flow context can be obtained from the National River Flow Archive (NRFA).

## Scope, period, and structure

- Temporal coverage: 2009–2023 (with some variables measured only within narrower subperiods, e.g., cation data 2009–2016; some elemental analyses paused after 2013).
- Data presentation order: monitoring site order first, then dates in ascending order.
- Sampling cadence: bulk weekly samples taken Monday or Tuesday; field measurements (temperature, pH, conductivity, redox) from March 2013 to present; dissolved oxygen measured since July 2018.
- Spatial context: eight Thames sites plus sixteen major tributary sites.

## Collection, measurement, and analytical methods (highlights)

- Field sampling and handling:
  - Bulk river samples collected weekly; field measurements performed in situ or shortly after sample collection.
  - Subsamples filtered through 0.45 μm membranes; samples stored at 4°C in the dark before analysis.
- In-field measurements:
  - Temperature, pH, conductivity, redox potential (via Myron Ultrameter; DO via YSI ProSolo since 2018).
- Laboratory analyses (selected methods and instruments):
  - pH: calibrated pH meter with NIST-traceable buffers.
  - Alkalinity: acidimetric titration to pH 4 and 3.
  - Suspended solids: filtration, drying, reweighing.
  - Chlorophyll a: filtration, acetone extraction, spectrophotometric measurement.
  - Phosphorus: TP and TDP by digestion with acidified persulfate; SRP by colorimetry (Murphy & Riley method with modifications).
  - Silica: molybdate reaction with tin(II) chloride reduction; spectrophotometric quantification.
  - Ammonium: indophenol-blue colorimetric method.
  - DOC/TDN: thermal oxidation (2010) and Elementar Vario Cube (from 2011).
  - Anions (F, Cl, nitrite, nitrate, sulfate) by ion chromatography.
  - Cations: ICP-OES after acidification.
- Quality control:
  - All analyses (except suspended solids) run with Aquacheck QC standards.

## Data quality, units, and data handling

- Data quality notes:
  - Missing data are represented as blanks; values below detection limits are marked as nd (not detectable).
  - QA includes routine use of reference QC standards (Aquacheck).
- Units and nomenclature:
  - Detailed units provided for each parameter (e.g., TP, TDP, SRP in μg P/L; chlorophyll a in μg/L; dissolved/total metals in mg/L or μg/L as applicable; temperature in °C; pH without units; alkalinity in μEq/L; solids in mg/L; various ions in mg/L or μg/L; conductivity in μS/cm; DO in %sat or mg/L).
- Data structure for GIS use:
  - Site-order primary, with temporal ordering by date, enabling straightforward join to geospatial site data and time-series analyses.

## Spatial data context and integration

- The dataset is suitable for GIS mapping and spatial-temporal analyses when linked to site coordinates and site metadata.
- Site locations and gauging context are described in Supporting Documents (SiteLocations_2009_2023); NRFA provides daily flow data for hydrological context.
- To create map-based products, link each measurement row to a fixed site polygon/point and to a date, then optionally join with flow, land-use, or catchment boundary layers.

## Practical notes for GIS workflows

- Data integration:
  - Combine site-order data with SiteLocations_2009_2023 for coordinates; ensure alignment of site identifiers across datasets.
  - Consider temporal alignment when comparing variables with different measurement periods (e.g., cation data 2009–2016 vs. others).
- Data cleaning:
  - Address missing values and nd detections; retain data provenance from QA standards.
  - Normalize or harmonize units if integrating with other datasets.
- Potential uses:
  - Create time-series maps of nutrient and metal concentrations by site.
  - Visualize seasonal or annual trends and compare tributaries vs. main river sites.
  - Overlay with hydrological context from NRFA flow data to explore concentration-flow relationships.

## References and provenance

- Methods and analytical references include Eisenreich et al. (phosphorus), Leeks et al. (LOIS river monitoring), Marker et al. (chlorophyll pigment standardization), Mullin & Riley (silicate determination), Murphy & Riley (phosphorus colorimetry), Neal et al. (phosphate measurement issues), and related QA standards.