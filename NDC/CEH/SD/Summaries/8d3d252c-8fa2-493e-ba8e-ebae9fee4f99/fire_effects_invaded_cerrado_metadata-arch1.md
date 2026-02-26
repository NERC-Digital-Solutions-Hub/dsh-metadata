# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

- Two protected Cerrado areas were studied: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB), both invaded by Urochloa decumbens. Invasion started more than 30 years ago (1980s–1990s).
- Design: BACI (Before-After, Control-Impact) with 5 x 5 m plots and six invasion gradients per area (0, 25, 50, 75, 100% ground cover by Urochloa decumbens). Each gradient comprises five plots; within each area, two gradients form a block: one left unmanaged (control) and one burned (fire treatment).
- Sampling periods: before burn in 2019 and after burn in 2021; two prescribed burns occurred in the middle of the dry season (October 2019 and September 2020). Entire gradients burned at once to standardize fire conditions.
- Blocks and layout: three blocks per area (Brasilía: B1–B3; Itirapina: I1–I3) with minimum 50 m separation between blocks and 10 m between plots within a gradient.
- Data collection scope includes microhabitat conditions, vegetation structure, leaf traits, biomass, soil CO2 efflux, and decomposition across invasion gradients and treatments.

- Data collected and measurements
  - Microhabitat: hourly ground-level illuminance, temperature; daily ranges of temperature and humidity; data logged with HOBO kits (20 kits total; two blocks sampled randomly due to kit limits); field duration from transition to end of dry season.
  - Vegetation: dominance-based cover estimates for all species within a core 9 m2 plot, using Braun-Blanquet-style rankings; estimates include native and invasive biomass; bare soil and dead biomass; native groups (graminoids, forbs, shrubs).
  - Specific leaf area (SLA): target dominant species (top cover-based selection ensuring ~80% cover); three leaves per individual, ten individuals per species, three leaves per leaf area measurement; SLA in mm2/mg.
  - Ecosystem properties: aboveground biomass by component (Urochloa decumbens live/dead; native graminoids, forbs, shrubs; dead biomass) across three subplots per plot; biomass dried and weighed; carbon fluxes via soil CO2 efflux measured with soda-lime method (g C m-2 day); litter-bag decomposition tests using standardized 5 g Urochloa decumbens biomass over 90, 120, and 160 days.
  - Experimental treatments: burning (Q) vs control (C) across invasion gradients; plots labeled with codes reflecting treatment and invasion gradient, e.g., 0–100% cover gradients encoded as 0, 2, 5, 7, 1.

- Data structure and content
  - Data stored in fire_effects_invaded_cerrado.RData containing six tables:
    - microhabitat: year, area, treatment, block, block_treatment, unit, plot, invasion, illuminance, day, temp_range, rh_range.
    - ground_cover: year, area, treatment, block, block_treatment, unit, plot, invasion, component, subplot, cover, group, height, status.
    - specific_leaf_area (SLA): year, area, treatment, block, block_treatment, unit, plot, invasion, individual, species, leaf, sla.
    - biomass: year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group, subplot, biomass.
    - soil_co2_efflux: year, area, treatment, block, block_treatment, plot, unit, efflux, invasion.
    - decomposition_rates: year, area, treatment, block, block_treatment, unit, plot, invasion, k.
  - Coding and gradients:
    - plot codes use letters and numbers to indicate treatment and invasion level: Q (burn) or C (control) plus a number representing 0, 25, 50, 75, 100% cover (encoded as 0, 2, 5, 7, 1 respectively).
    - invasion levels are encoded as discrete gradients: 0 (0%), 2 (25%), 5 (50%), 7 (75%), 1 (100%).
  - Areas: Brasilia (Brasilia) and Itirapina (Itirapina).
  - Years: 2019 (pre-burn) and 2021 (post-burn).

- Methods and references
  - Field and trait measurements follow established protocols for plant functional traits and vegetation analysis (e.g., Pérez-Harguindeguy et al. SLA protocols; Braun-Blanquet cover-abundance method).
  - Decomposition and soil CO2 efflux methods reference standard approaches (e.g., litter bags at fixed intervals; soda-lime CO2 absorption as per Keith & Wong).
  - BACI design and interpretation aligned with Smith (2014) BACI framework.

- Data provenance and funding
  - Data collected by Gabriella Damasceno (and field assistants) as part of her PhD work.
  - Projects and funding from Neotropical Grassland Conservancy, FAPESP (multiple grants), and NERC Newton Grant.

- Potential analysis questions for data users
  - How does prescribed fire impact native and invasive biomass and cover across invasion gradients, before vs after fire?
  - Do fire effects interact with invader abundance to influence soil CO2 efflux and decomposition rates?
  - Are SLA and microhabitat variables (illuminance, temperature) mediators of fire response across invasion levels?
  - Can the BACI design reveal differential fire responses between the two Cerrado areas and across gradients of invader abundance?