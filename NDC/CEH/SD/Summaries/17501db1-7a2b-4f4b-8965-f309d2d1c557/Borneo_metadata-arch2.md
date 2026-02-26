# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

## Purpose and Context
- Empirical study in Sabah, Borneo measuring microclimate variation across a gradient of selective logging.
- Introduces a microclimate thermal proxy sensitive to radiative, convective, and conductive heat fluxes, relevant to plant regeneration, animal behavior, and soil nutrient fluxes.

## Study Design and Setting
- Location: three 1-hectare plots along a logging intensity gradient (old growth unlogged, moderately logged, heavily logged) in Sabah.
- Deployment: end of the dry season 2015; 239 dataloggers installed across plots.
- Subplot layout: 25 subplots per plot (20 m x 20 m), with central litter traps and fixed stake coordinates; random focal subplots selected for higher-resolution sampling.
- Monitoring duration: 28 days of data collection with 20-minute intervals.
- Data recovery: 214 of 239 dataloggers recovered (about 90%).

## Microclimate Measurement and Proxy
- Instrumentation: Thermochron iButtons installed at 1–3 cm above the forest floor; no radiation shields to reflect the boundary layer experienced by small organisms.
- Measurement density: grid-based coverage with dedicated corner and center loggers per subplot; additional cross-type sampling in focal subplots (1–5 m spacing).
- Proxy interpretation: temperatures reflect a combination of conductive, convective, and radiative heat fluxes, serving as a rough proxy for microclimate experienced by small organisms.

## Air Temperature Data and Calibration
- On-plot sensors: radiation shields, 1.5 m height, hourly measurements (HOBO U23-002).
- Off-plot data: weather stations located at SAFE base camp and Maliau Basin Studies Center, providing open-area air temperature and photosynthetically active radiation (PAR); some gaps in old-growth station data.
- Calibration approach: LOESS model to predict off-plot air temperature for the old-growth plot using time-of-day and PAR; radiator-free adjustment due to small elevation differences (residual SE ~0.9°C).

## LiDAR and Topography
- LiDAR: 2014 airborne data at ~41 points/m², up to four returns; ground/non-ground classification; 1 m canopy height model (CHM) created.
- Gap filling: CHM gaps filled by averaging neighboring cells.
- Topography: digital elevation model (DEM) at 1 m resolution via ordinary kriging; derived slope and cosine of aspect.

## Forest Structure and Canopy Metrics
- Field survey (2016): trees ≥10 cm DBH mapped for stem position, diameter, height, and crown projection.
- Derived GIS rasters (1 m resolution): basal area density, canopy density (overlying canopies per unit area), and plant area index (PAI) via LiDAR.
- PAI estimation: MacArthur-Horn method using first LiDAR returns; κ set to 0.7; 2 m ground-cutoff to avoid ground returns; spatially interpolated PAI with a 10 m neighborhood, then resampled to 1 m.
- Acknowledged potential biases in PAI due to canopy clumping, leaf-angle variation, and edges; κ cannot be constrained with hemispherical photos due to saturation.

## Data Sheets and Data Products
- Data Sheet S1: Raw temperature measurements from all microclimate dataloggers; fields include site, logger tag, time elapsed, floor temperature, and 3D coordinates.
- Data Sheet S2: Spatial datasets at 1 m resolution in GeoTIFF format, including:
  - Plant_area_index
  - Canopy_density
  - Canopy_height
  - Basal_area_density
  - cos(Aspect)
  - Slope
  - Elevation
  - Maximum_temperature
  - Mean_temperature
  - Minimum_temperature
- Data Sheet S3: Raw off-plot and on-plot weather station air temperature data with time stamps and coordinates.

## Data Quality, Limitations, and Uncertainties
- High-density microclimate data enable fine-scale environmental health assessment but are a proxy rather than direct air temperature.
- Absence of radiation shields means measurements reflect near-surface boundary layer rather than standardized air temperature.
- Off-plot data gaps required model-based imputation for some plots, introducing additional uncertainty.
- Some dataloggers were displaced or lost (animal interactions); still a high recovery rate (90%).
- PAI and canopy metrics rely on assumptions (κ value) and may exhibit biases due to canopy heterogeneity.

## Implications for Monitoring and Policy-Relevant Analysis
- Demonstrates a comprehensive, standardized approach to environmental monitoring that connects microclimate with forest structure and topography.
- Provides rich, interoperable datasets (1 m resolution rasters and time-series temperature data) suitable for long-term monitoring and policy evaluation.
- Supports data value enhancement through integration with other datasets (e.g., canopy structure, topography) and potential sharing via data portals.
- Highlights the importance of explicit data documentation (Data Sheets) to facilitate reuse, replication, and scrutiny.