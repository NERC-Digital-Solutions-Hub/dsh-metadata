# Predicted recreation demand across the UK

- A UK-wide map predicting recreation demand at 250 m resolution to represent cultural ecosystem services (CES) and support map-based data products for policy, clients, and the public.
- Demand is defined as the projected visits for local outdoor recreation (e.g., walking, hiking, cycling) per 250 m grid cell, using a bespoke gravity-like equation and the universal law of human mobility.

## Key objective and approach

- Combine data on population, travel distance, visit frequency, and attractiveness to estimate local recreation demand.
- Remove urban target cells to focus on the wider landscape, while using urban areas as sources.
- Produce multiple scenarios to reflect uncertainty in visit frequency (weekly, monthly, yearly) and whether attractiveness is included.
- Provide GIS-ready rasters and accompanying data structures for map-based visualization.

## Predicted recreation demand method (Eq. 1)

- Demand per target cell i:
  - Demand_i = Attractiveness_i × Σ over all source cells j of [Population_j / (Frequency_i_j × TravelDistance_ij)^α], with α = 2.17.
  - Frequency_i_j represents visits per year; TravelDistance_ij is in kilometres.
- Notes:
  - Distance decay reduces predicted visits as distance and source population density change.
  - For densities < 1 visit per km^2, values are rounded to 0.
  - Urban target cells are excluded; urban areas are used only as sources.

## Data inputs and parameterization

- Population density: WorldPop unconstrained density (2020), 75 m resolution; resampled to 250 m and scaled by 250^2.
- Visit frequency scenarios (3): once per year (1), once per month (12), once per week (52); for each, results with and without attractiveness are produced (total of 6 datasets per target, see outputs below).
- Travel distance: two rasters combined to approximate distance from target cell center to all other cells:
  - Long-range cost-weighted distance (2.5 km) along roads (GB network).
  - Short-range Euclidean distance to nearest road within a 250 m cell.
  - Road network from OpenStreetMap; speeds adapted from 2014 GB data to derive cost-weights (Table 3).
- Attractiveness: based on protected areas (UK UNEP-WCMC) using IUCN categories; higher protection → higher attractiveness (II most attractive; V and no-status lowest). Linear scaling converts IUCN status to relative attractiveness (II = 1, V = 0.4, no status = 0.2, with other categories interpolated).
- Targeting and masking:
  - UK-wide 250 m grid; urban dominated cells removed as targets using the 2020 UKCEH Land Cover Map.
  - Source cells can be urban; target cells are non-urban.
- Data sources and validation references are from peer-reviewed or well-accepted sources.

## Data structure, formats, and outputs

- Output rasters: 250 m × 250 m resolution across the UK, in British National Grid (EPSG 27700), units in metres.
- Raster naming conventions (examples):
  - Weekly_250m_NonUrban_Attrac.tif
  - Weekly_250m_NonUrban_NoAttrac.tif
  - Monthly_250m_NonUrban_Attrac.tif
  - Monthly_250m_NonUrban_NoAttrac.tif
  - Yearly_250m_NonUrban_Attrac.tif
  - Yearly_250m_NonUrban_NoAttrac.tif
- Grid and scope details:
  - Grid size: 2854 cells wide × 5200 cells high (exact to match the described UK extent).
  - Outputs show the estimated number of visits per 250 m cell for the chosen frequency scenario.
- Distinct methodological step:
  - 2, 39,968 target-cell–specific distance maps were generated (one map per target cell) to compute TravelDistance_ij efficiently.

## Implementation and reproducibility

- Software:
  - ArcGIS Pro v2.9.0 for GIS processing.
  - Matlab v7.14.0.739 for computations.
- Code availability:
  - All codes and workflows are available at github.com/dhooftman72/RecreationalValue.
- Independence of steps:
  - The approach combines geographic data at varying resolutions, requiring data cleaning, harmonization, and careful integration across data sources.

## Quality control and validation

- Full internal team review by the paper’s authors.
- External peer review for publication in Ecological Indicators.
- Input data drawn from peer-reviewed or well-accepted sources; methods cross-validated with established references (e.g., universal visitation law, road networks, protected areas datasets).

## Data sources and references (selected)

- Population: WorldPop 2020.
- Road network and travel costs: OpenStreetMap data; 2014 GB road speeds (Statista-derived).
- Distance methodology: Long-range 2.5 km cost-weighted distance plus short-range Euclidean distance to roads.
- Attractiveness proxy: UK protected area network (UNEP-WCMC, IUCN categories II–VI; no-status areas included with scaled weights).
- Urban masking: UKCEH Land Cover Map 2020.

## Practical considerations for GIS specialists

- Produces a suite of map-ready data products that can be integrated with other spatial datasets to visualize recreation demand and CES values.
- Demonstrates handling of multi-resolution data, large-derived datasets (nearly 40k distance maps), and the application of a gravity-like model in a GIS context.
- Provides a reproducible workflow, including clear parameter choices, scenario testing, and documentation of data standards and provenance.

## Funding

- Funded by the Natural Environment Research Council (NERC) under NE/W005050/1 AgZero+.