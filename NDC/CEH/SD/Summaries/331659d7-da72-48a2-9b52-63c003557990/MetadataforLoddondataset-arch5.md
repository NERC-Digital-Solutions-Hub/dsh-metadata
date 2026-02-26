# Supporting information for 'High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)'

## Data Access and Citation
- Data available from the DOI: https://doi.org/10.5285/331659d7-da72-48a2-9b52-63c003557990
- Recommended citation:
  Hawkins, C.E; Kelly, T.J.; Loewenthal, M.; Smith, R.; Dudley, A.; Leggatt, A.; Dowman, S.; Oliver, R.G.; Collins, C.D.; Clark, J.M. (2019). High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017-Sept 2018). NERC Environmental Information Data Centre. (Dataset).

## Experimental Design and Sampling Regime
- Location: Bow Brook, a headwater tributary to the River Loddon in Hampshire; monitoring near the confluence with the Loddon near Sherfield-on-Loddon.
- High-resolution data: hourly from 00:00 GMT on 08/09/2017 to 00:00 GMT on 09/09/2018.
- Daily samples: collected at 09:00 GMT from 08/09/2017 to 08/09/2018.
- Storm samples: hourly sampling during storm events from 11/09/2017 to 22/01/2018.
- Data gaps and issues: missing samples due to equipment breakdown, temperature-related issues (frozen equipment) or measurement errors; turbidity measurements began on 10 October 2017 due to a delay in the lab meter arrival.

## Collection, Laboratory and Analytical Methods
- In-field sampling and measurement:
  - Hourly water extraction with a peristaltic pump; two flow-through cells (one with TriOS OPUS UV/VIS, one with YSI 6600 V2-2).
  - TriOS OPUS UV/VIS: full spectral scan 200–800 nm (2.2 nm per pixel).
  - YSI 6600 V2-2: turbidity, ammonium, pH, conductivity, temperature, dissolved oxygen.
  - Sontek IQ flow/gauge for river flow and height at sampling point.
  - Field equipment maintained/calibrated monthly (sonde) and UV-Vis cleaned weekly.
  - UV-Vis sensor cleaned by removing from flow cell; cleaning with cotton buds and deionised water; lenses cleaned; full spectral data downloaded biweekly via TriOS interface.
- Sampling and lab analyses:
  - Daily and storm samples collected with two ISCO 6712 autosamplers; 300 ml samples in 350 ml glass bottles (to reduce pesticide sorption).
  - Lab analyses: pH, conductivity, turbidity, full UV-Vis scan (laboratory), suspended sediment, DOC via NPOC.
  - Sample handling: refrigerated at 4°C on return; filtered within 48 hours.
- Analytical methods and equipment details:
  - pH: Mettler Toledo meter; calibration with pH 4 and 7 buffers; drift checks every ~5 samples.
  - Conductivity: Mettler Toledo EasyFive; calibration with 1413 µS at 25°C; drift checks every ~5 samples.
  - Turbidity: Hanna HI-93703; standards 0, 10, 500 FTU; two measurements per sample with settling time.
  - UV-Vis: Jenway 7315 Spectrophotometer; blank corrections; drift checks with ultra-pure water; cuvettes cleaned and prepared carefully.
  - Filtering and sample prep: suspended sediments via GF/F filters; NPOC (non-purgeable organic carbon) via acidification and purging to remove inorganic carbon; appropriate blanks included.
  - Pesticide analysis: external lab (Affinity Water Ltd.) using LC-MS/MS (Agilent 6490); 12 pesticides quantified with LOD ~0.01 µg/L; samples preserved with sodium thiosulfate.
- Data provenance notes:
  - Daily and storm pesticide data provided by external lab; dataset includes detailed methodology and instrument calibration notes to support reproducibility.

## Nature and Units of Recorded Values, and Details of Data Structure
- Dataset comprises six CSV files:
  - DailyWaterQualityData.csv (366 samples) – in-field and lab measurements: Date, Flow (m3 s-1), Depth (m), 254 nm field absorbance (AU), Turbidity (NTU/FTU), Conductivity (µS cm-1), pH, Ammonium (mg L-1), lab pH and conductivity, lab turbidity (FTU), 254 nm (AU), Total Suspended Solids (g L-1), NPOC (mg L-1), 24D pesticides (µg L-1), Total pesticides, and EU limit indicators.
  - StormWaterQualityData.csv (207 samples) – storm-by-storm: Date, Time, Flow, Depth, 254 nm, Turbidity (field and lab), Conductivity, pH, Ammonium, lab pH/conductivity, turbidity measurements (5 min and 0 min), 254 nm, TSS, NPOC, 12 pesticides, Total pesticides, EU limits.
  - HighFrequencySensorDataFlowandSonde.csv (8332 samples) – high-frequency field data: flow, stage, mean velocity, total volume, area, depth, river temperature; together with YSI 6600 parameters: temperature, conductivity, pH, ammonium, turbidity, and DO% (as DO% of saturation) and DO in mg/L.
  - HighFrequencyDataOpticalScan.csv (8364 samples) – raw optical scans from TriOS OPUS: DateTime, Date, Time, Absorption across 197.976–720.86 nm (AU).
  - DailyOpticalScansBlankCorrected.csv (366 samples) – blank-corrected daily lab optical scans: 200–800 nm in 2 nm increments (AU); some missing dates noted.
  - StormOpticalScansBlankCorrected.csv (194 samples) – blank-corrected storm optical scans: 200–800 nm in 2 nm increments (AU); notes on missing data and event-based grouping.
- Units:
  - Flow: m3 s-1; Depth: m; Velocity: m s-1; Area: m2; Temperature: °C; Conductivity: µS cm-1; pH: pH; Turbidity: NTU/FTU; 254 nm absorbance: AU; TSS: g L-1; NPOC/DOC: mg L-1; pesticides: µg L-1.
- Data notes:
  - Some missing data due to equipment issues; turbidity data started mid-2017.
  - Lab vs field measurements may involve slightly different processing times and QA steps (e.g., blank corrections for optical scans).

## Data Quality, Gaps and Limitations
- Missing data:
  - Some samples missing due to equipment temperature issues or measurement error.
  - Turbidity measurements began only from 10 October 2017.
  - Storm optical data contain intentional gaps and event-based batching; some exact timestamps are not perfectly aligned with storm event dates.
- Calibration and drift:
  - Regular calibration of pH and conductivity meters; drift checks performed periodically.
  - UV-Vis instrument cleaning and sensor maintenance documented to mitigate fouling drift.
- Data handling and formatting:
  - Multiple files with different temporal resolutions (hourly, daily, event-based storms, high-frequency sensor data) requiring careful integration for users.
  - Some missing or placeholder rows in StormOpticalScansBlankCorrected.csv introduced for readability; date/time alignment may require careful parsing.

## Data Governance and Stewardship Considerations for Data Stewards
- Metadata completeness and standardization:
  - The dataset includes comprehensive instrument details, measurement methods, and data files, but a unified metadata schema (data dictionary, variable definitions, and units) would facilitate discovery and interoperability.
- Data licensing and reuse:
  - Data access and citation are provided; explicit licensing for reuse should be added or clarified to support downstream data sharing.
- Data curation and publishing:
  - Six-file structure with clear provenance; consider publishing a consolidated data dictionary and a data provenance report to accompany the six CSVs.
  - Implement versioning and changelog for future updates or corrections.
- Interoperability and standards alignment:
  - Align variable naming, units, and formats with common data standards to ease integration with other hydrological datasets.
  - Provide schema mapping to allow automated ingestion by data portals and catalogues.
- Access, updates, and governance:
  - Clearly define data update cadence and any embargo periods if relevant; ensure user needs are captured (e.g., researchers needing synchronized high-frequency and lab-data).
  - Include a data quality flagging scheme and traceable QA steps so users can assess reliability of each record.
- Practical recommendations for Data Stewards:
  - Add a comprehensive data dictionary covering all six CSV files, with explicit definitions, units, and permissible value ranges.
  - Include a data license and usage terms within the repository.
  - Standardize datetime formats and ensure consistent time zones across all files.
  - Document data processing steps (e.g., NPOC calculation, blank corrections) and calibration schedules in a single, accessible readme.