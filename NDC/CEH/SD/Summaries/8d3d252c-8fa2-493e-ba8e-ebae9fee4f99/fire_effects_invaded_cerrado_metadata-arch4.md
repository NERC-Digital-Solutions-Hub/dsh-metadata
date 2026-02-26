# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

- Study purpose and design
  - Investigates how prescribed fires interact with the abundance of an invasive grass (Urochloa decumbens) to affect ecosystem properties in tropical savannas.
  - Location: two protected areas in Brazil (Estação Ecológica de Itirapina, EcEI; Parque Nacional de Brasília, PNB).
  - Timeline: data collected before burnings in March/April 2019 and after burnings in 2021; two burn events occurred mid-dry season (October 2019 and September 2020).
  - Experimental design: BACI (Before-After, Control-Impact) with plots of 5 x 5 m across six invasion gradients (0, 25, 50, 75, 100% cover by U. decumbens). Each gradient forms a block pair: one gradient left unmanaged (control) and one burned (fire treatment). In total, each area contains 30 plots arranged into three blocks, distributed across gradients with at least 50 m between blocks and 10 m between plots within a gradient.

- Data domains and variables collected
  - Microhabitat
    - Ground-level hourly illuminance and temperature (using HOBO data loggers); humidity data included in microhabitat dataset.
    - Variables include year, area, treatment, block, block_treatment, unit, plot, invasion, day, temp_range, rh_range.
  - Vegetation and ground cover
    - Community composition via visual estimation of species cover (Braun-Blanquet approach) within a 9 m2 core plot divided into nine 1 m2 subplots.
    - Measurements include cover by species, bare soil, dead biomass (native and invasive), and plant growth forms (graminoids, forbs, shrubs).
    - Additional plot-level attributes per subplot: height and status (native or invasive); gradient invasion code.
  - Specific leaf area (SLA)
    - SLA measured for dominant species (top 80% cover represented). Three leaves per individual, ten individuals per species; SLA measured per leaf with leaf area (LI-COR L3000C) and area analysis via scanning.
    - Variables include year, area, treatment, block, block_treatment, unit, plot, invasion, individual, species, leaf, sla.
  - Biomass
    - Aboveground biomass collected per subplot (0.5 x 0.5 m) and sorted into functional groups and species (e.g., native grasses, natives, Urochloa decumbens live/dead, total biomass).
    - Variables include year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group, subplot, biomass (kg/m2).
  - Decomposition rates
    - Litter bag method to assess decomposition rates (k) across invasion gradients.
    - Variables include year, area, treatment, block, block_treatment, unit, plot, invasion, k.
  - Soil CO2 efflux
    - Measurements of soil CO2 efflux (g C m-2 day) using soda-lime incubation chambers.
    - Variables include year, area, treatment, block, block_treatment, plot, unit, efflux, invasion.

- Data structure and accessibility
  - The dataset is stored in a single RData file: fire_effects_invaded_cerrado.RData.
  - Six interconnected tables:
    - microhabitat: illuminance, temperature ranges, humidity ranges, and related identifiers.
    - ground_cover: component-level cover data with plot-level metadata.
    - specific_leaf_area (SLA): species- and leaf-level SLA measurements.
    - biomass: biomass by functional group and subplot.
    - soil_co2_efflux: CO2 efflux values by plot and invasion level.
    - decomposition_rates: decomposition rate (k) by plot and invasion level.
  - Coding and data conventions
    - Invasion gradient coding: 0 (0%), 2 (25%), 5 (50%), 7 (75%), 1 (100%).
    - Plot codes combine treatment letter (Q = burn, C = control) with gradient code (0, 2, 5, 7, 1).
    - Block identifiers differ by area (Brasilia: B1–B3; Itirapina: I1–I3).
    - Measurements and units follow standard ecological methods cited in the references.

- Study areas and ecological context
  - EcEI (Itirapina) and PNB (Brasília) are protected areas in which the Cerrado's herbaceous layer is dominated by C4 grasses (Urochloa decumbens as the invasive).
  - Invasion gradients reflect long-standing invasion dynamics (began in the 1980s in EcEI and 1990s in PNB).
  - Vegetation structure includes a continuous herbaceous layer with scattered shrubs and small trees; data include native and invasive species categorizations, with a focus on grass-dominated communities (graminoids, forbs, shrubs).

- Methods and standard references
  - Field methods align with established practices (e.g., Braun-Blanquet cover-abundance scale; Pérez-Harguindeguy et al. 2013 for trait measurements; Keith & Wong 2006 for CO2 efflux; Karberg et al. 2008 for decomposition; Smith 2014 BACI design).
  - SLA and leaf-area measurements used standardized protocols (e.g., LI-COR leaf area meter, scanning and image analysis for leaf area).

- Funding and provenance
  - Funded by Neotropical Grassland Conservancy, FAPESP (two grants), and NERC Newton Grant (with FAPESP collaboration).
  - Data collected by Gabriella Damasceno and field assistants as part of the second chapter of a PhD thesis.

- Relevance for data leadership and stewardship
  - Demonstrates multi-domain data integration (microclimate, vegetation structure, functional traits, biomass, soil processes) collected across a controlled experimental framework.
  - Highlights explicit data documentation and schema, facilitating reproducibility and cross-study comparisons on fire regimes, invasion dynamics, and tropical savanna ecology.
  - Provides a structured data asset with clear metadata, enabling governance, discoverability, and potential reuse for policy and conservation planning.