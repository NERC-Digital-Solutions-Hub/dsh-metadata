# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- Datasets record GPS locations for instruments and features used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Primary measurements include surface elevation relative to the rod SET instrument and depths of sediment deposited above feldspar horizons near the SET benchmarks.

## Dataset scope and purpose
- Supports environmental monitoring focused on coastal biodiversity and ecosystem services.
- Enables inter-comparability with a global network of SET installations.
- Provides precise geolocation, instrumentation details, and measurement procedures to inform monitoring frameworks and policy evaluation.

## Locations and habitats
- Essex locations (Saltmarsh and Mudflat):
  - Abbotts Hall (AH) 51°47'N, 0°52'E
  - Fingringhoe Wick (FW) 51°49'N, 0°58'E
  - Tillingham Marshes (TM) 51°41'N, 0°56'E
  - Habitat contrasts: clay soils, inundation patterns, creek structures, vegetation differences.
- Morecambe Bay locations (Saltmarsh and Mudflat):
  - Cartmel Sands (CS) 54°10'N, 3°0'W
  - Warton Sands (WS)
  - West Plain (WP)
  - Site descriptions indicate sandy soils and varying inundation regimes.
- Site-level setup intended to represent contrasting habitat types (soil types, inundation, vegetation) across Essex and Morecambe Bay.

## Data collection and methods
- Instrumentation: Rod Surface Elevation Table (SET) with benchmark rods; receivers bolted to rods and cemented into substrate.
- Protocols reference: Cahoon et al. (2002) and USGS SET guidance; detailed design described at the SET website.
- Installation: Autumn 2012; benchmarks driven to refusal with measurement arms and 100 mm drain pipes housing the top of rods.
- Measurements:
  - Nine pins per SET, measured in four quadrants, typically every 3–6 months over a 1-year monitoring period.
  - Feldspar horizon marker horizons (50 cm x 50 cm) installed beyond instrument reach; sediment depth above horizon measured in cores (three-side measurements used to estimate non-horizontal horizons).
  - Depths reported in millimetres; horizons transcribed with 0 mm for horizons with <1 mm of sediment; notes captured for significant factors.
- GPS: Coordinates of SET benchmarks recorded with Leica GS08 GNSS; accuracy better than 50 mm in all directions; OSGB1936 coordinate system.
- Data handling: Observations summarized in spreadsheets; includes calibration notes (Leica RTK corrections in real-time) and standard data formats (Excel).

## Data structure and contents
- Dataset fields include:
  - Location, Site, Habitat, Quadrat, Scale, Record, Date, Time
  - SET Number and Pin readings (Pins 1–9)
  - Marker horizon depths (Core 1–3)
  - Notes/comments on readings
  - Header/Row descriptors, data formats, and land-sea context
- Additional metadata:
  - GPS locations of benchmarks and marker horizons available in the associated dataset CBESS_gps_wave_transects
  - Seasonality and data entry details encoded to support downstream analysis

## Data quality, provenance, and governance
- Quality considerations:
  - Pin readings have stated confidence intervals (±4.3 mm) per Cahoon et al. (2002)
  - Accurate geolocation (≤50 mm) and standardized measurement procedures to enable cross-site comparability
  - NA values indicate measurements not performed; calibration notes indicate methods used
- Metadata completeness:
  - Comprehensive field descriptions and data dictionary included
  - Data entry in Excel spreadsheets with explicit row/column definitions
- Data governance:
  - Data sharing and openness supported by explicit notes on underlying data availability and provenance
  - Field notes capture potentially significant factors affecting results

## Access, formats, and references
- Data format: Excel spreadsheets (data and metadata)
- Associated datasets: CBESS_gps_wave_transects for GPS coordinates
- References:
  - Cahoon, D. R., et al. 2002. High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table. Journal of Sedimentary Research, 72(5), 734-739
  - USGS SET design and implementation guidance linked in dataset description