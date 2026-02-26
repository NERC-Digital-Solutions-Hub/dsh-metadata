# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

## Overview
- Empirical study conducted in Sabah, Borneo, measuring a microclimate thermal proxy sensitive to radiative, convective, and conductive heat fluxes.
- Focuses on three 1-hectare plots along a logging intensity gradient: unlogged old growth, moderately logged, and heavily logged.
- Integrates microclimate data with canopy structure, topography, and weather data to characterize microclimate heterogeneity and its potential ecological implications.

## Study Design and Context
- Three 1-ha plots representing a gradient from old growth to heavy selective logging.
- Within each plot: 25 subplots (20 m x 20 m) with central litter traps; exact subplot stakes mapped in 3D.
- Randomly selected three focal subplots per plot for higher-resolution sampling.
- Deployment period: end of the dry season in 2015, with dataloggers recording for 28 days at 20-minute intervals.
- Weather data used for comparison: off-plot (open area) and on-plot (below canopy) air temperature measurements from multiple sites.

## Data Collected

### Microclimate and Temperature Proxy
- 239 dataloggers installed on PVC stakes at 1–3 cm above the forest floor (Thermochron iButtons, -30°C to 70°C) without radiation shields to capture a rough proxy of temperatures experienced by small organisms.
- Data coverage: 214 of 239 dataloggers recovered (90%), with some losses due to movement, damage, or animal interference.
- Primary data: raw microclimate temperatures recorded per logger with spatial coordinates (UTM Zone 50N).

### Spatial, Topographic, and Canopy Data
- LiDAR-derived canopy structure:
  - Canopy height model at 1 m resolution (derived from first LiDAR returns; ground and non-ground classification).
  - Canopy density and Plant Area Index (PAI) estimates mapped to 1 m grids (PAI via MacArthur-Horn method).
  - Awareness of potential biases due to canopy clumping, leaf angle, and κ = 0.7.
- Topography:
  - Digital Elevation Model (DEM) at 1 m resolution via ordinary kriging from ground coordinates.
  - Derived slope (degrees) and cosine of aspect (higher values = more southerly exposures).
- Forest structure (field surveys 2016):
  - All trees ≥10 cm DBH counted; height measured; stem positions recorded.
  - Rasterized outputs: basal area density, canopy density, and PAI (PAI downscaled to 1 m resolution).

### Weather and On-/Off-Plot Temperature Context
- On-plot air temperature sensors (HOBO U23-002) within radiation shields at ~1.5 m height in a focal subplot per plot.
- Off-plot weather stations located at ~2–4 km away, with additional calibration for the old-growth site using LOESS regression based on time and photosynthetically active radiation (PAR).

## Data Processing and Integration
- Alignment of microclimate datalogger times; synchronization across units.
- Off-plot temperature predictions for old growth via LOESS regression using time of day and PAR, due to data gaps.
- 1 m resolution spatial datasets were produced and projected to UTM Zone 50N.
- Data products and formats:
  - Data Sheet S1: Raw temperature measurements (CSV) with fields for site, logger tag, time, temperature, and coordinates.
  - Data Sheet S2: Spatial datasets (GeoTIFFs) at 1 m resolution for variables including Plant_area_index, Canopy_density, Canopy_height, Basal_area_density, cos(Aspect), Slope, Elevation, Maximum/Mean/Minimum_temperature.
  - Data Sheet S3: Raw weather station data (CSV) for off-plot and on-plot air temperatures.
- Data products are organized for reuse and further analysis, with consistent georeferencing and coordinate systems.

## Key Datasets and Access
- Raw microclimate data: Data Sheet S1 (CSV) with site, logger code, timestamp, temperature proxy, and coordinates.
- Spatial context data: Data Sheet S2 (GeoTIFFs) including:
  - Plant_area_index
  - Canopy_density
  - Canopy_height
  - Basal_area_density
  - cos(Aspect)
  - Slope
  - Elevation
  - Maximum_temperature, Mean_temperature, Minimum_temperature
- Weather context: Data Sheet S3 (CSV) for off-plot and on-plot air temperatures.
- Data formats emphasize 1 m spatial resolution and UTM Zone 50N projection for interoperability and reuse.

## Data Quality, Limitations, and Considerations
- Data gaps and losses: some dataloggers lost or punctured; 214/239 recovered.
- Proxy nature of measurements: microclimate proxy reflects a combination of conductive, convective, and radiative heat fluxes, not a direct air temperature measure; interpretation as a rough proxy for small organisms.
- Off-plot temperature calibration: LOESS-based adjustments used to estimate old-growth site temperatures due to incomplete off-plot data.
- PAI estimation caveats: κ = 0.7 is assumed; clumping and leaf-angle variability can bias canopy metrics; hemispherical photos could not constrain κ due to saturation effects.

## Implications and Potential Uses
- Enables analysis of how selective logging alters microclimate heterogeneity and the downstream effects on plant regeneration, animal behavior, and soil nutrient fluxes.
- Provides a rich, integrated dataset combining microclimate proxies with high-resolution canopy and topographic context for modeling and comparative studies across tropical forests.
- Data can support dashboards, maps, and self-serve analyses for researchers and practitioners studying land-use change and microclimate dynamics.
- Facilitates cross-disciplinary research by linking physical climate proxies with ecological processes across different logging intensities.