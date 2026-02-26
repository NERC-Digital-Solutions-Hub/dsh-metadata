# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) sedimentation and erosion monitoring over saltmarsh and mudflat habitats

## Overview
- Purpose: Monitor sedimentation and erosion using a Rod Surface Elevation Table (rSET) approach to measure surface elevation changes and sediment deposition in saltmarsh and mudflat habitats.
- Temporal scope: Monitoring conducted twice over a 1-year period.
- Locations and habitats:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing saltmarsh and mudflat habitats with clay soils.
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS) representing saltmarsh and mudflat habitats with sandy/coarser sediments.
- Rationale: Sites chosen to represent contrasting sediment types and inundation structure/vegetation; enables inter-site comparisons and cross-site intercomparability via standardised rSET methods.
- Staff: Tom Spencer, Ben Evans.

## Datasets and structure
- Measurements:
  - Surface elevation changes at nine pins (Pin 1–9) around four quadrants of a benchmark.
  - Horizon depths above 50 cm by 50 cm feldspar marker horizons (Core 1–3).
  - Additional notes on significant factors affecting results.
- Instrumentation and protocol:
  - Rod Surface Elevation Table (rSET) installed autumn 2012; measurements taken every 3–6 months at each location.
  - Nine pins in four quadrants around the benchmark; measurements twice within the monitoring year.
  - Feldspar marker horizons installed just beyond the instrument reach; cores measured for depth of sediment above horizon.
  - Handling of non-horizontal horizons by averaging measurements from multiple sides; 0 mm recorded where less than 1 mm of sediment is present.
  - Accuracy: pin-level confidence intervals reported as ±4.3 mm.
- Data management:
  - Observations entered in Excel spreadsheets.
  - NA values used to indicate non-performed measurements or undetectable horizons.
  - GPS coordinates for benchmarks provided; OSGB1936 coordinate system; accuracy better than 50 mm in all directions.
  - Reference dataset for GPS: CBESS_gps_wave_transects (separate dataset).

## Methods and metadata
- Standard approach: RSET instrumentation allows for intercomparability across global networks; detailed description available via Cahoon et al. (2002) and USGS Rod SET resource.
- Data recording fields and timing:
  - Measurements recorded at 3–6 month intervals; locations include multiple sites per region.
  - Marker horizons captured with depth measurements in Core 1–3; horizon depths recorded in millimetres.
- Reference framework:
  - Cahoon, D. R. et al. (2002) High-Precision Measurements of Wetland Sediment Elevation: II. The Rod Surface Elevation Table.
- Data checks: Formal data checking procedures are not specified (NA in the record).

## Data structure and field dictionary (high-level)
- Location codes: Essex (E), Morecambe (M).
- Site names: For Essex — Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM); For Morecambe — Cartmel Sands (CS), Warton Sands (WS).
- Habitat types: Mudflat (MF), Saltmarsh (SM).
- Spatial granularity: Quadrat numbers (1–22); Scale categories (A–D) representing distance bands; Records and associated dates/times.
- Measurements:
  - SET measurements: Reading Pin 1–9 (mm) per SET; SET Number (increases landward).
  - Marker horizons: Depths for Core 1–3 (mm).
- Notes: Free-text field for observations and potential factors impacting readings.

## Data quality, caveats, and accessibility
- Data quality:
  - Measurement uncertainty for pins: ±4.3 mm.
  - Horizons: depth measurements recorded with handling for undetectable horizons (NA or 0 mm where appropriate).
  - Data checking procedures are not explicitly documented (NA).
- Accessibility and format:
  - Primary data stored in Excel spreadsheets.
  - Geographic coordinates provided in OSGB1936 with sub-centimetre accuracy for benchmarks; GPS dataset exists separately.
- Documentation and references:
  - Clear linkage to field methods (rSET) and standardisation framework.
  - Primary reference: Cahoon et al. (2002) for rSET methodology.

## How Data Support can enable use
- Data integration and cleaning:
  - Merge SET heights (Pins 1–9) with horizon depths (Core 1–3) and site metadata; align with GPS dataset for mapping.
  - Handle NA values and non-horizontal horizons; standardize date/time formats.
- Data products and analyses:
  - Time-series dashboards of surface elevation change by site and habitat.
  - Comparative analyses across Essex vs. Morecambe Bay and saltmarsh vs. mudflat habitats.
  - Pivot tables to summarize mean/median elevation change and horizon deposition per quadrat, site, and region.
- Visualization and reporting:
  - Maps showing benchmark and horizon locations with OSGB1936 coordinates.
  - Visual summaries of sedimentation vs. erosion patterns over the monitoring period.
- Documentation and reuse:
  - Maintain clear field definitions and data dictionary; ensure consistent column naming and units (mm, dates, times).
  - Provide guidance on handling NA values and non-detect horizons; note the measurement cadence and instrument specifics for reproducibility.