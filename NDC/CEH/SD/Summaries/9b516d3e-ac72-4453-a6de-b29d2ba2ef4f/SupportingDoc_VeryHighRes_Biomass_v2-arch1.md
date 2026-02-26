# Biomass Maps for Zones of Interest (ZOI) Using Random Forest Regression

## Overview
- Each biomass raster value represents dry biomass in tonnes per hectare (t/ha).
- Biomass maps were produced using random forest regression models implemented in R for four Zones of Interest (ZOIs).

## Data and Training
- Training data: 134 biomass plots spread across the four ZOIs.
  - For each plot: unique label, town location, land cover type (closed canopy, tree fallow, shrub fallow, tany maty), latitude and longitude, biomass measurement method (plot or transect), elevation, and biomass components (trees >5 cm DBH, understory, and total above-ground biomass).
- Biomass values were calculated per land cover type within each ZOI and across all ZOIs.
  - Example means (t/ha) across all ZOIs: Closed Canopy Forest ~87, Tree Fallow ~16, Shrub Fallow ~12, Tany Maty ~8.
- A point shapefile for each ZOI was created to provide training data; only aboveground biomass used as the training target, assigned to a single pixel for each point.

## Data and Predictors
- Predictors: a 4-band multispectral image at 6 m resolution.
- Land cover preprocessing: very-high-resolution land cover imagery used to mask clouds; 1.5 m land cover pixels were aggregated to 6 m using the mode to align with predictor resolution.

## Modeling Workflow
- For each ZOI, random forest regression relates image spectral signatures to biomass training data to predict biomass for each pixel.
- Training data links spectral signatures to biomass classes within each ZOI.

## Quality Control and Limitations
- Because training data may not capture the full spectral variation in heterogeneous areas and training points are limited, some predicted values may be erroneous if the spectral range is not represented.
- Data access, scale, and the need for domain expertise can impact interpretation and reliability of results.

## Data Structure
- The dataset consists of four rasters in .tif format, one per ZOI.