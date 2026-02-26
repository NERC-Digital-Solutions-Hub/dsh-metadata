# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

## Objective and Significance
- Investigates microclimate using a thermal proxy sensitive to radiative, convective, and conductive heat fluxes.
- Demonstrates extreme and heterogeneous microclimates across a gradient from old growth to heavily logged tropical forest in Sabah, Borneo.
- Microclimate data are tied to ecological processes including plant regeneration, animal behavior, and soil nutrient fluxes.
- Integrates microclimate with topography and canopy structure to map fine-scale variation.

## Study Area and Experimental Design
- Location: Sabah, Malaysian Borneo; three 1-hectare plots along a logging intensity gradient (old growth, moderately logged, heavily logged).
- Plot structure: 25 subplots per plot (20 × 20 m each) with central litter traps; 239 dataloggers deployed on stakes at 1–3 cm above forest floor.
- Deployment timeline: late 2015; data collection lasted 28 days with 20-minute intervals.
- Data recovery: 90% of dataloggers recovered (214/239); some losses due to animal damage or displacement.

## Data Collected and Measurement Approach
- Microclimate proxy: thermally sensitive loggers (Thermochron iButton) recording temperatures to reflect small-organism heat experiences; no radiation shields to avoid measuring air temperature.
- Additional air temperature data: on-plot sensors (HOBO at 1.5 m) and off-plot weather stations (SAFE base camp and Maliau Basin) for contextual comparisons.
- Temporal alignment: start dates differed slightly among plots but weather conditions were consistently dry/hot during sampling.

## Data Integration: LiDAR, Topography, and Forest Structure
- LiDAR: 2014 airborne data (41 points/m²) used to generate a 1 m canopy height model and other canopy metrics; ground and non-ground points classified.
- Topography: digital elevation model (DEM) at 1 m resolution; slope and cosine of aspect derived per location.
- Forest structure: 2016 field census of trees ≥10 cm DBH to produce stem maps; derived grids for basal area density, canopy density, and plant area index (PAI).
- PAI estimation: MacArthur-Horn method applied to LiDAR data with κ = 0.7; 1 m grid with 10 m sampling neighborhood; limitations noted due to potential κ variability and canopy clumping.

## Data Products and Accessibility
- Data Sheet S1: Raw temperature measurements from all microclimate dataloggers (CSV with site, logger tag, time, temperature, and location).
- Data Sheet S2: Spatial datasets (GeoTIFFs, 1 m resolution, UTM zone 50N) including:
  - Plant_area_index, Canopy_density, Canopy_height, Basal_area_density
  - cos(Aspect), Slope, Elevation
  - Maximum_temperature, Mean_temperature, Minimum_temperature (microclimate proxy)
- Data Sheet S3: Raw weather station data (off-plot and on-plot air temperatures; CSV).
- Data are organized with consistent spatial reference (UTM 50N) and a standardized 1 m raster grid for integration.

## Data Quality, Limitations, and Uncertainties
- Datalogger outcomes: some units lost or damaged; 214/239 recovered (≈90%).
- Temperature proxy limitations: absence of radiation shield means proxy reflects a mix of conductive, convective, and radiative fluxes; not a direct air temperature measure.
- Off-plot data gaps: old-growth plot lacked continuous direct off-plot air temperature; LOESS model used to predict missing values with residual error ~0.9°C.
- PAI and canopy metrics: κ-based estimation can be biased by leaf clumping, leaf angle variation, and canopy edges; hemispherical photography could not constrain κ due to saturation effects.
- Temporal scope: 28-day snapshot during a dry/hot period; results reflect conditions within this window and may not capture longer-term variability.

## Implications for Data Leaders
- Demonstrates effective multi-source data integration: in situ microclimate measurements, weather data, LiDAR-derived canopy structure, and topo-graphic context to produce high-resolution environmental maps.
- Highlights governance and documentation practices:
  - Clear data sheets detailing raw measurements and spatial datasets support discoverability, provenance, and reuse.
  - Standardized spatial framework (1 m rasters, UTM 50N) facilitates cross-site comparability and integration with other data networks.
- Practical data strategy considerations:
  - Balance between granular data (1 m, 20-minute intervals) and pragmatic data recovery; plan for data loss and recovery rates.
  - Explicit metadata on measurement methods (no radiation shields, height above ground, sampling grid, synchronization) to ensure reproducibility.
  - Acknowledge and document methodological assumptions and limitations (e.g., κ in PAI, off-plot temperature predictions) to guide appropriate reuse and interpretation.
- Potential for shared, cross-site analyses:
  - The standardized data products enable integration with broader datasets on microclimate, forest structure, and disturbance regimes.
  - Co-ownership and collaboration opportunities across research networks can enhance the development of robust, comparable microclimate datasets in tropical forests.