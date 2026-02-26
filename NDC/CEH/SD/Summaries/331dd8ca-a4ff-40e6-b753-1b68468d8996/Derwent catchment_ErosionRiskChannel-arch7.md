# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Overview
- Addresses fine-grained sediment diffusion in the River Derwent, Yorkshire.
- Uses SCIMAP to model erosion risk with a focus on seasonal variation, bare land detection, and climate scenarios.
- Produces map-based, spatially explicit erosion risk outputs (0 to 1) representing relative risk within the catchment.

## Data inputs and methodology
- SCIMAP requirements: elevation (Digital Elevation Model, DEM), rainfall, and land use data.
- Inputs used across scenarios:
  - Elevation: 5 m Ordnance Survey DEM.
  - Land use sources: CEH 2015 traditional land use map; Sentinel-2 derived seasonal land use.
  - Rainfall data: monthly rainfall from the Met Office (and long-term averages where applicable).
  - Additional features: artificial drainage networks burned into the DEM for certain scenarios.
  - Climate projections: UKCP09 projections for winter across High, Medium, and Low emission scenarios (90th, 50th, 10th quartiles).
- Output focus: erosion risk concentrations in river channels, with seasonal assessments (Spring, Summer, Autumn, Winter).

## Scenarios and data layers
- 1 - Traditional land use map (CEH 2015) + DEM + monthly 2016 rainfall.
- 2 - Seasonal satellite-derived land use (bare land detectable) + DEM + monthly 2016 rainfall.
- 3 - Long-term rainfall averages + Sentinel-2 land use + DEM.
- 4 - Artificial drainage network integrated into DEM + Sentinel-2 land use + monthly rainfall.
- 5–13 - Winter climate change scenarios using UKCP09 data (High/Medium/Low emissions) across 90th, 50th, and 10th quartiles; with artificial drainage and Sentinel-2 land use. This block is tested for winter only.
- Seasonal breakdown: outputs are shown for Summer, Spring, Autumn, and Winter across all scenarios (1–13).

## Nature, units, and interpretation
- Output values: 0 to 1, where 1 indicates the highest erosion risk (relative within the analysed catchment).
- Important interpretation note: SCIMAP emphasizes relative risk within the catchment rather than absolute risk levels.

## Data structure and practical notes for GIS use
- Data presentation: seasonal erosion risk maps (Summer, Spring, Autumn, Winter) for each scenario (1–13).
- Layer handling: when displaying shapefiles with graduated colours, increase the sampling size in the layer symbology to ensure the full data range is represented.
- Reproducibility and workflow considerations:
  - Compare how traditional vs. seasonal land use maps influence erosion risk patterns.
  - Assess impact of including bare land and drainage networks on risk concentrations.
  - Explore winter-only climate scenarios to understand potential changes under UKCP09 projections.

## Relevance for GIS specialists
- Provides a comprehensive set of map-based erosion risk layers under multiple data assumptions and climate scenarios.
- Supports data integration and visualization workflows by detailing inputs, resolutions (5 m DEM), and seasonal outputs.
- Enables scenario analysis for policy colleagues, clients, or the public by illustrating spatially explicit erosion risk differences across land use, drainage, rainfall, and climate projections.