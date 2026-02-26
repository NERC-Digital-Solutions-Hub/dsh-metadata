# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

- Study aim and scope
  - Empirical investigation of a microclimate proxy sensitive to radiative, convective, and conductive heat fluxes.
  - Focused in Sabah, Borneo, across three 1-hectare plots representing a gradient from old-growth to moderate and heavy selective logging.
  - Integrates microclimate measurements with nearby weather data, topography, and canopy structure derived from ground surveys and airborne LiDAR.

- Microclimate proxy and measurement design
  - Proxy: Temperature readings from small, inlaid dataloggers placed to reflect small-organism boundary layer experiences (conductive, convective, radiative fluxes).
  - Sensor setup: Thermochron iButtons installed at 1–3 cm above forest floor without radiation shields to avoid measuring air temperature; designed to approximate conditions for seedlings and small invertebrates.
  - Spatial deployment: 3 plots with 25 subplots each (20 m × 20 m), plus focal subsampling in randomly chosen subplots for higher resolution.
  - Datalogger density: 239 units arranged in a cross-type design around litter traps; included center and corner positions of subplots, with additional loggers 1–5 m from litter traps.
  - temporal coverage: 28 days of data per logger, starting late 2015 (end of the dry season); synchronized starts; ~90% recovered (214 of 239).

- Off-plot and on-plot weather data
  - Off-plot data: Continuous air temperature and photosynthetically active radiation from weather stations located 2–4 km away to represent open conditions.
  - On-plot data: Radiation shields installed in a representative subplot per plot; hourly temperature readings at 1.5 m height.
  - Old-growth site weather data for off-plot coverage partially missing; calibrated LOESS model using time of day and PAR where direct temperature data were unavailable.

- LiDAR and topographic data
  - LiDAR: 2014 airborne LiDAR at ~41 points per m2, up to four returns; used to build a 1 m canopy height model (CHM) and gap filling.
  - Topography: DEM created from ground coordinates; elevation interpolated to 1 m; slope and cosine of aspect calculated for each location.

- Forest structure metrics
  - Field surveys (2016): All trees ≥10 cm DBH censused; measurements included DBH, height, and stem x–y positions.
  - Canopy metrics: Convert stem maps to raster grids of basal area density, canopy density (stems per unit area), and plant area index (PAI).
  - PAI estimation: Derived from LiDAR using MacArthur–Horn method with κ = 0.7; uses first LiDAR returns; 1 m resolution with a 10 m circular sampling window to mitigate saturation; potential biases acknowledged due to canopy clumping and leaf angle variation.

- Data management and accessibility
  - Data Sheet S1: Raw microclimate temperature measurements (CSV) with site, logger tag, time, and coordinates.
  - Data Sheet S2: Spatial datasets (GeoTIFFs at 1 m resolution) including variables such as Plant_area_index, Canopy_density, Canopy_height, Basal_area_density, cos(Aspect), Slope, Elevation, Maximum/Mean/Minimum_temperature.
  - Data Sheet S3: Raw off-plot and on-plot weather station air temperatures (CSV).
  - All spatial data are projected to UTM Zone 50N; file naming follows a standardized structure for dataset retrieval and reuse.

- Study location and scale
  - Three 1-hectare plots in Sabah, Malaysian Borneo, representing a gradient of logging intensity (old growth, moderately logged, heavily logged).
  - Dense microclimate monitoring network nested within each plot to capture fine-scale heterogeneity and relationships to canopy structure and topography.

- Additional notes on data and interpretation
  - The microclimate proxy provides a rough but relevant measure for organismal processes across radiative and convective heat regimes.
  - Extensive metadata and raw datasets are provided to enable replication, cross-site comparisons, and integration with other environmental datasets.