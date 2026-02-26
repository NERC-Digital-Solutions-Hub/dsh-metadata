# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Aim and context
- Addresses fine-grained sediment (diffuse pollution) risk in the River Derwent, Yorkshire.
- Highlights limitations of traditional land use maps (they may miss seasonal bare land) and the lack of integration of rainfall changes and future climate projections in erosion risk assessments.
- Demonstrates how erosion risk varies under different scenarios, including seasonal land use, rainfall, drainage networks, and climate change projections.

## Data inputs and methods
- Tool: SCIMAP (requires elevation DEM, rainfall, and land use).
- Data sources:
  - Land use: traditional CEH 2015 map; seasonal satellite-derived land use (Sentinel-2).
  - Elevation: 5 m Ordnance Survey DEM.
  - Rainfall: monthly Met Office data (2016) or long-term averages.
- Model enhancements:
  - Incorporation of artificial drainage network by burning into the DEM.
  - Future climate scenarios using UKCP09 projections (winter only in this study), across High, Medium, and Low emissions.

## Scenarios analyzed
- Five core scenario types, each examined across seasonal contexts:
  - 1) Traditional land use map (CEH 2015).
  - 2) Seasonal satellite-derived land use (shows bare land).
  - 3) Long-term average rainfall.
  - 4) Integration of artificial drainage network.
  - 5–13) Winter climate change scenarios under High/Medium/Low emissions and 90th/50th/10th quartiles (i.e., 9 additional winter climate-change variants).

## Seasonal scope and outputs
- Seasonal erosion risk mapping for:
  - Summer, Spring, Autumn, and Winter.
- Output values:
  - Range 0 to 1, where 1 indicates the highest erosion risk.
  - Values are relative within the analyzed catchment.

## Data structure and interpretation
- Presented as multiple layers corresponding to:
  - The 13 scenarios (1–4 plus 5–13) across the four seasons.
- Important note for visualization:
  - When displaying shapefiles with graduated colors, increase the sampling size in the layer’s symbology to show all data.

## Practical considerations and limitations
- UKCP09 winter-only climate-change runs limit interpretation for other seasons.
- The approach emphasizes how different data inputs (land use, drainage, rainfall, climate change) alter erosion-risk conclusions.
- Data integration challenges highlighted (e.g., bare land detection via satellites, aligning multiple data sources).