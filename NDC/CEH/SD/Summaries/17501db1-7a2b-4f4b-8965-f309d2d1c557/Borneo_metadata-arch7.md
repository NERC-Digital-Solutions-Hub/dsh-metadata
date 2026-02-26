# Extreme and Highly Heterogeneous Microclimates in Selectively Logged Tropical Forests

## Overview
- Empirical study in Sabah, Borneo examining microclimate variability across a gradient of logging intensity (old growth, moderately logged, heavily logged) within three 1-hectare plots.
- Develops a microclimate thermal proxy sensitive to radiative, convective, and conductive heat fluxes, intended as a rough proxy for conditions experienced by small organisms.
- Integrates ground-based microclimate measurements with topography, canopy structure, and airborne LiDAR-derived canopy data to map fine-scale spatial patterns.

## Study location and design
- Three sites along a logging intensity gradient in Sabah, Malaysia, each with a 1-hectare plot representing unlogged, moderately logged, and heavily logged forest.
- Mapped and sampled across space and time to capture microclimate heterogeneity within each plot.

## Microclimate measurements
- Dataloggers: Thermochron iButtons deployed on a semi-regular grid with 1–14 m spacing, totaling 239 units; 28 days of data at 20-minute intervals (deployment late 2015; November 1–9 start dates).
- Sensor setup: No radiation shields; sensors placed at 1–3 cm above forest floor to reflect boundary-layer conditions experienced by small organisms.
- Resolution and coverage: 25 subplots per plot (20 m × 20 m each) with centralized data loggers; random high-resolution sampling in three focal subplots per plot (cross-type design).
- Recovery: 214 of 239 dataloggers recovered (90%); some moved slightly or failed due to damage.
- Temperature proxy: Reflects a combination of conductive, convective, and radiative heat fluxes rather than pure air temperature.

## Air temperature data integration
- On-plot sensors: HOBO devices at 1.5 m height within radiatively exposed subplots.
- Off-plot data: Weather stations located 1.4–3.9 km away (cleared sites) to represent broader conditions; calibration and LOESS-based predictions used to estimate missing values for the old-growth plot.
- Time synchronization: Start times aligned within plots to ensure comparability.

## LiDAR and topography data
- Airborne LiDAR: Leica ALS50-II, ~41 points/m², up to four returns; ground and non-ground classification; 1 m canopy height model (CHM) created from first returns.
- DEM and terrain: Ground coordinates used to build a 1 m DEM via ordinary kriging; slope and cos(aspect) derived (cosine of aspect indicates southerly exposure).
- Data alignment: LiDAR-derived products aligned with field plot locations and canopy measurements.

## Forest structure and canopy metrics
- Field survey: All trees ≥10 cm DBH tallied within each plot (2016); x–y positions, height, and crown boundaries captured to map canopy shapes.
- Rasterization: Stem basal area density, canopy density, and plant area index (PAI) generated at 1 m resolution; PAI estimated from LiDAR using MacArthur–Horn method with constant κ = 0.7.
- Sampling window: 10 m neighborhood for PAI estimation on a 1 m grid; first LiDAR returns used; low-lying ground returns excluded with a 2 m cutoff.
- Limitations: Possible biases from leaf/clumping variation, leaf-angle effects, and canopy edges; κ not constrained by hemispherical photos due to saturation.

## Data products and formats
- Data Sheet S1: Raw microclimate temperature measurements (CSV) with fields for site, logger tag, time, and coordinates.
- Data Sheet S2: Spatial datasets at 1 m resolution, GeoTIFFs (Data_S2_-<Site>-<Variable>.tif) for variables including:
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
- Data Sheet S3: Raw weather station data (CSV) for off-plot and on-plot air temperatures.
- Projections: All datasets in UTM Zone 50N; data integrated on a 1 m grid to support GIS analyses and microclimate mapping.

## Analytical approach and usage
- GIS-ready integration: Combine microclimate proxy data with LiDAR-derived canopy structure and topography to map fine-scale microclimate variation.
- Potential applications: Understanding how selective logging shapes microclimates, informing ecological and conservation planning, and linking microclimate patterns to plant regeneration and animal behavior.

## Key notes and considerations
- Data gaps: Some dataloggers failed or were damaged; 90% recovery rate achieved.
- Measurement caveats: The microclimate proxy is a surrogate measurement lacking radiation shields; best used as a relative indicator of microhabitat conditions rather than exact air temperature.
- Off-plot temperature estimation: LOESS-based calibration used where on-plot data were missing, with a residual error around 0.9°C.