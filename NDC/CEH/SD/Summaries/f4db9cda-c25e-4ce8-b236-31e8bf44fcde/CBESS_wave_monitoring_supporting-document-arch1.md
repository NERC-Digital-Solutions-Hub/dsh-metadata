# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats

## Aim and scope
- Document describes a dataset of coastal wave parameters derived from bottom pressure records along shore-normal transects spanning the saltmarsh–mudflat boundary.
- Intended to support understanding of coastal biodiversity and ecosystem service sustainability under different sediment and vegetation contexts.

## Study sites and habitat context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) — represent mudflat and saltmarsh with clay soils.
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS) — saltmarsh with sandy soils; mudflats with coarse, mobile sediments.
- Essex and Morecambe saltmarsh regions differ in inundation frequency, creek structure, and dominant vegetation.

## Temporal and sampling design
- Continuous monitoring with automated high-tide slack-water events.
- Pressure data recorded at 4 Hz during recording bursts; telemetered via GPRS.
- Events: logger records 4096 measurements at 4 Hz (~17 minutes) per inundation burst.
- Sensors: predominantly PDCR 1830; some PTX 1830 sensors for longer distances; data loggers Campbell CR1000.
- Maintenance: regular site checks; manual data downloads if telemetry fails.

## Observed variables and data structure
- For each sensor PT1–PT12: ValidPTn, hPTn (mean water depth), EPTn (spectrally-derived total energy), HsPTn (significant wave height), TpPTn (peak period).
- Dataset fields include: Site (AH, FW, TM, CS, WS), Habitat (Mudflat MF, Saltmarsh SM), Quadrat, Scale (A–D), Record, Date, Time, and per-sensor parameters (ValidPTn, hPTn, EPTn, HsPTn, TpPTn).
- Nominal identifiers and location metadata to enable sorting and cross-site comparisons.

## Observing and data processing methods
- Data acquisition: bottom pressure transducers; raw mV converted to pressure (Pa) using manufacturer calibration and zero offsets.
- Depth calculation: mean depth per sensor used to derive water depth from pressure.
- Spectral analysis: use established methods (Möller et al. 1999; Möller 2006) to derive EPT, Hs, and Tp.
- Data handling: results compiled into an “All output” spreadsheet; a filtered subset (“Filtered for reliability”) excludes suspect data.

## Quality control and data cleaning
- Exclusion criteria include:
  - periods with known equipment issues (e.g., barnacle growth on diaphragms, damaged cables).
  - records where PT2/PT3 submergence indicators are inconsistent with valid inundation.
  - depth-attenuation limitations at deeper water reducing high-frequency components, especially at mudflat sensors AH and FW.
- Validity criteria for records:
  - minimum mean depth threshold (≥20 cm) to ensure continuous inundation.
  - breaking-wave criterion: H(max)/hPT ≤ 0.78, where H(max) = 1.86 × HsPT.
- Sensors PT4–PT8 vetted with green markers if meeting both criteria; records flagged accordingly.
- Data processing and validation performed using Matlab and Excel; NA values denote missing measurements.

## Data formats and accessibility
- Original data: ASCII .dat; processed outputs saved as ASCII .txt.
- Supporting work: spreadsheets in Excel; analysis steps and validations documented.
- Data provenance and reproducibility emphasized through metadata and adherence to site-specific procedures.

## Limitations and interpretation notes
- Depth-attenuation effect reduces detection of small, short-period waves at greater depths; energy estimates from deeper sensors may be underrepresented.
- In some events, PT2/PT3 readings may not reflect marsh- or platform-related wave conditions, affecting cross-sensor comparability.
- Fetch limitations and local bathymetry influence wave measurements, particularly at AH and FW.
- Incomplete sensor inundation during events may affect the consistency of the dataset across sites and events.

## Staff and responsibility
- Primary contacts: Tom Spencer, Ben Evans.