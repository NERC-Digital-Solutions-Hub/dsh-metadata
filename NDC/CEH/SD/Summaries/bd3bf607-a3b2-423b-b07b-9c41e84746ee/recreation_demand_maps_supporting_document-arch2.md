# Predicted recreation demand across the UK

## Aim and relevance to Analysts Monitoring the Environment
- Develop a UK-wide map of predicted recreation demand at 250 m resolution to represent cultural ecosystem services (CES) from outdoor recreation (walking, hiking, cycling, etc.).
- Provide standardized, reproducible outputs suitable for monitoring environmental health and policy performance over time.
- Outputs support evidence-based assessment of landscape-level recreation demand and accessibility, with data and code available for reuse and scrutiny.

## Methodological overview
- Predicts total annual or frequency-based visits for local recreation in 250 m grid cells (i and j notation: target vs source cells).
- Uses a bespoke version of the universal law of human mobility to estimate demand, incorporating population, distance, visit frequency, and cell attractiveness.
- Distance decay is captured via a gravity-like function; higher attractiveness increases demand.
- Urban target cells are removed to focus on the wider landscape.
- Calculations performed in ArcGIS Pro and Matlab; code available on GitHub.

## Key inputs and data sources
- Population density: WorldPop unconstrained density (2020) at ~75 m, resampled to 250 m.
- Visit frequency scenarios: once per year, once per month, once per week (three output datasets per scenario).
- Travel distance: two-part distance metric:
  - Long-range cost-weighted distance (250 m scale) using a 2.5 km grid derived from UK road networks.
  - Short-range Euclidean distance to the nearest road (within 250 m).
- Roads and travel speeds: Open Street Map roads; speeds sourced from Statista (2014 GB speeds) to derive cost-weights per road type.
- Attractiveness proxy: UK terrestrial protected areas ( UNEP-WCMC 2022) mapped to IUCN categories II–V with a linear conversion to attractiveness (II highest, V lower, down to no status).
- Urban areas: identified via the 2020 UKCEH Land Cover Map and excluded as targets.

## Core equation
- Predicted recreation demand for target cell i:
  Demand_i = Attractiveness_i × sum over all source cells j of [ Population_j / (Frequency_i_j × TravelDistance_i_j)^α ]
- α = 2.17 (per Schläpfer et al., 2021); frequency is visits per year.
- Distance incorporates both long-range network distance and short-range proximity to roads. For practical computation, ~39,968 maps are generated (one per target cell).

## Outputs and data formats
- Six raster outputs per combination of frequency (Weekly, Monthly, Yearly) and attractiveness (Attrac, NoAttrac):
  - Weekly_250m_NonUrban_Attrac.tif
  - Weekly_250m_NonUrban_NoAttrac.tif
  - Monthly_250m_NonUrban_Attrac.tif
  - Monthly_250m_NonUrban_NoAttrac.tif
  - Yearly_250m_NonUrban_Attrac.tif
  - Yearly_250m_NonUrban_NoAttrac.tif
- Rasters are 250 m grain, non-urban target cells, in British National Grid projection (EPSG 27700).
- Each raster shows estimated number of visits per 250 m grid cell for the specified frequency.

## Data structure, processing details, and reproducibility
- Data grids: 2854 columns by 5200 rows; unit is visits per grid cell.
- Long-range distance: 2.5 km cost-weighted distance raster built from road networks (GB roads) and overseas links; short-range distance: Euclidean distance to nearest road within 250 m.
- Travel speeds and cost-weights: mapped per road type (motorway fastest, minor roads slower; remote cells with no roads assigned high cost).
- Protected areas: IUCN-based attractiveness weights applied to target cells; values range to reflect protection level.
- Urban target cells excluded to avoid bias toward urban recreation sites.

## Validation, quality control, and reproducibility
- All methods and outputs subjected to internal team review and external peer review for publication.
- Input data drawn from peer-reviewed or well-accepted sources.
- Funding and references provided; code and data sources detailed (including GitHub repository).

## Accessibility and use for monitoring
- Outputs enable standardized assessment of recreation demand across landscapes and over time.
- Data are designed for sharing and reuse, with clear documentation of parameters, assumptions, and scenarios.
- Provides a framework for integrating CES demand with other environmental datasets; supports scenario testing via Weekly/Monthly/Yearly options and attractiveness inclusion/exclusion.

## Limitations and assumptions to note
- Frequency scenarios are assumed in the absence of UK visit-frequency data; may not reflect actual behavior.
- Attractiveness is proxied by protected area status, which may not capture all draw factors (amenities, accessibility, cultural values).
- Urban areas are excluded as targets, potentially omitting relevant urban recreation dynamics if needed for different monitoring questions.
- Distance and travel-time estimates rely on 2014 road speeds and Open Street Map data; real-world speeds may vary.

## Funding and references
- Funded by Natural Environment Research Council (NERC) under AgZero+ programme; collaboration with Rothamsted Research and BBSRC.
- Key references include Schläpfer et al. (The universal visitation law of human mobility), UK land cover data, and protected area datasets.

## Practical takeaways for an Analytic Monitoring perspective
- Produces standardized, policy-relevant indicators of recreation demand across the UK landscape.
- Combines mobility theory with environmental protection status to reflect where recreation demand concentrates.
- Outputs are reproducible and openly auditable, with source data and code accessible for scrutiny and reuse in monitoring workflows.