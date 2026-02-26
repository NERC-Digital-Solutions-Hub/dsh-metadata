# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

- Purpose and scope
  - Provides GPS locations for instruments and features related to wave monitoring and Rod Surface Elevation Table (RSET) installations in saltmarsh and mudflat habitats.
  - Records surface elevation relative to rSET instruments and depths of sediment deposited above feldspar marker horizons adjacent to rSET benchmarks.
  - Aims to support coastal environmental health monitoring by enabling standardized, comparable measurements of wetland elevation and sediment deposition.

- Study locations and habitat diversity
  - Sites: Essex and Morecambe Bay (UK) to represent contrasting habitats and sediment types.
  - Essex: saltmarsh with clay soils; mudflat habitats with cohesive clays, mud, and silt.
  - Morecambe Bay: saltmarsh with sandy soils; mudflat habitats with coarse, mobile sediments.
  - Specific sites include Abbotts Hall (Ah), Fingringhoe Wick (FW), Tillingham Marshes (TM) in Essex and Cartmel Sands (CS) in Morecambe Bay, plus Warton Sands (WS) and West Plain (WP) at additional locations.

- Instrumentation and monitoring protocol
  - Instrument: Rod Surface Elevation Table (RSET) installed autumn 2012 to enable inter-comparability across a global network.
  - Measurements: surface elevation changes recorded relative to a local deep benchmark; depths of sediment deposited above marker horizons.
  - Frequency: measurements conducted twice within a 1-year monitoring period.
  - Deployment details: SET benchmarks driven into the substrate; receivers attached and top of rod cemented; nine pins per quadrant used for readings.

- Marker horizons and cores
  - Marker horizons: 50 cm x 50 cm potash feldspar horizons installed just beyond instrument reach in each quadrant.
  - Cores: horizons cored contemporaneously with subsequent SET measurements; sediment depth above horizon measured; horizontal horizon depth adjustments made if cores were not perfectly horizontal.
  - Data handling: NA indicates horizon not detectable; readings organized to ensure traceability.

- Data content and metadata
  - Variables captured: heights at pins 1–9, horizon depths for cores 1–3, date, time, location, site, habitat, quadrants, SET numbers, and readings.
  - Location data: GNSS coordinates for SET benchmarks with OSGB1936 reference; accuracy better than 50 mm in all directions.
  - Dataset field structure: includes fields such as Season, Location, Site, Habitat, Quadrat, Scale, Record, Date, Time, SET Number, Pin readings, Marker horizon depths, and Notes.
  - Related dataset: CBESS_gps_wave_transects contains GPS coordinates for benchmarks and horizons.

- Data collection and quality assurance
  - Reference standards: Procedure and instrumentation align with Cahoon et al. (2002) for high-precision wetland elevation measurements; detailed guidance available via USGS-set resource.
  - Calibration: Leica RTK corrections used in real-time where applicable.
  - Data formats: Data entered in Excel spreadsheets; metadata notes capture factors potentially affecting results.
  - Documentation: Includes dataset descriptions, field definitions, and notes on readings to support data provenance and reproducibility.

- Data governance and accessibility
  - Metadata and notes emphasize record-keeping, data provenance, and the need to share underlying data publicly where appropriate.
  - Data are organized to support cross-site comparability and long-term monitoring, with explicit references to the methods and calibration used.

- Relevance for monitoring frameworks
  - Enables standardized, transparent monitoring of coastal wetland elevation and sedimentation dynamics across contrasting habitats.
  - Facilitates data stewardship, quality assurance, and governance necessary for evaluating environmental health and informing policy decisions.
  - Supports integration with broader CBESS monitoring and global RSET networks for comparative analyses.

- Key considerations for collectors and analysts
  - Ensure metadata completeness, especially concerning horizon detectability, measurement notes, and weather/seasonal context.
  - Be aware of potential data gaps (NA entries) and the need to document missing measurements.
  - Use the standardized OSGB1936 coordinates and documented accuracy when integrating with other spatial datasets.