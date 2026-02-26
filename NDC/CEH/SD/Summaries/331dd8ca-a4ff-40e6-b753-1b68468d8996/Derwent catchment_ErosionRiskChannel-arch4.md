# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Overview
- Addresses a recognized fine-grained sediment problem in the River Derwent, Yorkshire.
- Traditional erosion risk mapping often omits seasonal risk and cropping-cycle effects, and may not account for future rainfall changes.
- Study compares erosion risk across multiple scenarios using the SCIMAP framework to reveal how land use, drainage, and climate projections influence risk.

## Data inputs and sources
- SCIMAP data requirements: elevation (digital elevation model), rainfall, and land use.
- Core data type: spatially distributed erosion risk within the river channels; results are relative (0 to 1, with 1 the highest risk).
- Resolution and inputs used consistently across scenarios:
  - Digital Elevation Model: 5 m Ordnance Survey DEM
  - Rainfall: monthly data from the Met Office (2016 for some scenarios; long-term averages for others)
  - Land use: varies by scenario (traditional CEH 2015 map vs. Sentinel-2 satellite-derived maps)

## Scenarios explored
- 1) Traditional land use map (CEH 2015); 5 m DEM; 2016 Met Office rainfall
- 2) Seasonal satellite-derived land use (shows bare land); 5 m DEM; 2016 Met Office rainfall
- 3) Long-term rainfall averages; land use from Sentinel-2; 5 m DEM; long-term rainfall data
- 4) Artificial drainage network integrated into the model; land use from Sentinel-2; 5 m DEM; monthly rainfall
- 5–13) Winter climate change scenarios based on UKCP09 projections, exploring combinations of emissions level (High / Medium / Low) and quartiles (90th / 50th / 10th):
  - 5) Winter climate change (High Emissions 90th quartile)
  - 6) Winter climate change (High Emissions 50th quartile)
  - 7) Winter climate change (High Emissions 10th quartile)
  - 8) Winter climate change (Medium Emissions 90th quartile)
  - 9) Winter climate change (Medium Emissions 50th quartile)
  - 10) Winter climate change (Medium Emissions 10th quartile)
  - 11) Winter climate change (Low Emissions 90th quartile)
  - 12) Winter climate change (Low Emissions 50th quartile)
  - 13) Winter climate change (Low Emissions 10th quartile)
- Note: The climate change runs are tested only for winter; each scenario uses Sentinel-2 land use, DEM, and rainfall projections (UKCP09).

## Data structure and outputs
- Seasonal erosion risk mapping with four seasons: Summer, Spring, Autumn, Winter.
- Data organized by the 13 scenarios listed above.
- Shapefile visualization tip: when displaying, increase the sampling size in the layer symbology to show all data.

## Units and interpretation
- Erosion risk values range from 0 to 1; higher values indicate greater relative risk within the analysed catchment.

## Practical implications for data leadership and governance
- Demonstrates the value of integrating seasonal dynamics and climate projections into risk assessments.
- Highlights the need for diverse data inputs (DEM, updated land use, real-time or projected rainfall) and standardized data structures to support scenario comparisons.
- Emphasizes reproducibility and interoperability across scenarios (consistent resolution, inputs, and metadata).
- Supports evidence-based decision-making for land management, drainage planning, and policy aimed at reducing diffuse sediment risk.
- Indicates potential visualisation considerations and metadata needs to ensure discoverability and ease of interpretation for policy colleagues and partners.