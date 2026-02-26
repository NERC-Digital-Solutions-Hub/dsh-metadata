# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sedimentation and erosion monitoring over saltmarsh and mudflat habitats.

## Overview
- A CBESS dataset monitoring sedimentation and erosion over saltmarsh and mudflat habitats using a Rod Surface Elevation Table (rSET) framework to measure surface elevation changes and sediment deposition.

## Study locations and habitats
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS).
- Habitats: Saltmarsh (two contrasting soil types—clay in Essex, sandy in Morecambe Bay) and associated mudflats; Essex mudflats characterized by cohesive clays, mud, silt; Morecambe mudflats by coarse, mobile sediments.
- Coordinates and GPS accuracy: SET benchmarks and markers located with OSGB1936 coordinates; accuracy better than 50 mm in all directions. GPS dataset available separately (CBESS_gps_wave_transects).

## Sampling design and timing
- Monitoring cadence: Observations conducted twice over a 1-year monitoring period (roughly every 3–6 months).
- Benchmarking framework: SET benchmarks installed autumn 2012; measurements taken around the benchmark in nine pins per quadrant (four quadrants around each benchmark).

## Instrumentation and procedures
- Instrumentation: Rod Surface Elevation Table (rSET) used for standardized, comparable measurements.
- Installation details: Rods driven into substrate (6–12 m depth) with receivers bolted to rods; top 30 cm cemented into 100 mm plastic drains around the benchmark.
- Marker horizons: 50 cm x 50 cm potash feldspar horizons installed just beyond reach of the instrument arm; cored at subsequent SET measurements to determine sediment depth above horizon.
- Core handling: If horizon not horizontal, mean depth estimated from three measurements around the core; cores with <1 mm sediment above horizon recorded as 0 mm; ‘NA’ used where horizon undetectable.
- Reference standards: Calibration procedures described by Cahoon et al. (2002); measurements recorded with noted field conditions.

## Observed variables and data types
- Heights: Readings for Pin 1–9.
- Horizon depths: Marker horizon depths for Core 1–3.
- Additional data: Notes on readings and other potentially significant factors affecting results.

## Data collection specifics and coordinates
- Field coordinates: SET benchmarks located and recorded with high precision; OSGB1936 coordinate system used.
- Data collection context: Observations include contemporaneous cores and horizon measurements; field notes capture contextual factors.

## Data formats and quality control
- Data format: Excel spreadsheets used for entry and storage.
- Data quality notes: Confidence intervals for individual pins previously reported (±4.3 mm in related methodology); NA values indicate non-performed measurements or horizon not detectable; notes field captures reading caveats and contextual factors.

## Dataset contents and structure
- Core fields (high-level): Location (Morecambe or Essex), Site (e.g., CS, WS, WP, AH, FW, TM), Habitat (Mudflat or Saltmarsh), Quadrat (1–22), Scale (A–D representing 1m to upper range), Record (sequence of data entry), Date, Time of Day, SET Number, Pin readings (Pin 1–9), Marker horizon depths (Core 1–3), Notes/comments.
- Additional data: Leverage of the associated gps dataset for precise geographic positioning.

## Access, references, and provenance
- Responsible personnel: Tom Spencer, Ben Evans.
- Primary reference for methods: Cahoon et al. (2002) on high-precision sediment elevation measurements.
- Data provenance: Detailed monitoring procedures and location descriptions provided, enabling inter-site comparability and potential cross-site analyses.

## Practical relevance for GIS work
- GIS-ready components: 
  - Point features for SET benchmarks and horizon markers with precise OSGB36 coordinates and elevation data.
  - Attributes capturing site, habitat, quadrant, scale, dates, and depth readings.
  - Linked horizon depth data (Core 1–3) and pin readings for temporal analysis.
  - Separate GPS dataset ("CBESS_gps_wave_transects") for enhanced spatial accuracy.
- Considerations for mapping and analysis:
  - Use OSGB1936 CRS; maintain depth units in millimeters or convert to centimeters/meters as needed.
  - Handle missing data (NA) and notes for context-specific interpretations.
  - Integrate with habitat polygons to compare sedimentation/erosion across saltmarsh versus mudflat and across soil types.
- Data quality cues:
  - Measurements have a known precision (±4.3 mm per Cahoon et al.); ensure propagation of measurement uncertainty in analyses.

## Summary
- The CBESS sedimentation and erosion dataset provides a multi-site, repeat-measurement framework using rSET to quantify surface elevation change and sediment deposition on saltmarsh and mudflat habitats in Essex and Morecambe Bay. It combines precise benchmark locations, horizon marker data, and repeated pin readings across quadrants, with robust metadata and a GIS-friendly structure suitable for spatial analyses of coastal dynamics and habitat-specific processes.