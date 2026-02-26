# Fine-grained sediment diffuse pollution risk mapping scenarios for the Yorkshire Derwent catchment

## Introduction
- The River Derwent, Yorkshire has a known fine-grained sediment problem.
- Diffuse pollution is often modelled with erosion risk mapping, but many studies do not integrate seasonal risk or detect bare land not captured by standard land use maps.
- In agricultural catchments, land can be bare due to cropping; future rainfall changes are rarely integrated.
- This dataset demonstrates how erosion risk varies under different scenarios, including seasonal land-use changes and climate projections.

## Collection methods
- Data produced using SCIMAP (http://www.scimap.org.uk/).
- Required inputs: elevation (5 m OS DEM), rainfall, and land use.
- Focuses on erosion risk concentrations within River Derwent channels.
- Seasonal erosion risk assessed for a year across multiple scenarios.

## Data inputs by scenario
- 1) Traditional land use maps
  - CEH 2015 land use map
  - 5 m Ordnance Survey DEM
  - Monthly 2016 rainfall data (Met Office)
- 2) Seasonal satellite-derived land use maps
  - Land use from Sentinel-2 data
  - 5 m OS DEM
  - Monthly 2016 rainfall data (Met Office)
- 3) Long-term rainfall averages
  - Land use from Sentinel-2
  - 5 m OS DEM
  - Monthly long-term average rainfall (Met Office)
- 4) Artificial drainage network integrated
  - Sentinel-2 land use
  - 5 m OS DEM
  - Artificial drainage network burned into DEM
  - Monthly average rainfall (Met Office)
- 5) Winter climate change (High Emissions 90th quartile)
  - Sentinel-2 land use
  - 5 m OS DEM
  - Artificial drainage network burned into DEM
  - UKCP09 rainfall projections for winter (High Emissions, 90th quartile)
  - Model run tested for winter
- 6) Winter climate change (High Emissions 50th quartile)
- 7) Winter climate change (High Emissions 10th quartile)
- 8) Winter climate change (Medium Emissions 90th quartile)
- 9) Winter climate change (Medium Emissions 50th quartile)
- 10) Winter climate change (Medium Emissions 10th quartile)
- 11) Winter climate change (Low Emissions 90th quartile)
- 12) Winter climate change (Low Emissions 50th quartile)
- 13) Winter climate change (Low Emissions 10th quartile)
- Note: The winter climate change scenarios include High, Medium, and Low emission quartiles and were evaluated for winter.

## Nature and units of recorded values
- Values range from 0 to 1, where 1 indicates the highest erosion risk.
- SCIMAP reports relative risk within the analyzed catchment.

## Details of data structure
- Seasonal erosion risk mapping is shown for Summer, Spring, Autumn, and Winter.
- For each scenario (1–13), data are provided per season as described above.

## Additional interpretation notes
- When displaying shapefiles with graduated colours, increase the sampling size in the layer symbology to show all data.