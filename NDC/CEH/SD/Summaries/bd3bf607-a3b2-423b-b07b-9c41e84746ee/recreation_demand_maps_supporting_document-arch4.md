# Predicted recreation demand across the UK

## Purpose and significance
- Maps predicted local recreation demand (a cultural ecosystem service) at 250 m resolution across the UK.
- Uses a bespoke universal law of human mobility to estimate the number of visits for activities like walking, hiking, and cycling.
- Produces geospatial data products to support understanding of where recreation demand arises and how it interacts with landscape features and protected areas.
- Urban target cells are removed to focus on wide landscape recreation opportunities.

## Methodology (data, model, and workflow)
- Core equation: Demand_i = Attractiveness_i × sum over source cells j of (Population_j) / (Frequency_ij × Distance_ij^α), with α = 2.17.
- Key inputs:
  - Population density: WorldPop 2020 (0.00083333° resolution); resampled to 250 m grid (scaled by (250/75)^2).
  - Travel distance: long-range cost-weighted distance (2.5 km grid) derived from UK road networks (OpenStreetMap) plus a 250 m Euclidean short-range distance to roads.
  - Frequency: three scenarios for visit frequency to a target cell (once per year = 1, once per month = 12, once per week = 52).
  - Attractiveness: based on UK terrestrial protected areas (UNEP-WCMC 2022) using IUCN categories II–V as proxies for protection level; higher protection yields higher attractiveness via a linear mapping.
- Distance and movement details:
  - Long-range distance computed across 39,968 target-specific maps using road speeds and cost-weights (Table 3) to approximate travel time.
  - Short-range distance accounts for proximity to roads within the target cell.
  - Urban target cells are excluded based on the 2020 UKCEH Land Cover Map.
- Outputs (datasets and variants):
  - For each frequency, two variants: with attractiveness (_Attrac) and without attractiveness (_NoAttrac).
  - Six rasters total:
    - Weekly_250m_NonUrban_Attrac.tif
    - Weekly_250m_NonUrban_NoAttrac.tif
    - Monthly_250m_NonUrban_Attrac.tif
    - Monthly_250m_NonUrban_NoAttrac.tif
    - Yearly_250m_NonUrban_Attrac.tif
    - Yearly_250m_NonUrban_NoAttrac.tif
- Tools and reproducibility:
  - ArcGIS Pro v2.9.0 and Matlab v7.14.0.739 used for calculations.
  - Code and data processing workflow available at github.com/dhooftman72/RecreationalValue.

## Data structure, units, and access
- Data format: GeoTIFF rasters (.tif) at 250 m resolution, British National Grid projection (EPSG 27700) with a 0.9996 scale factor.
- Grid size: 2854 (width) × 5200 (height) cells.
- Output units: estimated number of individual visits per 250 m grid cell for the specified period (weekly, monthly, or yearly).
- File naming and descriptions reflect frequency, urban exclusion, and attractiveness inclusion.

## Quality control and validation
- Full internal review by the authors plus external peer review for publication in Ecological Indicators.
- Inputs drawn from peer-reviewed or widely accepted sources.
- Data processing approach designed to balance computational feasibility (2.5 km long-range distance maps) with the 250 m resolution requirement.

## Data sources and funding
- Population: WorldPop (2020).
- Travel distance: UK road network from OpenStreetMap; speeds/road weights derived from Statista (2014).
- Protected areas: UNEP-WCMC Protected Area Dataset (UK) with IUCN categories.
- Land cover: UKCEH Land Cover Map (2020) to exclude urban targets.
- Funding: Natural Environment Research Council (NERC) under AgZero+; data and tools developed to support sustainable farming and ecosystem service assessment.

## Implications for Data Leaders
- Demonstrates an end-to-end data product lifecycle:
  - Identification and integration of diverse data sources (demographics, infrastructure, ecology, land cover).
  - A transparent, reproducible modeling approach with clearly defined parameters and scenarios.
  - Production of user-relevant geospatial outputs with varying assumptions (with/without attractiveness) to support stakeholder needs.
- Highlights opportunities for cross-sector collaboration:
  - Combines data for policy planning, recreation management, and conservation prioritization.
  - Provides a baseline method that can be adapted to other geographies or updated as new data become available.
- Emphasizes data governance aspects:
  - Clear data provenance and versioning through cited sources and a public code repository.
  - Metadata-like clarity in file naming and data description to support discoverability and reuse.

## Limitations and considerations for implementation
- Relies on assumptions about visit frequency and attractiveness proxies; alternatives could alter results.
- Distance modelling uses a simplified two-layer distance approach (2.5 km cost-weighted plus short-range road proximity) for computational feasibility.
- Urban targets excluded; may omit urban recreation dynamics that could be relevant in other analyses.
- Data are static snapshots; periodic updates would be needed to reflect changing populations, road networks, and protected area status.

## How this aligns with a data-driven organisation
- Encourages building scalable, transparent geospatial data products that support decision-making.
- Supports recognition of data gaps and the need for ongoing data governance, discoverability, and community feedback loops to ensure outputs meet user needs.