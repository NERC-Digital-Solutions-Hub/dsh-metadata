# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

## Overview
- Investigates how fire season effects interact with invasive grass (Urochloa decumbens) abundance to shape vegetation and ecosystem responses in tropical savannas (Cerrado).
- Design: Before-After, Control-Impact (BACI) across two protected areas in Brazil (EcEI and PNB) with invaded landscapes.
- Experimental setup: Six invasion gradients (0–100% U. decumbens cover) represented by 5 plots each; within each gradient one plot left as control and one burned; total 30 plots per area.
- Timeframe: Data collected pre-burn in 2019 and post-burn in 2021; two prescribed burns occurred mid-dry season (2019 and 2020).
- Data structure: All data compiled in a single RData file (fire_effects_invaded_cerrado.RData) with six linked data tables.

## Study design and sites
- Study areas: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB) in the Cerrado; both areas invaded by Urochloa decumbens.
- Invasion gradients: 0, 25, 50, 75, 100% ground cover by the invasive species; gradients organized into pairs (one unburned control, one fire treatment).
- Plot geometry: Each plot is 5 x 5 m; blocks separated by at least 50 m; gradients within blocks arranged to ensure independent invaded patches.
- Fire regime: Two burn events during the dry season to maximize biomass reduction; whole-gradient burns performed with head-fires by the local fire brigade.
- Microhabitat monitoring: Data loggers (HOBO Pendant and HOBO Pro v2) used to monitor ground-level illuminance and temperature hourly over a minimum of 130 days (transition from rainy-dry to end of dry season).

## Data collected and measurements

- Microhabitat (ground-level conditions)
  - Illumination (lux) and temperature; recorded hourly.
  - Temporal coverage: at least 130 days per block/plot period.
  - Key fields include year, area, treatment, block, block_treatment, unit, plot, invasion gradient, day, temp_range, rh_range.

- Vegetation and cover
  - Community composition via Braun-Blanquet-style visual cover estimates (0–100%), within a 9 m2 core zone subdivided into nine 1 m2 subplots.
  - Measurements include bare soil and dead biomass (native and invasive) and grouping by growth form (graminoids, forbs, shrubs).
  - Ground cover data fields include year, area, treatment, block, block_treatment, unit, plot, invasion, component, subplot, cover, group, height, status.

- Specific leaf area (SLA)
  - SLA measured for dominant species that collectively represent at least 80% of plot cover.
  - Sampling: 3 leaves per individual, 10 individuals per species; leaves scanned and measured; leaves dried and weighed.
  - Fields include year, area, treatment, block, block_treatment, unit, plot, invasion, individual, species, leaf, sla.

- Biomass and carbon/nutrient dynamics
  - Aboveground biomass collected in a 0.5 x 0.5 m subplot; samples sorted into functional groups and live/dead categories.
  - Biomass data fields include year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group, subplot, biomass.

- Soil CO2 efflux
  - Measured per plot using soda-lime incubation chambers following standard methods.
  - Fields include year, area, treatment, block, block_treatment, plot, unit, efflux, invasion.

- Decomposition rates
  - Litter-bag method with standardized substrate (5 g U. decumbens) exposed for 90, 120, and 160 days; used to compare decomposition across invasion gradients.
  - Fields include year, area, treatment, block, block_treatment, unit, plot, invasion, k (decomposition rate constant).

## Data structure (the six tables in fire_effects_invaded_cerrado.RData)

- Microhabitat
  - Columns: year, area, treatment, block, block_treatment, unit, plot, invasion, illuminance, day, temp_range, rh_range

- Specific leaf area (SLA)
  - Columns: year, area, treatment, block, block_treatment, unit, plot, invasion, individual, species, leaf, sla

- Ground cover
  - Columns: year, area, treatment, block, block_treatment, unit, plot, invasion, component, subplot, cover, group, height, status

- Biomass
  - Columns: year, area, block, plot, treatment, unit, block_treatment, invasion, functional_group, subplot, biomass

- Soil CO2 efflux
  - Columns: year, area, treatment, block, block_treatment, plot, unit, efflux, invasion

- Decomposition rates
  - Columns: year, area, treatment, block, block_treatment, unit, plot, invasion, k

## Data access and documentation

- Data file: fire_effects_invaded_cerrado.RData
- Documentation provides detailed descriptions of each table, data fields, and measurement protocols.
- References for methods and trait standards are included (e.g., Braun-Blanquet cover-abundance, SLA measurement standards, and BACI design guidance).

## Relevance for monitoring frameworks

- Demonstrates a robust, gradient-based BACI framework to evaluate how invasive species abundance and fire regimes jointly influence environmental health indicators.
- Integrates multi-taxon and multi-metric monitoring:
  - Microhabitat conditions
  - Plant functional composition and trait data (SLA)
  - Aboveground biomass and productivity
  - Soil processes (CO2 efflux)
  - Decomposition dynamics
- Provides a clear data structure with explicit metadata fields (year, area, treatment, block, gradient, plot, etc.), facilitating data governance, transparency, and reproducibility.
- Highlights the importance of standardized sampling, transparent data sharing, and data management at the point of data collection to support future monitoring and policy evaluation.