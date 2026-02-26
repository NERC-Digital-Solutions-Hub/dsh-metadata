# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats.

## Overview
- Dataset of GPS locations for Rod Surface Elevation Table (SET) instruments and associated marker horizons (feldspar) in saltmarsh and mudflat habitats.
- Records include instrument positions, horizon depths, and related observational details collected during a 1-year monitoring period with measurements roughly every 3–6 months.

## Spatial scope and sites
- Study regions represent contrasting habitats and soil types:
  - Essex, UK: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) – saltmarshes with clay soils; mudflats with cohesive clays, mud, and silt.
  - Morecambe Bay, UK: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) – saltmarshes with sandy soils (Morecambe Bay).
- Sites differ in inundation frequency, creek structure, and vegetation.
- GPS coordinates for SET benchmarks are provided in Easting/Northing with OSGB1936 coordinates; accuracy better than 50 mm in all directions.

## Methods and instrumentation
- Instrumentation: Rod Surface Elevation Table (SET) with receivers mounted on benchmark rods; rods driven 6–12 m into the substrate.
- Depths measured: depths of sediment above 50 cm by 50 cm feldspar marker horizons installed just beyond instrument reach in each quadrant.
- Sampling schedule: measurements taken every 3–6 months at nine pins per SET in each of four quadrants.
- Data notes: site-specific contextual notes recorded in spreadsheets; references for methods include Cahoon et al. (2002) and USGS SET description.
- Data handling: depths recorded as millimeters; cores with non-horizontal horizons averaged from multiple sides; horizon depths of <1 mm recorded as 0 mm; 'NA' used if horizon not detectable.

## Instrumentation details and observations
- SET benchmarks and horizon data are linked to the dataset "CBESS_gps_wave_transects" (GPS locations of benchmarks and marker horizons).
- Confidence intervals: individual pin readings have a reported ±4.3 mm precision (Cahoon et al., 2002).
- Calibration and real-time corrections: Leica RTK corrections in real time where applicable.
- Data capture format: spreadsheet-based data entry (Excel) with structured fields for dates, times, locations, site, habitat, quadrats, scale, and readings (pins and horizon depths).

## Data structure and formats
- Primary formats: Excel spreadsheets; dataset fields described in detail (e.g., Season, Location, Site, Habitat, Quadrat, Scale, Pin readings, Horizon depths, Notes).
- Dataset fields cover:
  - Spatial: SET benchmark locations (Easting/Northing) and site/habitat classifications.
  - Temporal: date and time of measurement; season (Winter or Summer).
  - Measurements: readings for Pins 1–9, marker horizon depths for Core 1–3.
  - Meta: recording order, notes/comments, and data quality indicators.
- Coordinate system and accuracy:
  - OSGB1936 coordinate system; accuracy better than 50 mm in all directions.

## Quality, notes, and provenance
- Data quality considerations:
  - NA values indicate measurements not performed.
  - Horizons not detectable in multiple cores recorded as NA.
  - Notes on readings capture potential significant factors affecting results.
- Provenance:
  - Observations follow globally standardized SET procedures (Rod Surface Elevation Table) with references to Cahoon et al. (2002).
  - GPS positions and benchmark coordinates documented for reproducibility and inter-site comparability.

## Access and references
- Associated GPS dataset: CBESS_gps_wave_transects (GPS locations of benchmarks and marker horizons).
- Key references:
  - Cahoon, D. R., et al. 2002. High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table. Journal of Sedimentary Research.
  - Rod SET methodology and real-time Leica RTK calibration details referenced in dataset notes.
- Data presentation: data were recorded and stored in Excel spreadsheets; accompanying methodological notes provide calibration and measurement procedures.