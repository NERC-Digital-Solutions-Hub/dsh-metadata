# Supporting information for 'High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)'

## Data access and citation
- Data available from: https://doi.org/10.5285/331659d7-da72-48a2-9b52-63c003557990
- Please cite:
  Hawkins, C.E; Kelly, T.J.; Loewenthal, M.; Smith, R.; Dudley, A.; Leggatt, A.; Dowman, S.; Oliver, R.G.; Collins, C.D.; Clark, J.M. (2019). High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017-Sept 2018) . NERC Environmental Information Data Centre. (Dataset).

## Experimental design and sampling regime
- Location: Bow Brook, a headwater tributary to the River Loddon, Hampshire, sampled near the confluence with the Loddon at Sherfield-on-Loddon.
- Monitoring period and cadence:
  - High-resolution water quality and flow data: hourly from 00:00 GMT on 08/09/2017 to 00:00 GMT on 09/09/2018.
  - Daily water quality samples: taken at 09:00 GMT from 08/09/2017 to 08/09/2018.
  - Storm water quality samples: hourly during storm events from 11/09/2017 to 22/01/2018.
- Data gaps and issues:
  - Missing samples due to equipment breakdown (temperature-related freezing) or measurement errors.
  - Turbidity measurements began on 10 October 2017 due to a delay in the arrival of the lab meter.

## Collection, laboratory and analytical methods and instrumentation
- In-field sampling and automation:
  - Hourly water collection using a peristaltic pump with two flow-through cells.
  - TriOS OPUS UV/VIS Spectral Analyser (full spectral scan 200–800 nm, 2.2 nm per pixel).
  - YSI 6600 V2-2 multi-parameter Sonde (turbidity, ammonium, pH, conductivity, temperature, dissolved oxygen).
  - Sontek IQ flow gauge for river flow and height at sampling point.
  - Sondes calibrated monthly; UV/Vis cleaned weekly.
  - Autosamplers: two ISCO 6712 units for daily and storm samples.
- Sample handling and storage:
  - 300 mL samples collected in 350 mL glass bottles (to reduce pesticide sorption).
  - Samples stored at 4°C and analyzed within 48 hours.
- Laboratory analyses and instrumentation:
  - pH: Mettler Toledo meter (calibrated with pH 4 and pH 7 buffers).
  - Conductivity: Mettler Toledo EasyFive (calibrated with 1413 µS standard at 25°C).
  - Turbidity: Hanna HI-93703 (0, 10, 500 FTU standards).
  - UV-Vis: Jenway 7315 spectrophotometer; scans for unfiltered and 0.7 µm filtered samples.
  - Total and dissolved analyses: filtered samples for NPOC (with acidification and purge for inorganic carbon removal) and DOC assessment.
  - Filtration and sediment: GF/F filters; calculation of total suspended solids (TSS) from filter weight change and sample volume.
  - Pesticides: daily/storm samples analyzed by Affinity Water Ltd. using LC-MS/MS (Agilent 6490) for 12 pesticides; LODs ~0.01 µg/L.
- Data processing reminders:
  - Blank corrections applied to optical scans (DailyOpticalScansBlankCorrected.csv and StormOpticalScansBlankCorrected.csv).
  - UV-Vis drift considered; baseline scans performed; blanks measured regularly.

## pH, conductivity, turbidity, and UV-Vis scan methods (in-field and laboratory)
- pH:
  - Measured on unfiltered samples (5 mL) with daily calibration checks every 5 samples.
- Conductivity:
  - Measured on unfiltered samples (5 mL) with drift checks every 5 samples.
- Turbidity:
  - Immediate measurement and a 5-minute waiting period to allow settling; blanks run every 10 measurements for drift checks.
- UV-Vis scans:
  - Two approaches: unfiltered and filtered (0.7 µm) samples; baseline scans and drift checks via blanks (water).
  - Measurements include full spectral range (200–800 nm) with samples diluted into cuvettes.

## Filtering, suspended sediments and NPOC (DOC) analysis
- Suspended sediments:
  - GF/F filters weighed before/after filtration; turbidity calculated from filter weights and filtered volume.
- NPOC (non-purgeable organic carbon):
  - Acidified samples purged with carbon-free air/nitrogen to remove inorganic carbon; samples filtered prior to NPOC analysis; TIC/TOC considerations noted to avoid negative results in carbonate-rich waters.
- Pesticide analysis (lab methodology):
  - Sub-sampling, preservative addition, and LC-MS/MS quantification of 12 pesticides; regulatory context provided via EU limits.

## Nature and units of recorded values, and data structure
- Data files (six CSVs):
  - DailyWaterQualityData.csv: 366 samples
    - Variables include: Date; Flow (m3 s-1); Depth (m); 254 nm absorbance (AU); Turbidity (NTU) in field; Conductivity (µS cm-1); pH (field and lab); Ammonium (mg L-1); NPOC (mg L-1); TSS (g L-1); 24D pesticide concentrations (µg L-1) for 12 compounds; Total pesticides (µg L-1); Individual EU limits and Total EU limits.
  - StormWaterQualityData.csv: 207 samples
    - Similar structure to daily data, with date, time, flow, depth, UV/Vis, turbidity, conductivity, pH, ammonium, lab pH/conductivity, turbidity (5 min and 0 min), 254 nm, TSS, NPOC, 12 pesticides, total pesticides, and EU limits.
  - HighFrequencySensorDataFlowandSonde.csv: 8332 samples
    - In-field flow data (FLOW in m3 s-1; STAGE in m; MEANVELOCITY; TOTALVOLUME; DEPTH; AREA; TEMP) and in-field multi-parameter sonded data (SONDEDATE/SONDETIME; SONDETEMP; SONDECOND; SONDEPH; SONDEAMMONIUM; SONDETURBIDITY; SONDEDOO-pcent; SONDEDOO-MGL).
  - HighFrequencyDataOpticalScan.csv: 8364 samples
    - Raw optical scans from TriOS OPUS (Absorption from ~198 to ~721 nm in AU); DateTime, Date, Time.
  - DailyOpticalScansBlankCorrected.csv: 366 samples
    - Blank-corrected daily optical scans (200–800 nm) in AU; notes on missing dates: 18/01/18, 08/02/18, 12/02/18, 18/07/18–30/07/18.
  - StormOpticalScansBlankCorrected.csv: 194 samples
    - Blank-corrected storm optical scans (200–800 nm) in AU; includes explicit notes on missing data and batching for storm events (e.g., Oct 2017 storm).
- Data characteristics:
  - Units for major fields defined (e.g., Flow in m3 s-1; Conductivity in µS cm-1; pH; Turbidity in NTU or FTU depending on measurement stage; NPOC in mg L-1; TSS in g L-1; pesticide concentrations in µg L-1).
  - Sample naming conventions and timestamp formats described in the DailyWaterQualityData.csv and StormWaterQualityData.csv descriptions.
- Data completeness and caveats:
  - Several gaps due to equipment issues or holidays; turbidity data started later in the study.
  - Storm sampling includes batch-based labeling and some irregularities noted (e.g., 08/11/17 partial analyses due to time constraints).

## Notes on data quality and usability
- The dataset provides a comprehensive, multi-modal view of water quality across hourly, daily, and storm-event scales for the Bow Brook/Loddon catchment during Sept 2017–Sept 2018.
- Calibration, drift checks, and cleaning procedures are documented for all instruments and analyses to support transparent data quality assessment.
- Blank-corrected optical data are provided to support robust interpretation of spectral measurements.
- The six CSV files collectively enable time-series analyses, cross-variable correlations (e.g., flow vs. turbidity, pesticide occurrence vs. rainfall/storm events), and assessment of dissolved and particulate carbon dynamics, as well as pesticide loadings.