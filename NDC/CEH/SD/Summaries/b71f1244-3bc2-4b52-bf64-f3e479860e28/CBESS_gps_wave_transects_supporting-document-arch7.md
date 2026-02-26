# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

- Overview
  - GIS-ready dataset of global positioning system (GPS) locations for instruments and marker horizons used in wave monitoring and sedimentation-erosion table (SET) installations.
  - Targets saltmarsh and mudflat habitats to support comparative analyses across habitat types and sites.

- Spatial coverage and coordinate system
  - Locations across Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton/Sands and related sites referenced in the dataset).
  - Site descriptors include habitat type (saltmarsh or mudflat) and soil contrasts (clay in Essex; sandy soils in Morecambe Bay).
  - Coordinates provided in OSGB1936 Easting/Northing with accuracy better than 50 mm in all directions.
  - GPS data available in the dataset CBESS_gps_wave_transects (and accompanying spreadsheet fields).

- Instrumentation, sampling design, and timing
  - Instrumentation: Rod Surface Elevation Table (SET); standardised approach enabling cross-site comparability (see Cahoon et al. 2002).
  - Installation: autumn 2012 at all locations.
  - Monitoring cadence: measurements taken twice during a 1-year monitoring period; intervals of 3–6 months for SET readings.
  - Setup details: SET benchmarks surrounded by four quadrants; multiple pins (Pin 1–9) record vertical heights; 50 cm × 50 cm marker horizons of potash feldspar installed just beyond instrument reach; horizons are cores for depth of sediment deposition (Core 1–3).
  - Data handling for measurements: if a horizon is not detectable or not horizontal, depth is estimated (mean of three measurements); values <1 mm above horizon recorded as 0 mm; NA indicates not performed.

- Data collection, management, and schema
  - Observations recorded in Excel spreadsheets; notes capture potential significant factors affecting results.
  - Benchmark coordinates and marker horizon depths captured as structured fields in the dataset (e.g., Season, Location, Site, Habitat, SET Number, Pin readings, Marker horizon depths, Date, Time, Notes).
  - Quality and calibration: Leica RTK corrections used in real-time; GNSS coordinates obtained with high precision (Leica GS08 system referenced).

- staff and provenance
  - Staff responsible: Tom Spencer, Ben Evans.
  - Methodology anchored to established SET procedures (Cahoon et al. 2002); reference entries included for traceability.

- Potential GIS uses and relevance
  - Enables precise mapping of instrument locations, measurement points, and marker horizons for spatial analyses of sedimentation, elevation dynamics, and wave monitoring across contrasting habitats.
  - Supports integration with related CBESS datasets for multi-layer spatial analyses, trend detection, and inter-site comparability.

- Additional info and references
  - Detailed procedure and instrument design documentation available via the Rod Surface Elevation Table (SET) information (e.g., USGS SET resources).
  - Specific references to Cahoon, Lynch, Perez et al. (2002) for high-precision wetland sediment elevation measurements.
  - Additional data structure and field descriptions are available within the dataset (e.g., dataset fields such as Season, Location, Site, Habitat, Quadrant, Scale, Date, Time, SET Number, Pin readings, Horizon depths, Notes).