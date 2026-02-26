# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations for instruments and features associated with wave monitoring and sedimentation-erosion table installations in saltmarsh and mudflat habitats

## Purpose and scope
- Documents GPS locations for instruments and features used in wave monitoring and sedimentation-erosion table (SET) installations in saltmarsh and mudflat habitats.
- Provides surface elevation relative to a rod SET instrument on local benchmarks and depths of sediment deposited above feldspar marker horizons adjacent to the SET benchmarks.

## Study sites and habitat contexts
- Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM) representing contrasting habitats and soil types (clay soils).
- Morecambe Bay: Cartmel Sands (CS) representing sandy soils.
- Habitat contrasts: saltmarsh vs mudflat; differences in inundation frequency, creek structure, and dominant vegetation.
- Coordinates and GPS data cover benchmarks and horizon markers across these sites, with associated dataset CBESS_gps_wave_transects.

## Methods and instrumentation
- Installations started in autumn 2012; monitoring conducted twice over a 1-year period.
- Instrumentation: Rod Surface Elevation Table (SET) to enable inter-comparability across a global network; receivers attached to benchmark rods and cemented into substrate.
- Benchmark coordinates were measured with Leica GS08 GNSS (OSGB1936 coordinate system) with accuracy better than 50 mm in all directions.
- 9 pins per benchmark (in four quadrants around each benchmark) and 50 cm × 50 cm feldspar marker horizons installed just beyond instrument reach; cores measured for sediment depth above horizons.
- Depth measurements: depths recorded in millimetres; for non-horizontal horizons, mean depth from multiple core measurements; 0 mm recorded where less than 1 mm of sediment is present above horizon.
- Documentation notes and metadata accompany readings (significant factors, conditions, etc.).

## Data content, structure, and variables
- Primary measurements: heights at Pins 1–9; horizon depths at Cores 1–3; SET-related readings and horizon depths captured in structured spreadsheets.
- Dataset fields (as described in the dataset documentation) include: season, location, site, habitat, quadrat numbers, scale (various spatial aggregations), reading records, date/time, SET number, pin readings (1–9), marker horizon depths (core 1–3), and notes.
- Data are stored in Excel spreadsheets; GPS coordinates for benchmarks and horizons are included in the associated dataset CBESS_gps_wave_transects.
- Data lineage references high-precision SET method (Cahoon et al., 2002) and real-time Leica RTK calibration in some instances.

## Data quality, provenance, and notes
- Staff responsible: Tom Spencer, Ben Evans.
- Quality considerations: coordinates with OSGB1936, accuracy better than 50 mm; notes field captures potential factors affecting readings; some fields marked as NA when measurements were not performed.
- Calibration: Leica RTK corrections in real-time where applicable.
- Observational cadence and field procedures are standardized to enable cross-site comparability.

## Access, related data, and references
- Related dataset: CBESS_gps_wave_transects (GPS locations of benchmarks and marker horizons).
- Core methodological references: Cahoon, D. R. et al. (2002) on high-precision wetland sediment elevation measurements and the rod surface elevation table; detailed SET design and use described at USGS Rod SET resource.
- Data format: Excel spreadsheets with detailed dataset field descriptions and coding for site, habitat, scale, and readings.

## Relevance for data leadership and data strategy
- Demonstrates comprehensive data stewardship: explicit documentation of purpose, methods, locations, and data structure; alignment with standardized measurement techniques to enable cross-network comparability.
- Emphasizes discoverability and reuse through linkage to a dedicated GPS dataset (CBESS_gps_wave_transects) and clear provenance to foundational sources.
- Highlights common data challenges for data leaders: ensuring complete metadata, managing multi-site datasets with varying habitat contexts, and maintaining data quality notes to support future use and integration.