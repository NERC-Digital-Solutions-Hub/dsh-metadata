# Continuous   measurements   of   conductivity,   dissolved   oxygen,   pH,   temperature and water level in rivers (20022007) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR baseline dataset: continuous river water quality and level measurements across 23 sites in the Frome, Piddle, Pang, Lambourn, and Tern catchments.
- Timeframe: 2002–2007.
- Frequency: measurements every 15 minutes.
- Co-located with Environment Agency monitoring sites; some sites align with NRFA registered stations.

## What was measured and units
- Conductivity at 25°C: microSiemens per centimetre (uS/cm)
- Dissolved oxygen: percent saturation (% sat)
- pH: pH units
- Temperature (water): degrees Celsius (°C)
- Water level: millimetres (mm)

## Locations and site codes
- 23 LOCAR water quality sampling sites (LCWQ) with codes such as FP01, FP02, FP06, FP11, FP12, FP15, FP21, FP22, FP23, FP26, FP31, PL09, PL15, PL17, PL18, PL19, PL20, TE03, TE05, TE09, TE16, TE20, TE22.
- Site details include catchment designation (FP = Frome/Piddle, PL = Pang/Lambourn, TE = Tern) and NRFA station associations where applicable.
- Some sites share locations (e.g., TE05 and TE22 at the same site).

## Instrumentation and data collection
- Water quality: YSI 6-Series multi-parameter sondes with sensors for temperature, pH, conductivity, and DO.
  - Temperature: thermistor; range -5 to 45°C; accuracy ±0.15°C; resolution 0.01°C.
  - pH: glass electrode; range 0–14; accuracy ±0.2 pH units; resolution 0.01 pH; calibrated with pH 7 and 10 buffers.
  - Conductivity: 4 nickel electrodes; range 0–100 mS/cm; accuracy ±0.5% of reading + 0.001 mS/cm; resolution 0.001–0.1 mS/cm.
  - Dissolved oxygen: polarographic; 0–500% saturation; accuracy variable by range; resolution 0.1%.
- Water level: Druck PDCR 1830 pressure transducers; range 0.75–600 mH2O; accuracy ±0.06%.
- Maintenance: sondes calibrated and maintained roughly every deployment; two-week deployment cycles with field calibration and lab checks during/after deployment.

## Calibration and quality assurance procedures
- Pre-field calibration (in lab): calibrate DO (air-saturation reference), conductivity, and pH using standard solutions and buffers; fresh solutions used per calibration.
- Field deployment: calibration steps performed with equipment connected to a laptop/software (EcoWatch); ensure membrane conditioning and proper cleaning prior to calibration.
- Post-field deployment: post-calibration checks conducted in the lab; data logged from calibration software for DO, conductivity, and pH.
- DO calibration specifics: saturate membrane in moist air; use barometric pressure entry; record DO% and DO change.
- Cleaning procedures: mud removal, sensor surface care, membrane conditioning, and careful handling to avoid touching sensitive glass and DO membranes.
- Data capture: Catchment Service Team installs, maintains, and downloads data from loggers at each site.

## Data quality and limitations
- Data are raw; no quality control or correction for instrument drift or failures included.
- Normal ranges (Chapman 1996) referenced for context:
  - Temperature: 0–30°C
  - pH: 6.0–8.5
  - Conductivity: 10–1000 uS/cm
  - DO: 0–20 mg/L
- Observations from QA review:
  - Notable scatter and periods of implausible data.
  - Battery level below 10 V likely yields unreliable data for all parameters.
  - DO values above 200% are possible but unlikely; extremely low DO values also unlikely.
  - pH values outside 1–14 are not possible by definition; values >11 or <4 are considered unreliable.
  - Temperature generally reasonable; values outside 5–25°C should be investigated.
  - Conductivity and water level are highly site-specific; typical ranges observed 200–1200 for conductivity.
- Data quality assessments were reviewed by a senior water quality scientist; box-and-whisker plots produced for all variables to illustrate distribution and outliers.

## Data stewardship considerations
- Data lifecycle: raw data collected 2002–2007, with site metadata and instrument information critical for reuse.
- Metadata needs for discoverability and interoperability:
  - Site codes, catchment designation, NRFA associations, and exact coordinates.
  - Instrument specifications (YSI 6-Series model, sensor ranges, accuracy, calibration procedures).
  - Measurement intervals, units, and data formats.
  - Calibration and maintenance logs, including lab and field procedures.
- Data sharing and governance:
  - Data are linked to EA monitoring networks and NRFA, implying governance and potential access through respective portals.
  - Clear documentation of calibration/maintenance routines supports reproducibility and traceability.
  - Flagging and handling of unreliable data (e.g., battery <10 V) recommended before publishing or integration into broader datasets.
- Recommendations for Data Stewards:
  - Prepare comprehensive data dictionaries, metadata records, and provenance trails.
  - Document QC practices and establish a data quality flagging scheme for raw data.
  - Plan for data versioning, updates, and any embargo or access restrictions.
  - Ensure data are uploaded to appropriate data portals with consistent naming, units, and schemas to aid discoverability and reuse.