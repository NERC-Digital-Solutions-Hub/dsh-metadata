# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sedimentation and erosion monitoring over saltmarsh and mudflat habitats

- Purpose and scope
  - Document describes a CBESS dataset monitoring sedimentation and erosion over saltmarsh and mudflat habitats.
  - Focuses on surface elevation changes and sediment deposition using standardized measurement techniques to enable cross-site comparability.

- Study sites and habitat characterization
  - Locations:
    - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
    - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS)
  - Habitat contrasts:
    - Saltmarsh habitats with contrasting soil types: clay-rich in Essex and sandy soils in Morecambe Bay
    - Mudflats with differences in sediment composition (cohesive clays, muds vs coarse, mobile sediments)
  - Site selection reflects broad differences in inundation frequency, creek structure, and dominant vegetation.

- Instrumentation and methodology
  - Standard instrument: Rod Surface Elevation Table (rSET) for high-precision surface elevation measurements.
  - Additional marker horizons: 50 cm x 50 cm potash feldspar horizons installed beyond the instrument arm.
  - Monitoring setup:
    - Benchmarks installed autumn 2012; receivers anchored to rods and top of rod cemented into plastic drains.
    - Nine pin locations arranged in four quadrants around each benchmark for periodic readings.
  - Standards and references: rSET design follows global standardization; detailed methods described in Cahoon et al. (2002) and linked at USGS SET resource.

- Data collection schedule and parameters
  - Monitoring frequency: Twice within a 1-year monitoring period (roughly 3–6 months between sessions).
  - Observed variables:
    - Heights at nine pins (Pin 1–9)
    - Horizon depths at three marker horizons (Core 1–3)
  - Spatial data: Coordinates collected with Leica GS08 GNSS; accuracy better than 50 mm (OSGB1936).
  - Data quality and notes: Field notes recorded to capture potentially significant factors affecting results.

- Metadata, data management, and formats
  - Dataset format: Excel spreadsheets (data entry and organization).
  - Data provenance and quality control:
    - Metadata and notes accompany readings; NA indicates measurements not performed.
    - Confidence intervals for individual pins: ±4.3 mm (as cited from Cahoon et al., 2002).
  - Location metadata:
    - SET benchmark coordinates and additional GPS data referenced as CBESS_gps_wave_transects (associated dataset).
  - Data governance and sharing:
    - Original text indicates the need for quality assurance, transparent data sharing, and standardized data management practices; data are structured to be clear and reusable with defined fields and codes.

- Data content and structure
  - Dataset field descriptions include:
    - Location (Essex or Morecambe), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat or Saltmarsh)
    - Quadrat and scale codes to indicate spatial granularity
    - Record and Date fields for measurement timing
    - Time of Day for measurement start
    - SET Number (progression of horizon distance landward)
    - Pin 1–9 readings (mm)
    - Marker horizon depths (Core 1–3) (mm)
    - Notes/comments for readings
  - Reference framework:
    - Cahoon, D. R., et al. (2002) on High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table
  - Data handling guidance:
    - NA values indicate measurements not performed; Excel-based data entry and organization.

- Related data and accessibility
  - GPS coordinates and transects are stored in a related dataset CBESS_gps_wave_transects.
  - The dataset emphasizes cross-site comparability and openness of measurement methods, with explicit links to standard procedures and calibration references.

- Summary of relevance for monitoring framework development
  - Demonstrates a robust, standardized approach to measuring wetland elevation change and sediment deposition across contrasting habitats.
  - Combines rSET with marker horizons to capture both elevation dynamics and accretion signals.
  - Provides detailed metadata, precise geolocation, and a clear data structure conducive to integration into broader environmental health monitoring frameworks.
  - Highlights practical data governance considerations, including data sharing, metadata completeness, and provenance.