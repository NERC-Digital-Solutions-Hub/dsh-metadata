# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

## Overview
- A dataset describing GPS locations for Rod Surface Elevation Table (RSET) instruments and associated marker horizons used for wave monitoring and sedimentation-erosion measurements in saltmarsh and mudflat habitats.
- Provides inter-comparable positioning and instrument setup to support analysis of wetland elevation and sedimentation processes.

## Study Sites and Habitats
- Regions: Essex (south-eastern Atlantic UK) and Morecambe Bay (west UK).
- Habitats: Saltmarsh and mudflats represented with contrasting sediment types.
  - Essex: Saltmarsh with clay soils; mudflats with cohesive clays, mud, and silt.
  - Morecambe Bay: Saltmarsh with sandy soils; mudflats with coarse, mobile sediments.
- Specific locations (examples):
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).

## Measurements and Instruments
- Instruments: Rod Surface Elevation Table (RSET) installed to enable inter-comparability of elevations.
- Markers: 50 cm by 50 cm feldspar marker horizons installed just beyond instrument reach; depths of sediment above horizons measured via cores (Core 1–3).
- Observables:
  - Heights at 9 pins around each SET (Pins 1–9 across four quadrants around the benchmark).
  - Marker horizon depths in three cores.
  - Additional notes on readings and potentially significant factors affecting results.
- Procedure details:
  - SETs installed autumn 2012; RSET used per globally standardised design.
  - Benchmark rods driven into substrate typically 6–12 m; receivers bolted to rods and integrated in drain pipes.
  - Measurements taken every 3–6 months during a 1-year monitoring period.
- Data quality indicators:
  - Pin measurement confidence interval around 4.3 mm (per Cahoon et al. 2002 reference).
  - NA values indicate measurements not performed.

## Data Collection Schedule
- Monitoring frequency: Twice within the 1-year period (across 3–6 month intervals).

## Data Structure, Field Descriptions, and File Formats
- Dataset is named CBESS_gps_wave_transects and includes GPS locations of benchmarks and marker horizons.
- Data format: Excel spreadsheets (data entries and field descriptions included).
- Key fields and structure:
  - Location metadata: Season (Winter/Summer), Location (e.g., Morecambe or Essex), Site (e.g., CS, WS, WP; AH, FW, TM), Habitat (Mudflat or Saltmarsh).
  - Recording specifics: Quadrat number (1–22), Scale categories (A–D with corresponding numeric values), Record (entry order), Date (DD.MM.YYYY), Time, SET Number (inland progression), Pin readings (Pin 1–9 in mm), Marker horizon depths (Core 1–3 in mm), Notes/Comments.
  - Instrument and measurement metadata: Description header, Row number for original input order, and additional dataset field descriptions.
- Coordinate data:
  - Coordinates for SET benchmarks supplied with accuracy better than 50 mm in all directions.
  - Coordinate system: OSGB1936.
  - GPS locations of benchmarks and marker horizons are included in the associated dataset CBESS_gps_wave_transects.
- Calibration and data handling:
  - Calibration: Leica RTK corrections used in real time where applicable.
  - Data quality checks: Not explicitly described (noted as NA in some quality-control fields).
  - Data entries were recorded in Excel spreadsheets; NA values indicate non-performed measurements.

## Quality, Calibration, and Provenance
- Standardised measurement approach (RSET) enables inter-site comparability.
- Accuracy of location data: better than 50 mm (in all directions) for benchmark coordinates.
- Calibration aligned with real-time Leica RTK corrections.
- Provenance: References Cahoon et al. (2002) for high-precision wetland elevation methods.

## References and Related Information
- Core methodology reference: Cahoon, D. R., et al. (2002). High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table. Journal of Sedimentary Research, 72(5), 734-739. DOI: 10.1306/020702720734.
- Additional background on RSET equipment design and use: http://www.pwrc.usgs.gov/set/set/rod.html (accessed 02/12/2013).

## Access, Usage Notes, and Limitations
- Outputs include GPS locations of SET benchmarks and horizons to support cross-site comparisons and further analyses of coastal sedimentation and elevation dynamics.
- NA values indicate non-recorded measurements; some quality-control procedures are not detailed in the dataset.
- Users should reference Cahoon (2002) for methodological context and ensure OSGB1936 coordinate handling when integrating with other spatial data.