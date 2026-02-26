# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

## Overview
- Describes GPS locations for instruments and features used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Captures surface elevation relative to a rod SET (rSET) instrument, and depths of sediment deposited above feldspar marker horizons near rSET benchmarks.
- Staff: Tom Spencer, Ben Evans.
- Monitoring occurred at multiple UK sites during a 1-year period with measurements roughly every 3–6 months.

## Spatial and temporal scope
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS).
- Habitat types: Saltmarsh (two contrasting soil types: clay in Essex; sandy in Morecambe Bay) and Mudflat (Essex and Morecambe Bay with differing sediment characteristics).
- Coordinates and accuracy:
  - GPS coordinates provided; accuracy better than 50 mm in all directions.
  - Coordinate system: OSGB1936 (2).
- Temporal coverage:
  - Field installations in autumn 2012.
  - Measurements at nine pins per benchmark, in four quadrants, at 3–6 month intervals over the monitoring year.
- Data file reference: CBESS_gps_wave_transects contains GPS locations of benchmarks and horizons.

## Data collection and instrumentation
- Instrumentation and methods:
  - Rod Surface Elevation Table (SET) used for standardized, inter-comparable measurements (RSET).
  - Benchmarks driven into substrate using body mass and mallet; receivers bolted to rods and top of rod cemented into plastic pipes.
  - Measurements taken at nine pins per benchmark.
  - 50 cm x 50 cm feldspar horizon markers installed beyond instrument reach; depths of sediment above horizons measured in cores.
  - Cores may require averaging depths if horizons are not horizontal; 0 mm recorded if less than 1 mm of sediment present above horizon.
- Observational schedule and metadata:
  - Observations recorded every 3–6 months; notes on potentially significant factors included in spreadsheets.
  - GNSS locations captured with Leica GS08; accuracy under 50 mm; GPS coordinates provided for all SET benchmarks and horizons.
- Data standards and references:
  - SET methodology aligned with Cahoon et al. (2002) and general Rod SET guidance from USGS.
  - Real-time Leica RTK corrections used for calibration where applicable.
- Data formats:
  - Data entered in Excel spreadsheets.
  - Associated data description and field dictionary included within the dataset.

## Data content and structure
- Dataset fields and structure:
  - Season, Location (Morecambe or Essex), Site (e.g., CS, WS, WP, AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrant and Quadrat identifiers, Scale categories (A–D) and corresponding measurements.
  - Recording fields include: Date, Time, SET Number, Pin 1–9 readings (mm), Marker horizon depths (core 1–3) in mm, and Notes/comments.
  - Metadata fields include: Row number, Record, Description headers, and Core details for horizon depths.
- Data lineage and provenance:
  - GPS locations and benchmarks are linked to the CBESS_gps_wave_transects dataset.
  - Field descriptions and dataset field descriptions provided to support interpretation and reuse.
- Documentation:
  - Detailed methodological notes and references included within the dataset records.
  - NA values indicate non-performed measurements; notes capture any special considerations.

## Data quality, limitations, and uncertainty
- Measurement precision:
  - Confidence intervals for individual pins: ±4.3 mm (Cahoon et al. 2002 reference).
  - GPS coordinates with accuracy better than 50 mm in all directions.
- Data completeness:
  - Some fields marked NA where measurements were not performed.
  - Calibration and quality control steps are described but some data checks are NA.
- Notes and caveats:
  - Special factors affecting readings are recorded as notes; horizon depths may require averaging across sides if horizons are not perfectly horizontal.

## Access, sharing, and governance
- Data accessibility:
  - GPS locations are contained in the associated dataset CBESS_gps_wave_transects.
  - Data are provided as Excel spreadsheets with accompanying data field descriptions.
- Documentation and references:
  - Methodological basis cited (Cahoon et al. 2002) and links to SET design documentation.
  - References and calibration procedures noted (Leica RTK corrections in real time).
- Data stewardship considerations:
  - Dataset includes both raw measurements and measurement context notes.
  - Clear field definitions and coordinate system standardization (OSGB1936) to support interoperability.
  - Emphasis on inter-comparability across CBESS network via standardized instruments and recording practices.

## Practical implications for data stewards
- Ensure ongoing updates and synchronization with the CBESS_gps_wave_transects dataset for complete spatial context.
- Maintain metadata completeness (site, habitat, quadrant, horizon depths, pins, dates, times, and notes) to facilitate reuse.
- Preserve measurement provenance (instrument type, installation procedure, calibration, and references) to support replication and inter-network comparisons.
- Monitor and document any data gaps (NA entries) and the reasons for missing measurements to support future data integration.
- Consider standardizing data formats beyond Excel for long-term interoperability and ease of data ingestion into catalogs and portals.