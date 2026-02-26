# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

## Overview
- Dataset describes all data associated with a study on how prescribed fire impact interacts with invader abundance (Urochloa decumbens) in two Cerrado protected areas: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB).
- Temporal coverage: data collected in March/April 2019 (pre-burn) and 2021 (post-burn).
- Experimental design: BACI (Before-After, Control-Impact) with plots of 5 x 5 m. Six invasion gradients per area (0, 25, 50, 75, 100% invader cover). Each gradient forms blocks with a control (unburned) and a fire treatment (burned). Total of 30 plots per area, across three blocks.
- Treatments: burning vs control; two burn events in October 2019 and September 2020 to align fire conditions.
- Data content spans microhabitat conditions, vegetation structure, functional traits, ecosystem processes, and decomposition.

## Study areas and sampling design
- Areas:
  - EcEI (Brasilia region, 700 m a.s.l.)
  - PNB (Central Brazil, ~100 m a.s.l.)
- Invasion: non-converted landscapes invaded by Urochloa decumbens; grasses dominate herbaceous layer with scattered shrubs/trees.
- Gradient creation: plots assigned discrete invasion levels (0, 25, 50, 75, 100% cover) across gradients; plots 10 m apart within a gradient; gradients grouped into blocks (three per area) with one gradient burned and one left as control per block.
- Field campaigns:
  - Microhabitat: ground-level illuminance and temperature via HOBO sensors (20 kits total; two blocks sampled per area; 130+ days of data collection).
  - Vegetation: Braun-Blanquet cover estimates within a 9 m2 core zone, subdivided into nine 1 m2 subplots; separate estimates for native and invasive species; bare soil and dead biomass recorded.
  - Specific leaf area (SLA): measured on dominant species to capture trait variation; sampling across species to exceed 80% cover representation; three leaves per individual, ten individuals per species.
  - Ecosystem properties: aboveground biomass by subplot; CO2 soil efflux using soda lime incubation chambers; decomposition rates via litter bags at 90, 120, and 160 days.
  - Documentation: data collection protocols follow established references (Pérez-Harguindeguy et al., Braun-Blanquet method, etc.).

## Data structure and contents
- Data file: fire_effects_invaded_cerrado.RData
- Six data tables:
  - microhabitat: hourly ground-level illuminance and temperature/humidity metrics
  - ground_cover: vegetation cover by component (bare soil, dead biomass, plant species) and related metadata
  - specific_leaf_area (SLA): SLA measurements for dominant species across individuals and leaves
  - biomass: live and dead biomass by functional group and invasion gradient
  - soil_co2_efflux: soil CO2 efflux values per plot
  - decomposition_rates: decomposition rate (k) per plot
- Coding and structure highlights:
  - Year (2019 or 2021), area (Brasilia or Itirapina)
  - treatment (burning or control), block (B1-B3 in Brasilia; I1-I3 in Itirapina)
  - block_treatment: combination of block and treatment
  - unit/plot codes: letters for treatment (Q = burn, C = control) combined with gradient indicator (0, 2, 5, 7, 1) representing 0%, 25%, 50%, 75%, 100% invasion
  - invasion: invasion level represented as discrete gradient values (0, 2, 5, 7, 1)
  - specific fields per table reflect per-table specifics (e.g., SLA includes individual, species, leaf number; biomass includes functional_group and subplot; soil_co2_efflux includes efflux and invasion)

## Key methodological details and variables
- Microhabitat variables:
  - illuminance (lux), temperature/humidity ranges, year, area, treatment, block, plot, invasion level
- Ground cover details:
  - components (bare soil, dead biomass, live plant components), subplot identifiers, cover percentages, plant functional groups, height, status (native/invasive)
- SLA measurements:
  - year, area, treatment, block, block_treatment, unit, plot, invasion, individual/species/leaf identifiers, sla value (mm2/mg)
- Biomass measurements:
  - year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group categories, subplot, biomass (kg/m2)
- Decomposition rates:
  - year, area, treatment, block, block_treatment, unit, plot, invasion, k (decomposition rate)
- Soil CO2 efflux:
  - year, area, treatment, block, block_treatment, plot, unit, efflux (g C m-2 day-1), invasion

## Data usage and governance considerations
- Data are stored as a single RData file containing six interrelated tables, enabling integrated analyses across microhabitat conditions, community composition, functional traits, biomass, soil respiration, and decomposition.
- Coding conventions for plots and invasion gradients should be preserved to maintain data integrity and comparability across areas and years.
- The dataset integrates standardized trait measurement protocols (SLA) and established ecological methods (Braun-Blanquet cover estimation, litter bag decomposition, soda-lime CO2 efflux) to support reproducibility and cross-study synthesis.
- Given the structured BACI design, data can support analyses of fire effects conditioned on invader abundance and gradient-level responses over time.

## References and methodological notes
- P-TRAP: a Panicle Trait Phenotyping tool (Al-Tam et al., 2013)
- Spatial heterogeneity in herbaceous layer of savanna ecosystems (Augustine, 2003)
- Abundance of invasive grasses depends on fire regime and climate (Damasceno & Fidelis, 2020)
- Decomposition and carbon monitoring methods (Karberg et al., 2008; Keith & Wong, 2006)
- Standardized plant functional trait measurements (Pérez-Harguindeguy et al., 2013)
- BACI design principles (Smith, 2014)
- Braun-Blanquet cover-abundance scale applications (Wikum & Shanholtzer, 1978)