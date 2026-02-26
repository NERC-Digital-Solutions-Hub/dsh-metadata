# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Overview
- Dataset of GPS locations for instruments and features used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Focuses on Rod Surface Elevation Table (rSET) benchmarks, associated markers, and survey coordinates to enable inter-comparability across CBESS networks.
- Supports inter-site analyses of coastal sedimentation, elevation changes, and habitat-related sediment dynamics.

## What is included
- Basic dataset description: surface elevation relative to an rSET instrument on a local benchmark; depths of sediment above a feldspar marker horizon.
- Staff: Tom Spencer, Ben Evans.
- Locations: Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands).
- Habitats: saltmarsh and mudflat; contrasting soil types (clay vs. sandy) and inundation/vegetation differences.
- Monitoring: observations collected twice over a 1-year period.
- Variables: Heights at Pin 1–9; Horizon depths at Core 1–3.
- Data format: Excel spreadsheets; GPS coordinates in dataset CBESS_gps_wave_transects.
- References and standards: follows Rod Surface Elevation Table methodology (Cahoon et al. 2002); Leica RTK real-time corrections for calibration.

## Locations and sampling design
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Habitat contrasts:
  - Saltmarsh: two contrasting soils in Essex (clay) vs Morecambe Bay (sandy).
  - Mudflat: Essex (cohesive clays, mud/silt) vs Morecambe Bay (coarse, mobile sediments).
- GPS accuracy: coordinates accurate to better than 50 mm; OSGB1936 coordinate system.

## Measurements and instruments
- Instruments: Rod Surface Elevation Table (rSET) with receivers bolted to benchmark rods; top of rod cemented into protective casing.
- Benchmark deployment: autumn 2012; typically 6–12 m depth into substrate.
- Measurements: nine pins in each of four quadrants around each benchmark; readings every 3–6 months.
- Marker horizons: 50 cm x 50 cm potash feldspar horizons placed just beyond instrument reach; depths measured from horizon to surface in cores.
- Cores: three horizons per core; if horizon not horizontal, depth estimated from multiple sides; <1 mm sediment recorded as 0 mm; NA indicates horizon not detectable.
- Data notes: Field notes recorded for significant factors affecting results.
- GPS data: coordinates for SET benchmarks provided; linked to CBESS_gps_wave_transects dataset.

## Data format and fields
- File format: Excel spreadsheets.
- Key dataset fields (examples):
  - Season (Winter/Summer)
  - Location (Morecambe/Mass/ Essex)
  - Site (e.g., Cartmel Sands, Abbotts Hall)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper limit)
  - Record (order of analysis)
  - Date (DD.MM.YYYY)
  - Time
  - SET Number (increases landward)
  - Pin 1–9 (mm readings)
  - Marker horizon depths (Core 1–3) (mm)
  - Notes/comments on readings
- Dataset-level notes: NA values indicate measurements not performed; data quality checks not fully detailed in the dataset (NA for some quality-control fields).

## Data quality, limitations, and notes
- Patchy data and NA values in places (evidence of incomplete measurements or unavailable horizons).
- Data collected within a defined 1-year monitoring window; long-term trends require integration with other CBESS datasets.
- Data are stored in Excel spreadsheets, which may require careful handling for reproducibility and merging with other datasets.
- Some fields (calibration, data checking) are marked NA, indicating limited metadata on QA processes in this document.

## How to use for analysis and data products
- Suitable for time-series analysis of elevation changes relative to rSET across sites and habitat types.
- Enables cross-site comparisons of sediment deposition depths above horizon markers.
- Can be joined with CBESS_gps_wave_transects for geospatial visualizations and mapping of instrument locations.
- Useful for building dashboards or pivot tables to explore by site, habitat, season, or measurement type (Pin readings vs. horizon depths).
- Data transformations may include converting OSGB1936 coordinates to other systems, unit harmonization (mm), and aligning sampling intervals (3–6 months).

## References and provenance
- Methodology based on Rod Surface Elevation Table standard (Cahoon et al., 2002).
- Calibration using Leica RTK corrections in real time.
- Related data: CBESS_gps_wave_transects dataset containing GPS locations of benchmarks and horizons.