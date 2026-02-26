# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

- Purpose and scope
  - Presents a comprehensive data collection on how prescribed fires interact with invader abundance (Urochloa decumbens) in tropical Cerrado savannas.
  - Aim is to support GIS-enabled analyses of spatial patterns and fire-vegetation interactions for biodiversity and land management.

- Study areas (spatial context)
  - Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB) in the Cerrado, Brazil.
  - Two protected areas with distinct elevations (EcEI ~700 m; PNB ~100 m) and geographic coordinates provided.
  - Invaded, non-converted landscapes dominated by C4 grasses; invasion began in the 1980s–1990s.

- Experimental design and sampling framework
  - BACI-type design with plot-level sampling unit (5 x 5 m).
  - Six invasion gradients per area based on ground cover of Urochloa decumbens: 0, 25, 50, 75, 100%.
  - Each gradient comprises five plots; gradients are organized into blocks (two gradients per block: one control, one burned).
  - Total of 30 plots per area, across three blocks (space: blocks at least 50 m apart; plots within a gradient 10 m apart).
  - Two burns occurred in the mid-dry season (2019 and 2020); the same gradient was burned to standardize fire conditions.

- Temporal scope and data collection timing
  - Plant and environmental data collected in 2019 (pre-burn) and 2021 (post-burn).
  - Burns occurred in October 2019 and September 2020.
  - Data capture spans pre- and post-fire conditions to assess short-term fire effects conditioned by invader abundance.

- Data collected and variables (why it matters for GIS)
  - Microhabitat (ground-level conditions): hourly illuminance and temperature using HOBO sensors; daily range metrics (temp_range, rh_range).
  - Vegetation and ground cover: Braun-Blanquet-style cover estimates across 9 subplots per core plot; categories include native and invasive biomass, bare soil, and dead biomass; plant height and growth-form groupings recorded.
  - Specific leaf area (SLA): species- and individual-level SLA measurements for dominant species, enabling trait-based GIS analyses.
  - Ecosystem properties: aboveground biomass by functional groups, soil CO2 efflux (gas flux maps potential), and litter decomposition rates via standardized litter bags.
  - Spatial design details: plot layout, gradient codes, and block/treatment identifiers that enable spatial joins and gradient mapping.

- Data structure and content (GIS-ready schema)
  - Data stored in fire_effects_invaded_cerrado.RData with six tables:
    - microhabitat: year, area, treatment, block, block_treatment, unit, plot, invasion, day, illuminance, temp_range, rh_range.
    - ground_cover: year, area, treatment, block, block_treatment, unit, plot, invasion, component, subplot, cover, group, height, status.
    - specific_leaf_area: year, area, treatment, block, block_treatment, unit, plot, invasion, individual, species, leaf, sla.
    - biomass: year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group, subplot, biomass.
    - soil_co2_efflux: year, area, treatment, block, block_treatment, plot, unit, efflux, invasion.
    - decomposition_rates: year, area, treatment, block, block_treatment, unit, plot, invasion, k.
  - Each table uses consistent coding for plot and invasion gradients (0, 2, 5, 7, 1 corresponding to 0%, 25%, 50%, 75%, 100%).

- GIS considerations and potential map products
  - Spatially explicit gradient framework with two sites and two time points enables:
    - Thematic mapping of invader abundance by plot and gradient level.
    - Visualization of burn vs. control effects across invasion gradients.
    - Integration with microhabitat and ecosystem-process layers (biomass, SLA, CO2 efflux, decomposition) for spatial modeling.
  - Applicable analyses include BACI-based fire response conditioned on invader density, and trait-enabled spatial analyses using SLA data.
  - Data are delivered in an RData format; GIS workflows may require exporting to CSV/GeoJSON and inferring approximate plot coordinates from the described layout (plots are 5x5 m with 10 m spacing; blocks separated by at least 50 m).

- Limitations and practical notes for GIS work
  - Spatial coordinates are provided for the study areas, but per-plot coordinates are not explicitly listed; georeferencing relies on the described plot layout.
  - Temporal scope centers on two burn events and two sampling years, which constrains long-term trend analyses.
  - Data are contained within a single RData file with six tables, requiring extraction for most GIS platforms.

- References and methodology basis
  - Aligns with established methods for ground cover estimation (Braun-Blanquet), SLA measurement, soil CO2 efflux, and decomposition rate assessments.
  - Cited methodological sources include Pérez-Harguindeguy et al. (trait measurements), Keith & Wong (CO2 efflux), and standard BACI design references.