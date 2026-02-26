# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) wave monitoring in saltmarsh and mudflat habitats.

## Overview
- Objective: Use continuous wave-monitoring data to quantify environmental conditions and support assessment of coastal ecosystem health and policy performance over time.
- Focus: Wave parameters derived from bottom pressure records across shore-normal transects at the saltmarsh–mudflat boundary in saltmarsh and mudflat habitats.
- Responsible staff: Tom Spencer, Ben Evans.

## Study sites and design
- Locations: Essex (Abbotts Hall AH, Fingringhoe Wick FW, Tillingham Marshes TM) and Morecambe Bay (Cartmel Sands CS, Warton Sands WS).
- Site descriptions: Essex and Morecambe saltmarsh regions chosen to represent contrasting sediment types (clay soils in Essex; sandy soils in Morecambe Bay) and differing inundation frequency, creek structure, and vegetation. Mudflat sites differ in sediment composition (Essex: cohesive clays, mud/silt; Morecambe: coarser, mobile sediments).

## Data collection and instrumentation
- Monitoring approach: Continuous monitoring with automated high-tide–aligned recording events; pressure recorded at all sensors at 4 Hz during events.
- Instruments: Druck PDCR1830 sensors (most) and PTX1830 sensors (for longer reaches); Campbell CR1000 data loggers.
- Deployment specifics: Sensors arranged along transects with marsh-platform and mudflat placements; logging designed to capture inundation near high tide slack water.
- Data transmission and upkeep: Telemetry via GPRS; regular field maintenance and manual downloads if telemetry fails.

## Variables and outputs
- Sensor data (PT1–PT12) include:
  - ValidPTn: binary validity of each sensor’s record
  - hPTn: mean water depth at the sensor during the event
  - EPTn: spectrally-derived total spectral energy
  - HsPTn: spectrally-derived significant wave height
  - TpPTn: spectrally-derived peak wave period

## Procedures and data processing
- Raw data handling: Data acquired as ASCII, converted from mv to pressure (Pa) using calibration and offsets; mean depth computed from pressure timeseries.
- Wave metrics: Spectral energy, significant wave height, and peak period calculated following Möller et al. (1999, 2006).
- Data compilation: Site event summaries compiled into an “All output” spreadsheet; marked and filtered into “Filtered for reliability.”
- Event validation: Excluded data due to known equipment issues (e.g., barnacle growth on diaphragms, cable damage) and irregular sensor inundation timing; checks for submergence using PT2/PT3 differences relative to valid events.
- Depth-related limitations: Attenuation of high-frequency components with depth reduces ability to detect small/short-period waves, especially at deeper mudflat sites AH and FW in front of marsh cliffs; PT2/PT3 may underrepresent events in deeper water.

## Data quality control and filtering
- Submergence checks: Ensure continuous inundation by comparing PT2/PT3 depths; remove records with implausible differences.
- Validity criteria for PT4–PT8:
  - Minimum mean depth threshold (≥20 cm) to avoid exposure effects
  - H(max)/hPT ≤ 0.78 (where H(max) = 1.86 × HsPT) to flag breaking waves
- Marking: Valid records flagged in spreadsheets (green markers); partial validity indicated (1/0).
- Data formats: Raw, filtered, and validation statuses maintained in Excel; subsequent analyses rely on validated records.

## Limitations and considerations
- Depth attenuation effects: Underestimation of spectral energy at greater depths, notably for mudflat sensors, due to depth-related loss of high-frequency components.
- Limited fetch: Low-amplitude, short-period waves predominate in some sites, affecting energy estimates and comparability across sensors and events.
- Data comparability: EPT results may not be directly comparable across sensors with depth differences due to attenuation.

## Data formats and storage
- File formats: Data retrieved from loggers in ASCII .dat; processed in MATLAB; saved as ASCII .txt; validation tests conducted in Excel.
- NA values: Indicate measurements not performed or unavailable.

## Dataset fields and structure
- Field descriptors cover:
  - Site, Habitat, Quadrat, Scale, Record, Date, Time
  - For each PT1–PT12: Valid PTn, hPTn, EPTn, HsPTn, TpPTn
- Location and site codes: Essex (E), Morecambe (M), with corresponding site labels and habitat types (Saltmarsh, Mudflat)
- Dimensional scales and recording order: Quadrant and scale definitions to support data sorting and analysis.