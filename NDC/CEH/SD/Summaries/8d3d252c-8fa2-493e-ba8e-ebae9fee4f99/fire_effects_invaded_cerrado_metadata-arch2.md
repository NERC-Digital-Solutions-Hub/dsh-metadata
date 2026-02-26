# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

## Overview
- Purpose: document and describe all data associated with a study on how prescribed fire effects on tropical savannas depend on invasive grass abundance.
- Study design: BACI-type with invasion gradients (0–100% Urochloa decumbens) to assess pre- and post-fire responses.
- Timeline: data collected in 2019 (before burns) and 2021 (after burns).
- Focus area: two Cerrado protected areas in Brazil (Estação Ecológica de Itirapina and Parque Nacional de Brasília), invaded by Urochloa decumbens.

## Study Areas and Experimental Design
- Areas:
  - Itirapina EcEI (Brasilia region) and Brasília PNB (Central Brazil).
  - Vegetation characterized by a continuous herbaceous layer dominated by C4 grasses, with scattered shrubs and small trees.
  - Invasion started >30 years ago.
- Invasion gradients:
  - Six gradients per area, each with five plots representing 0, 25, 50, 75, 100% cover by Urochloa decumbens.
  - Each gradient forms two plots: one left as control, one subjected to fire.
  - Total: 30 plots per area, arranged in three blocks with at least 50 m between blocks and 10 m between plots within a gradient.
- Fire regime:
  - Two burns during the middle of the dry season: October 2019 and September 2020.
  - Entire gradient burned at once to standardize fire conditions.

## Data Tables and Key Variables
- Data file: fire_effects_invaded_cerrado.RData containing six tables:
  - microhabitat: ground-level illuminance, temperature, humidity; year, area, treatment, block, plot identifiers; daily ranges.
  - ground_cover: vegetation cover by component (bare soil, dead biomass, plant species); height; status; subplot-level data; covers by functional group.
  - specific_leaf_area: SLA for dominant species; year, area, treatment, block, plot; individual, species, leaf number; SLA value.
  - biomass: aboveground biomass by component (live/dead native, Urochloa, total); year, area, block, plot; subplot; biomass per area.
  - soil_co2_efflux: soil CO2 efflux (g C m-2 day); year, area, treatment, block, plot; unit; invasion gradient.
  - decomposition_rates: decomposition rate (k); year, area, treatment, block, plot; invasion gradient.
- Invasion coding:
  - Discrete gradient values representing percentage cover: 0 (0%), 2 (25%), 5 (50%), 7 (75%), 1 (100%).
- Vegetation and functional groups:
  - Native vs invasive; graminoids, forbs, shrubs; bare soil and dead biomass categorized accordingly.
- Data structure details:
  - Each table uses consistent identifiers (year, area, treatment, block, unit, plot) to link measurements across microhabitat, vegetation, and ecosystem properties.

## Data Collection Methods
- Microhabitat:
  - Data loggers (HOBO Pendant and HOBO Pro v2) deployed for ~130 days to capture hourly ground-level illuminance and temperature.
- Vegetation and cover:
  - Braun-Blanquet-based visual estimates within a 9 m2 core zone per plot, subdivided into nine 1 m2 subplots; cover estimates cover traditional 0–100% scales with specific rounding rules.
  - Additional measurements: bare soil and dead biomass (native vs invasive), plant height per subplot.
- Specific leaf area (SLA):
  - Dominant species selected to represent ≥80% community cover.
  - Three leaves per individual, ten individuals per species; SLA measured via LI-COR and leaf area scanning; leaves dried and weighed.
- Ecosystem properties:
  - Biomass: destructive sampling in a 0.5 x 0.5 m marginal subplot; biomass sorted into functional/group categories and dried for mass.
  - CO2 efflux: in situ gas exchange using soda-lime absorption in sealed chambers, following established methods.
  - Decomposition: litter bags (20 x 20 cm) deployed for 90, 120, and 160 days to assess decay rates.
- Sampling intensity:
  - Within each plot, sampling targets balance spatial heterogeneity and replication across gradients and treatments.

## Data Structure and Access
- Primary data format includes six tables with clearly defined columns for year, area, treatment, block, plot, invasion level, and measurement values.
- Core fields enable cross-tabulation of microhabitat conditions, vegetation structure, leaf traits, biomass, soil CO2 flux, and decomposition across fire treatments and invasion gradients.
- Purpose-built to support standardized environmental health monitoring and policy-performance assessment over time.

## Relevance for Monitoring and Policy
- Enables consistent, comparable monitoring of fire effects in invaded tropical savannas.
- Facilitates evaluation of how fire regimes interact with invasive species to influence ecosystem properties and carbon cycling.
- Provides a structured data framework that can be integrated with other monitoring datasets for broader environmental health assessments.

## Limitations and Considerations
- Data come from two protected areas with specific invasion histories; caution is needed when generalizing beyond similar systems.
- Data collection used a finite number of data loggers (20) and a discretized invasion gradient, which may influence resolution.
- Data quality relies on standardized field methods and careful cross-site consistency; documentation provides comprehensive metadata to support reproducibility.