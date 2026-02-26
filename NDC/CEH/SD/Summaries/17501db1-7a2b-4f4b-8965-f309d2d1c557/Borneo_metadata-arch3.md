# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

- Purpose and relevance
  - Empirically measured microclimates in Sabah, Borneo to assess a microclimate thermal proxy sensitive to radiative, convective, and conductive heat fluxes.
  - Proxy relates to broad ecological processes (plant regeneration, animal behavior, soil nutrient fluxes).
  - Integrates microclimate data with topography and canopy structure to inform environmental health monitoring and policy evaluation across disturbance gradients.

- Study location and design
  - Three sites along a logging intensity gradient in Sabah, Malaysia.
  - Each site contains a 1-hectare plot representing: unlogged old growth, moderately logged, and heavily logged forest.
  - Aimed to capture spatial and temporal microclimate variation across the gradient.

- Microclimate measurements
  - Dataloggers: 239 units (Thermochron iButton) deployed on a semi-regular grid within plots, at 1–3 cm above forest floor.
  - Coverage: 25 subplots per plot (20 m × 20 m) plus center subplots; random high-resolution sampling in three focal subplots per plot.
  - Temporal resolution: 28 days of data collection at 20-minute intervals, deployed late 2015; start times synchronized across dataloggers.
  - Sensor placement decisions: no radiation shield to capture a rough proxy for small organisms’ thermal experiences; sensors mounted on stakes with tape chosen to approximate vegetation/soil albedo.
  - Data recovery: 90% of loggers recovered (214 of 239); some losses due to movement, damage, or animal activity.

- Supporting climate and environmental data
  - On-plot and off-plot air temperature measurements for context and comparison with the microclimate proxy.
  - Off-plot stations located at SAFE base camp (2–4 km away) and at Maliau Basin Studies Center (1.4 km away) with PAR measurements; calibration for old-growth plot using LOESS regression based on time of day and PAR.
  - On-plot sensors (HOBO) set at 1.5 m height within focal subplots; hourly readings to represent near-canopy conditions.

- LiDAR, topography, and forest structure
  - LiDAR: 2014 airborne data at ~41 points per m², up to four returns; ground and non-ground classification; 1 m canopy height model.
  - Topography: digital elevation model created via ordinary kriging on subplot corners/centers and stems; slope and cosine of aspect derived per location.
  - Forest structure: field census of trees ≥10 cm DBH (2016); stem mapping for crown projection; rasterized grids for basal area density, canopy density, and plant area index (PAI).
  - Canopy metrics from LiDAR: PAI estimated using MacArthur-Horn method (PAI = -1/κ ln(β)) with κ = 0.7; sole use of first LiDAR returns; 1 m grid with 10 m sampling window; acknowledged potential biases from clumping and canopy edges.

- Data products and accessibility
  - Data Sheet S1: Raw temperature measurements from microclimate dataloggers (CSV) including site, logger tag, time, temperature, and location coordinates (UTM zone 50N).
  - Data Sheet S2: Spatial datasets at 1 m resolution (GeoTIFFs) for microclimate, topography, and canopy structure; naming convention D_S2_lhdX_lhdY.tif.
  - Data Sheet S3: Raw temperature data from off-plot and on-plot weather stations (CSV) with time and temperature fields.
  - Data are projected to UTM zone 50N; datasets cover microclimate proxies, canopy structure, and environmental covariates.

- Data quality, limitations, and methodological considerations
  - Data completeness: high but not perfect—loggers recovered in most cases; occasional loss or damage noted.
  - Calibration and gaps: old-growth air temperature data partially missing; LOESS-based imputation used for off-plot temperature estimates.
  - Microclimate proxy limitations: sensors intentionally lacked radiation shields; proxy reflects a mix of conductive, convective, and radiative heat fluxes, not a pure air temperature measure.
  - Metadata and transformation: detailed metadata provided; acknowledges potential transformation needs to ensure data usability and comparability.
  - Potential biases: canopy clumping, leaf-angle variability, and edge effects may bias PAI estimates via the MacArthur-Horn method; κ value and assumptions discussed.

- Implications for monitoring frameworks
  - Demonstrates the value of dense, ground-truth microclimate measurements across disturbance gradients for policy-relevant environmental health monitoring.
  - Highlights the importance of integrating microclimate proxies with high-resolution LiDAR-derived canopy structure and robust topographic data.
  - Emphasizes rigorous data governance, metadata quality, and open data practices to enable transparency, reproducibility, and stakeholder engagement.
  - Provides a concrete data architecture (raw measurements, derived spatial layers, and comprehensive data sheets) that can inform monitoring standards, data sharing, and decision-making in environmental management contexts.