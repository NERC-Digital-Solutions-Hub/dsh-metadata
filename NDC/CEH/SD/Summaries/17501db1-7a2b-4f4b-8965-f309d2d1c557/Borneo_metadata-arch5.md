# Publication Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

## Aim and Context
- Empirical study in Sabah, Borneo, mapping a microclimate thermal proxy across a gradient from old growth to heavily logged forests.
- Aim to link microclimate variation to processes like plant regeneration, animal behavior, and soil nutrient fluxes.
- Integrated data from ground-based dataloggers, nearby weather stations, topography, and canopy structure (via ground surveys and airborne LiDAR).

## Study Design and Data Collection
- Three 1-hectare plots along a logging intensity gradient (old growth, moderately logged, heavily logged) in lowland mixed dipterocarp forest.
- Microclimate proxy measured with a dense array of 239 Thermochron iButton dataloggers on stakes 1–3 cm above forest floor; no radiation shields to capture conductive, convective, and radiative heat fluxes.
- Datalogger deployment: semi-regular grid within each plot, with 25 subplots of 20 × 20 m and additional high-density sampling in three focal subplots per plot (cross-type design).
- Each logger recorded 28 days of data at 20-minute intervals; deployments around early November 2015; robust synchronization across loggers.
- Recovery: 214 of 239 loggers (90%) successfully retrieved; some moved 1–2 m downslope or were damaged by animals.
- Off-plot vs on-plot temperature data collected from weather stations at nearby cleared sites; calibration/estimation used for data gaps, particularly for the old-growth plot.

## Data Types and Formats
- Temperature microclimate data (raw) provided in Data Sheet S1 (CSV) with fields: site, logger tag, time elapsed, floor temperature, and 3D coordinates (X, Y, Z).
- Spatial environmental datasets provided as Data Sheet S2 (GeoTIFFs) at 1 m resolution, including:
  - Plant_area_index, Canopy_density, Canopy_height
  - Basal_area_density, cos(Aspect), Slope, Elevation
  - Maximum_temperature, Mean_temperature, Minimum_temperature (microclimate proxy)
- Weather data provided as Data Sheet S3 (CSV) with off-plot and on-plot air temperatures.
- Canopy and topography derived from LiDAR and field surveys:
  - 1 m canopy height model from airborne LiDAR (41 points/m2; ground/non-ground classification; gaps filled)
  - DEM (1 m) interpolated from ground coordinates; slope and cosine of aspect derived
  - Forest structure metrics reconstructed into rasters: stem basal area density, canopy density, and Plant Area Index (PAI) using the MacArthur-Horn method with κ = 0.7
- Data resolution and projection: all spatial data resampled to 1 m, projected to UTM Zone 50N.

## Quality Assurance and Technical Details
- Datalogger performance: high recovery rate (90%); some devices displaced or damaged; a subset failed.
- Microclimate proxy interpretation: loggers lack radiation shields to reflect boundary-layer conditions for small organisms; proxy blends radiative, convective, and conductive heat fluxes.
- Off-plot data: calibrated LOESS model using time of day and photosynthetically active radiation to predict temperatures for a plot lacking continuous weather data; model residuals ~0.9°C.
- PAI estimation: based on LiDAR-derived canopy structure, using a constant κ and a 10 m neighborhood to mitigate saturation; acknowledges potential biases from clumping and leaf-angle variance.
- Data alignment: precise spatial positioning of subplot corners/centers and stems; careful synchronization of start times across loggers.

## Data Sharing and Documentation
- Comprehensive raw and derived data are documented in Data Sheets S1–S3, including metadata about collection methods, locations, and variables.
- Spatial data and climate metrics are provided as standardized formats (CSV and GeoTIFF) with clear naming conventions to indicate site and variable.
- Study materials emphasize reproducibility: detailed deployment design, measurement intervals, and processing steps (e.g., LiDAR processing, PAI calculation) are documented.

## Relevance and Applications
- Provides a high-resolution, multi-dimensional dataset linking microclimate heterogeneity to forest structure and disturbance (selective logging).
- Supports investigations into how microclimate variation influences ecological processes such as regeneration, behavior, and nutrient cycling in tropical forests.
- Offers a framework for data stewardship in large ecological data collections, including comprehensive metadata, standardized formats, and integration of ground and remote-sensing data.

## Governance and Stewardship Considerations
- Clear provenance and methodological transparency: full logging details, deployment schema, and processing steps enable reevaluation and reuse.
- Standardized data products, with explicit coordinate system, resolution, and variable definitions to facilitate interoperability.
- Data quality notes and limitations are explicitly documented (recovery rates, potential measurement biases, model-based estimations) to inform proper interpretation and updates.
- Data stewardship priorities reflected: metadata-rich, accessible data sheets, and interoperable formats to support discoverability, reuse, and integration with other datasets.