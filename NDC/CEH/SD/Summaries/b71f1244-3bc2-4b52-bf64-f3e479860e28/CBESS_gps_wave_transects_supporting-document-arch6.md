# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- Metadata describing GPS locations for instruments and features used in wave monitoring and sedimentation-erosion table (SET) installations within saltmarsh and mudflat habitats.
- Aims to support data interoperability and reuse by providing precise coordinates and associated measurement context for SET benchmarks, horizon markers, and related observations.

## What is in the dataset
- Dataset name and purpose: CBESS GPS locations for SET installations and wave-monitoring instruments; includes coordinates and feature locations.
- Staff responsible: Tom Spencer, Ben Evans.
- Monitoring cadence: Installations in autumn 2012; observations taken 3–6 months apart, twice within a 1-year monitoring period.
- Observed variables (high level): Heights at pins (Pin 1–9) and horizon depths at cores (Core 1–3); recording of observation metadata.

## Study sites and habitat context
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton (WS/WP in dataset schema)
- Habitat and soil contrasts:
  - Saltmarsh in Essex with clay soils vs. saltmarsh in Morecambe Bay with sandy soils
  - Mudflat sites: Essex with cohesive clays, mud, silt; Morecambe Bay with coarse, mobile sediments
- Broad site differences also include inundation frequency, creek structure, and dominant vegetation between Essex and Morecambe Bay

## Data collection and methods
- Instrumentation and standardization:
  - Rod Surface Elevation Table (SET) method used for inter-comparability (reference standards described by Cahoon et al., 2002; USGS resources linked in dataset notes).
  - SET benchmark rods installed to refusal depth; receivers mounted and cemented into substrate around the benchmark.
- Sampling and measurements:
  - Measurements taken at nine pins in each of four quadrants around each SET benchmark.
  - Horizon horizons (potash feldspar) installed 50 cm by 50 cm beyond instrument reach; depths measured above horizons.
  - If horizon depth is non-horizontal in cores, mean depth is used from multiple measurements.
  - Depths reported in millimeters; if no sediment above horizon, recorded as 0 mm; 'NA' used if horizon not detectable across cores.
- Data notes and quality:
  - Field notes on significant factors recorded within spreadsheets.
  - Coordinates derived with high precision using a Leica GS08 GNSS system; positional accuracy better than 50 mm in all directions; OSGB1936 coordinate system.
  - GPS data for benchmarks and horizons are contained in the associated dataset "CBESS_gps_wave_transects".
- Calibration and formats:
  - Real-time Leica RTK corrections used where applicable.
  - Data entered into Excel spreadsheets; NA values indicate non-performed measurements.

## Data structure and fields
- Dataset fields encompass descriptive and measurement metadata, including:
  - Season (Winter or Summer)
  - Location (Morecambe or Essex)
  - Site (e.g., Cartmel Sands, Warton Sands, West Plain; Abbotts Hall, Fingringhoe Wick, Tillingham Marshes)
  - Habitat (Mudflat or Saltmarsh)
  - Quadrat (1–22) and spatial scale (A–D; 1 m to upper range)
  - Record (sequence in analysis)
  - Date and Time of measurement
  - SET Number (inlandward progression)
  - Pins (Pin 1–9 readings in mm)
  - Marker horizon depths (Core 1–3 in mm)
  - Notes/comments on readings
- Dataset column descriptions provide structure and sorting keys to enable data ingestion and analysis.

## Quality, access, and references
- Accuracy: GPS coordinates with OSGB1936 reference, better than 50 mm precision.
- Data availability: Data are organized in Excel spreadsheets; associated GPS dataset provided as CBESS_gps_wave_transects.
- References and background:
  - Cahoon et al. (2002) on high-precision measurements of wetland sediment elevation and SET methodology.
  - Real-time Leica RTK corrections used for calibration where applicable.
- Additional context: NA values denote non-performed measurements; horizon readings may be core-based with multiple measurements to address non-horizontal horizons.