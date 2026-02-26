# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Introduction
- The River Derwent in Yorkshire has a known fine-grained sediment problem.
- Diffuse pollution risk is typically modelled with erosion risk mapping, but many studies lack seasonal integration and rely on annual-average land-use maps.
- In agricultural-dominated catchments, cropping cycles leave bare land not captured by traditional land-use maps.
- The study demonstrates how erosion risk varies across scenarios, including bare land from satellite data, rainfall variations, artificial drainage, and future climate change projections.

## Collection methods and approach
- Tool: SCIMAP, requiring inputs of elevation (DEM), rainfall, and land use.
- Objective: assess seasonal erosion risk for a year and compare multiple scenarios.
- Outputs focus on erosion risk concentrations within river channels; results are relative risk within the analysed catchment.

## Scenarios and data inputs
- The study evaluates 13 scenarios across seasons. Scenarios 1–4 use current or near-term inputs; Scenarios 5–13 incorporate winter climate-change projections.
- For each scenario, inputs include land-use data, DEM, and rainfall data as specified:
  - 1) Traditional land-use maps (CEH 2015), 5 m OS DEM, monthly 2016 Met Office rainfall.
  - 2) Seasonal satellite-derived land use (Sentinel-2), 5 m OS DEM, monthly 2016 rainfall.
  - 3) Long-term average rainfall, Sentinel-2 land use, 5 m OS DEM.
  - 4) Artificial drainage network added to the DEM, Sentinel-2 land use, 5 m OS DEM, monthly rainfall.
  - 5–13) Winter climate-change scenarios using UKCP09 data, with Sentinel-2 land use, artificial drainage burned into the DEM, and rainfall projections for High, Medium, and Low emission scenarios; tested only for winter.
- Winter climate-change runs include High Emissions (90th, 50th, 10th quartiles), Medium Emissions (90th, 50th, 10th quartiles), and Low Emissions (90th, 50th, 10th quartiles).

## Data structure and seasonal framing
- Seasonal erosion risk mapping is presented for Summer, Spring, Autumn, and Winter.
- Scenarios are labeled as:
  - 1 - traditional land use
  - 2 - satellite-derived land use
  - 3 - long-term average rainfall
  - 4 - artificial drainage network
  - 5–13 - Winter climate-change variants ( High/Medium/Low emissions across 90th/50th/10th quartiles)

## Values, interpretation, and presentation
- Erosion risk values range from 0 to 1, with 1 indicating the highest relative erosion risk within the catchment.
- SCIMAP results are relative risk measures rather than absolute erosion volumes.

## Practical notes for visualization and data handling
- When displaying shapefiles, increase the sampling size in the layer symbology to ensure all data are shown.

## Relevance for monitoring framework authors
- Demonstrates integration of multiple data sources (land use, DEM, rainfall, drainage networks) to produce scenario-based erosion risk maps.
- Illustrates how seasonal and future climate scenarios can be incorporated into environmental health monitoring outputs.
- Highlights the need to manage data inputs carefully (metadata quality, data transformation, and compatibility across sources) to support transparent, decision-relevant monitoring outputs.