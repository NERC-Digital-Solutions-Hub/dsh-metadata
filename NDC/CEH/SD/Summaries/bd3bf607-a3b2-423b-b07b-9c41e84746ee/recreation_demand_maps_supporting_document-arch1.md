# Predicted recreation demand across the UK

## Aim and scope
- Map predicted recreation demand as a proxy for cultural ecosystem services (CES) at 250 m resolution across the UK.
- Predict total local recreation visits (e.g., walking, hiking, cycling) using a bespoke form of the universal law of human mobility.
- Exclude urban target cells from the demand calculation (but urban cells are still used as potential source cells).

## Core method: predicted recreation demand
- Demand for target cell i is modeled as:
  - Demand_i = Attractiveness_i × sum over all source cells j of [ Population_j / (Frequency_i_j × TravelDistance_ij)^α ], with α = 2.17.
- Key components:
  - Population_j: population density in source cell j (from WorldPop 2020).
  - Frequency_i_j: visits per year from source j to target i (three scenarios: once per year, once per month, once per week).
  - TravelDistance_ij: distance between source j and target i, adjusted by road network cost.
  - Attractiveness_i: relative attractiveness of the target cell, derived from protected-area status (IUCN categories) as a proxy for appeal.
- Distance and travel cost:
  - Long-range cost-weighted distance raster (2.5 km scale) based on UK road networks to estimate travel costs between i and j.
  - Short-range component: Euclidean distance to the nearest road within the target cell.
  - Final distance decays visits with distance, favoring shorter trips and higher-population sources.

## Data inputs and parameter details
- Population density (Population_j): WorldPop unconstrained density for 2020, resampled to 250 m grid.
- Frequency (Frequency_i_j): three scenarios—1 visit/year, 12 visits/year (monthly), 52 visits/year (weekly).
- Traveling distance (TravelDistance_ij): derived from a combination of long-range 2.5 km cost-weighted road distance and short-range 250 m Euclidean distance to nearest road.
- Attractiveness (Attractiveness_i): derived from UK terrestrial protected areas (UNEP-WCMC 2022) using IUCN categories to assign relative attractiveness (II highest, V lowest, with a linear mapping so II = 1.0, V = 0.4, etc.; no-status areas receive the lowest weight).
- Road costs: cost-weights mapped to UK road types (motorways, trunk/primary/secondary/tertiary roads, overseas links, no-through roads) based on average speeds; remote cells with no roads assigned high weights to reflect walking speeds.
- Protected-area data and IUCN categories guide attractiveness; tables describe mappings and conversions used.

## Scenarios and outputs
- Three visit frequencies produce three primary datasets per attractiveness scenario:
  - Weekly, Monthly, Yearly
- For each frequency, two variants:
  - With attractiveness (Attrac)
  - Without attractiveness (NoAttrac)
- Resulting dataset names follow the pattern:
  - Weekly_250m_NonUrban_Attrac.tif
  - Weekly_250m_NonUrban_NoAttrac.tif
  - Monthly_250m_NonUrban_Attrac.tif
  - Monthly_250m_NonUrban_NoAttrac.tif
  - Yearly_250m_NonUrban_Attrac.tif
  - Yearly_250m_NonUrban_NoAttrac.tif
- Outputs are raster maps at 250 m resolution covering the UK (non-urban target cells removed from the calculation).

## Spatial structure and units
- Gridded rasters in .tif format at 250 m × 250 m resolution.
- Projection: British National Grid (OSGB 27700) with a scale factor of 0.9996.
- Raster size: 2854 cells wide by 5200 cells tall.
- Each map shows estimated number of individual visits per 250 m grid cell for the specified visit frequency.

## Data processing and workflow
- Long-range and short-range distance rasters generated to enable travel-distance calculations across all target cells.
- Urban-dominated target cells excluded using the 2020 UKCEH Land Cover Map; sources may still include urban cells.
- Calculation performed in ArcGIS Pro and Matlab; custom code available at GitHub (github.com/dhooftman72/RecreationalValue).
- 39,968 unique target-cell maps produced (one per target cell) to compute travel distances.

## Quality assurance and validation
- Full internal review by the four study authors.
- External peer review for publication in Ecological Indicators.
- Data sources are peer-reviewed or widely accepted; methods are grounded in established datasets and prior work.

## Data availability, tools, and funding
- Tools: ArcGIS Pro v2.9.0 and Matlab v7.14.0.739.
- Data and code: publicly accessible via the mentioned GitHub repository.
- Funding: Natural Environment Research Council (NERC) under AgZero+; additional support from BBSRC.

## References and data sources (key)
- Universal visitation law of human mobility (Schläpfer et al., 2021).
- WorldPop population datasets (Lloyd et al., 2019).
- UK Land Cover Map 2020 (Morton et al., 2021).
- UNEP-WCMC Protected Areas; IUCN category mappings.
- OpenStreetMap road networks (Geofabrik, 2018).
- Supporting datasets and methodological references listed in the document.