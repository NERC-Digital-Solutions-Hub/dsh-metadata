# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats

## Overview
- Longitudinal dataset of wave parameters derived from bottom pressure records along shore-normal transects crossing the saltmarsh–mudflat boundary.
- Focus on two contrasting ecological settings to capture habitat and sediment-type differences.
- Continuous monitoring with automated high-tide events; data processed to produce wave metrics.

## Study sites and design
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Essex: saltmarsh with cohesive clays; Morecambe Bay: saltmarsh with sandy soils; mudflats differ (Essex: cohesive clays; Morecambe: coarse, mobile sediments).
- Essex and Morecambe Bay saltmarsh regions also differ in inundation frequency, creek structure, and vegetation.
- Transects deployed to represent vegetated and unvegetated habitats; monitoring includes potential marsh platform effects.

## Data collection and instruments
- Instrumentation: Druck pressure transducers (PT1–PT12; mostly PDCR1830 with 350 mbar range; PTX1830 at Tillingham for longer distances) wired to a Campbell CR1000 data logger.
- Sampling: continuous monitoring; events triggered near high tide slack water; data recorded at 4 Hz during bursts.
- Telemetry and maintenance: data telemetered via GPRS; regular maintenance visits for sensor cleaning and data download; some records excluded due to equipment issues (barnacle growth, damaged cables, etc.).

## Variables observed
- For each sensor (PT1–PT12): 
  - ValidPTn (data validity)
  - hPTn (mean water depth at sensor during event)
  - EPTn (spectrally-derived total spectral energy)
  - HsPTn (spectrally-derived significant wave height)
  - TpPTn (spectrally-derived peak period)

## Data processing workflow
- Raw voltages converted to pressure using manufacturer calibration and offsets; mean depth computed from pressure timeseries.
- Spectral analyses performed following Möller et al. (1999, 2005) to derive EPT, Hs, Tp.
- Outputs compiled per event into an “All output” spreadsheet; validated data moved to “Filtered for reliability” spreadsheet.
- Data handled in ASCII formats; processing in Matlab; validation tests in Excel.

## Quality control and data screening
- Records flagged for reliability; suspect data eliminated (equipment issues, calibration or exposure problems).
- Submergence checks using PT2/PT3; records where submergence criteria fail are removed.
- Depth-attenuation caveat: deeper water underestimates high-frequency components, affecting PT2–PT3 at some sites (AH and FW).
- Validity criteria for records:
  - Minimum mean depth threshold (≥ 20 cm) to avoid exposure effects.
  - Breaking-wave criterion: H(max)/hPT ≤ 0.78, where H(max) = 1.86 × HsPT.
- PT4–PT8 records are marked for validity; green markers indicate suitability for analysis.
- Datasets exist in two forms: All output (raw collected) and Filtered for reliability (validated data).

## Data limitations and caveats
- Depth attenuation reduces detection of short-period waves at greater depths, especially for mudflat sensors.
- Limited fetch at some sites results in typically low-amplitude, short-period waves.
- Some records may be unsuitable due to marsh platform effects or sensor-specific issues; not all sensors record every event.

## Dataset structure and field descriptions
- Site and habitat metadata:
  - Site (Essex or Morecambe; e.g., AH, FW, TM, CS, WS)
  - Habitat (Mudflat MF or Saltmarsh SM)
  - Quadrat (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper limit)
  - Record (entry order)
  - Date, Time of Day
- For each PT1–PT12:
  - ValidPTn (0 or 1)
  - hPTn (mean depth in meters)
  - EPTn (total spectral energy)
  - HsPTn (significant wave height)
  - TpPTn (dominant wave period in seconds)
- Additional non-sensor fields include Winter/Summer and location codes.

## Data access and formats
- Data retrieved from loggers in ASCII .dat format; processed into ASCII .txt files.
- Outputs stored as two spreadsheets:
  - All output (complete set of records)
  - Filtered for reliability (validated records)
- NA values indicate missing measurements.

## Stewardship, maintenance, and use
- Staff: Tom Spencer, Ben Evans.
- Regular field maintenance ensures sensor cleanliness and data integrity; data quality controlled before dissemination.
- Clear metadata and validation workflow support data discoverability, governance, and reuse across the data ecosystem.