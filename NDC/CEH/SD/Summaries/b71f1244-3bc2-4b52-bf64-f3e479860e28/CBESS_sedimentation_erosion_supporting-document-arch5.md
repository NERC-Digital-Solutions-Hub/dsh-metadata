# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sedimentation and erosion monitoring over saltmarsh and mudflat habitats

## Dataset purpose and scope
- Monitors sedimentation and erosion using rod Surface Elevation Table (rSET) instrumentation and feldspar marker horizons (50 cm x 50 cm) adjacent to benchmark rods.
- Applies to saltmarsh and mudflat habitats in Essex (Abbots Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands).
- Aims to enable inter-comparability and long-term tracking of surface elevation changes across contrasting habitat types and sediment compositions.

## Geographic and site details
- Essex: saltmarsh with clay soils; mudflat with cohesive clays, mud, silt.
- Morecambe Bay: saltmarsh with sandy soils; mudflat with coarse, mobile sediments.
- GPS and location data provided; coordinate accuracy better than 50 mm (OSGB1936).

## Sampling design and schedule
- Monitoring occurred twice over a 1-year period.
- Nine measurement pins around each SET benchmark (in four quadrants); three SETs per site (SET 1–3) with data collected at each pin.
- Marker horizons installed just beyond instrument reach in each quadrant; cores measured for sediment depth above horizon.
- Measurements taken 3–6 months after installation; SE intervals and QA notes recorded in spreadsheets.
- For horizons not horizontal, depth estimates derived from multiple measurements; horizons with <1 mm of sediment recorded as 0 mm.

## Variables and data structure
- Observed variables include:
  - Heights at multiple pins (Pin 1–9 per SET in each quadrant).
  - Marker horizon depths (Core 1–3).
  - SET metadata (SET number, quadrant, and site identifiers).
  - Date, time of measurement, and seasonal designation (Winter, Summer).
  - Site and habitat classifications (Location: Morecambe or Essex; Site: CS, WS, WP, AH, FW, TM; Habitat: Mudflat or Saltmarsh).
- Data organized in a tabular format with field descriptors for consistent analysis (e.g., Quadrat numbers, scales, and reading sequence).
- Data quality flags and notes captured in “Notes/comments on readings.”

## Instrumentation, methods, and provenance
- Uses rod Surface Elevation Table (rSET) with standard receiver installation around benchmark rods to enable inter-study comparability (reference: Cahoon et al., 2002; USGS rod instructions).
- Benchmark installation involved driving rods into substrate and securing receivers, with top 30 cm anchored in protective pipes.
- Depths measured relative to feldspar horizons installed contemporaneously with SET measurements.
- Calibration and references provided (link to USGS SET method; Cahoon et al. 2002). 

## Data formats, metadata, and provenance
- Primary data stored in Excel spreadsheets; field descriptions and data-entry conventions documented.
- GPS coordinates of benchmarks and horizon transects are in a separate dataset (CBESS_gps_wave_transects).
- Data include a detailed coordinate set for benchmarks (Easting, Northing, elevation) with accuracy notes.
- Data provenance includes installation dates (autumn 2012) and measurement cadence (3–6 months), plus notes on significant factors affecting readings.

## Quality control and limitations
- Reported pin-level measurement precision: ±4.3 mm for individual pins (Cahoon et al. 2002).
- Data checks are indicated as NA in the documentation (i.e., formal QA steps are not described within this record).
- NA values indicate measurements not performed; potential gaps due to horizon detectability or measurement limitations.
- Data may rely on legacy systems and multiple formats; potential interoperability considerations for cross-dataset integration.

## Data access, sharing, and governance
- Dataset described for publication to relevant portals; indicates intention to upload and catalogue data holdings.
- Documentation suggests the dataset is part of a broader CBESS data ecosystem (GPS transects referenced via an associated dataset).
- Responsible staff: Tom Spencer and Ben Evans.
- Standardized formatting and metadata enable discoverability and reuse, with explicit documentation of methods, units (mm, meters), and coordinate systems (OSGB1936).

## Governance and stewarding considerations for Data Stewards
- Metadata completeness: ensure all fields (Location, Site, Habitat, Season, Date/Time, SET details, Pin readings, Horizon depths, Notes) are consistently populated and validated.
- Metadata standards: maintain OSGB1936 coordinate system usage; link to external method references (Cahoon 2002) and the CBESS GPS dataset for full provenance.
- Data quality assurance: implement explicit QA steps beyond NA fields, including validation of horizon depth calculations and handling of non-horizontal horizons.
- Data format and interoperability: encourage machine-readable exports beyond Excel (e.g., CSV/JSON) and consistent column naming; maintain controlled vocabularies for Location, Site, Habitat, Season.
- Versioning and updates: establish a clear versioning and update protocol, capturing measurement status (performed vs. NA) and any corrections to readings.
- Data sharing policies: confirm embargoes, access controls, and portal submission requirements; document any data-use licenses and attribution needs.
- Provenance and traceability: retain links to measurement protocols, instrumentation descriptions, and external references to enable reproducibility.
- Usability for data users: maintain an easily discoverable dataset catalog entry with a concise methods summary, data schema, and QA notes to support reuse by researchers and managers.