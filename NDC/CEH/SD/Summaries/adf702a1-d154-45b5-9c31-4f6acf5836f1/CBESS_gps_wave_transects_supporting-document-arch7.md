# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- GIS-focused dataset documenting GPS locations for wave monitoring instruments and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Captures instrument benchmarks, marker horizons, and associated field measurements to enable spatial analysis and inter-site comparisons.
- Data linked to a CBESS GPS dataset (CBESS_gps_wave_transects) and designed for inter-operability with a global SET network.

## Spatial scope and locations
- Study sites:
  - Essex: Abbotts Hall (AH) and Fingringhoe Wick (FW) and Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS) and Warton area (SETS noted)
- Habitat types:
  - Saltmarsh with contrasting soil types: clay soils (Essex) and sandy soils (Morecambe Bay)
  - Mudflats: cohesive clays/mud/silt (Essex) and coarse, mobile sediments (Morecambe Bay)
- Instrument and horizon locations:
  - SET benchmarks with precise E, N coordinates (OSGB1936) and elevations (meters)
  - Nine pins per benchmark (3x3 quadrant arrangement) and 50 cm × 50 cm feldspar marker horizons per quadrant
- Spatial accuracy:
  - GPS coordinates with accuracy better than 50 mm in all directions
  - Coordinates provided for each SET benchmark and horizon locations
- Data citation:
  - GPS locations of benchmarks and marker horizons are contained in CBESS_gps_wave_transects

## Data collection methods and instrumentation
- Instrumentation:
  - Rod Surface Elevation Table (SET) installations following globally standardised methods
  - Leica RTK corrections used for calibration (real-time)
- Monitoring schedule:
  - Observations collected twice within a 1-year monitoring period
- Measurements and variables:
  - Heights at pins 1–9 around each SET
  - Horizon depths at cores 1–3 above 50 cm marker horizons
- Procedures:
  - Benchmark rods driven into substrate (6–12 m depth typical) and fixed with receivers
  - Horizons cored contemporaneously with SET measurements
  - Depths measured in millimeters; horizontal cores averaged if horizons not perfectly level
- Documentation and references:
  - Methodology described by Cahoon et al. (2002)
  - Design and instrumentation details available via USGS SET resources

## Data structure and schema
- File formats:
  - Data initially entered into Excel spreadsheets
- Dataset scope:
  - Includes the description, calibration, field notes, and measurement records
- Key fields (examples):
  - Season (Winter/Summer)
  - Location (Morecambe: CS, WS, WP; Essex: AH, FW, TM)
  - Site (e.g., Cartmel Sands, Abbotts Hall)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat (1–22)
  - Scale (A: 1 m; B/C/D ranges)
  - Record (order of data entry for analyses)
  - Date, Time of Day
  - SET Number (inland progression)
  - Pin readings (Pin 1–9)
  - Marker horizon depths (Core 1–3)
  - Notes/comments
- Data quality and interpretation notes:
  - NA values indicate non-performed measurements
  - Notes provide context for readings and potential factors affecting results
- Dataset linkage:
  - CBESS_gps_wave_transects contains GPS data for benchmarks and horizons

## Quality control and provenance
- Data quality and consistency:
  - Multiple procedures standardised to ensure comparability across sites and datasets
  - Measurements repeated over time with notes documenting significant factors
- Provenance and references:
  - Base methodology grounded in Cahoon et al. (2002) for SET measurements
  - Calibration and instrumentation details documented (Leica RTK, OSGB36 system)

## Practical GIS applications
- Map-based visualization and analysis of:
  - Spatial distribution of SET benchmarks and horizon markers
  - Elevation change over time and sediment deposition patterns across habitat types
  - Comparisons between Essex and Morecambe Bay sites by habitat and soil type
- Data integration:
  - Combines with CBESS_gps_wave_transects for comprehensive spatial datasets
  - Supports cross-site analyses and inter-operability within a global SET network

## Access and references
- Primary references:
  - Cahoon, D.R., et al. 2002. High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table. Journal of Sedimentary Research
- Data accessibility:
  - GPS locations and related measurements are stored in CBESS_gps_wave_transects and linked within the CBESS dataset framework