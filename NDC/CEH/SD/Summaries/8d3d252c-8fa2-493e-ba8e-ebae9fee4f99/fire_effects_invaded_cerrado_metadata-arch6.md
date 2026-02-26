# Short-term effects of prescribed fires are modulated by invader's abundance in tropical savannas

## Overview
- Dataset describing a BACI-type study on how prescribed fire interacts with invader abundance in tropical savannas (Cerrado).
- Two protected areas in Brazil: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB).
- Invader: Urochloa decumbens (invasive grass).
- Time points: before burnings in 2019 and after burnings in 2021.
- Experimental design includes invasion gradients (0–100% cover), two treatments (burning vs control), and two study areas, enabling assessment of fire effects across invasion levels.

## Study design and locations
- Experimental framework: BACI (Before-After-Control-Impact) with plots of 5 x 5 m.
- Invasion gradients: six gradients per area, each with five plots for 0, 25, 50, 75, and 100% invasive cover.
- Blocks and treatment: in each area, gradients are paired into blocks; within each block, one gradient is left unmanaged (control) and one gradient is burned (fire treatment).
- Plot layout: 30 plots per area (total 60 plots across both areas), with blocks at least 50 m apart and plots within a gradient 10 m apart.
- Fire timing: two burns during the dry season (October 2019 and September 2020) to maximize effects on invader biomass.
- Microhabitat monitoring: hourly ground-level illuminance and temperature via data loggers over ~130 days (rainy-to-dry season transition to end of dry season).

## Data collected and measurements
- Vegetation and ground cover:
  - Visual estimation of species cover using Braun-Blanquet approach across nine 1 m2 subplots per plot.
  - Cover tallies include native grasses, forbs, shrubs, bare soil, and dead biomass (live/dead for native and invader groups).
  - Measurement context: core 9 m2 area per plot subdivided into 1 m2 subplots; total cover may exceed 100% due to 3D structure.
- Specific leaf area (SLA):
  - SLA measured for dominant species representing at least ~80% of cover per community.
  - Protocol follows standardized trait measurements: multiple leaves per individual, multiple individuals per species, leaf area via LI-COR meter and image analysis, then drying and weighing.
- Biomass:
  - Destructive sampling in a 0.5 x 0.5 m subplot per plot; biomass sorted into invader (Urochloa decumbens) and native components (graminoids, forbs, shrubs) plus dead biomass.
  - Biomass dried and weighed (kg/m2).
- Decomposition:
  - Litter bag method (90–160 days) to estimate decomposition rates; materials standardized to 5 g invader biomass per bag.
- Soil CO2 efflux:
  - Gas flux measured with soda-lime incubation in opaque chambers following standard methods.
- Microhabitat and environmental context:
  - Illumination (lux), temperature, and humidity details recorded; year, area, treatment, block, and plot identifiers captured for each measurement.

## Data structure and contents
- Data file: fire_effects_invaded_cerrado.RData
- Six tables included:
  - microhabitat: ground-level illuminance, temperature, humidity; year, area, treatment, block, plot, invasion gradient, day, etc.
  - ground_cover: cover estimates by component (bare soil, dead biomass, plant species) and groups (graminoid, forb, shrub), height, status (native/invasive); includes subplot and invasion gradient details.
  - specific_leaf_area: SLA measurements by year, area, treatment, block, plot, species, leaf, and SLA value.
  - biomass: biomass per area by year, area, block, plot, treatment, and biomass category.
  - soil_co2_efflux: soil CO2 efflux values by year, area, treatment, block, plot, and invasion gradient.
  - decomposition_rates: decomposition rate (k) by year, area, treatment, block, plot, and invasion gradient.
- Column-level highlights (examples):
  - microhabitat: illuminance, day timestamp, temp_range, rh_range.
  - SLA: individual, species, leaf number, sla (mm2/mg).
  - ground_cover: component, subplot, cover (%), group, height (cm), status.
  - biomass/soil_co2_efflux/decomposition_rates: invasion gradient, plot identifiers, and respective measurement values.

## Data access and structure notes
- The dataset is organized to enable cross-table joins by year, area, block, plot, and invasion gradient, supporting comparative analyses across fire treatment and invasion levels.
- Plot naming encodes treatment and invasion level (e.g., Q2, C5 correspond to burning or control at specific invasion percentages).
- Standardized methods and references accompany the data (e.g., Braun-Blanquet cover estimation, SLA protocols, litter decomposition methods, and soda-lime CO2 flux measurements).

## Potential data products and analyses for data support
- Dashboards or reports to explore:
  - How fire treatment interacts with invasion level to affect biomass composition (native vs invader) and dead biomass.
  - Relationships between invasion gradient and microhabitat variables (illuminance, temperature), across years.
  - Effects of fire on CO2 soil efflux and on decomposition rates across invasion levels and areas.
  - Temporal comparisons between pre-burn (2019) and post-burn (2021) data within BACI framework.
- Data activities:
  - Data integration across six tables to model outcomes like invader biomass, native biomass, soil respiration, and decomposition as functions of invasion level, treatment, site, and year.
  - Trait-based analyses using SLA to examine trait shifts with invasion intensity and fire exposure.
  - Spatial/ gradient analyses to assess how patch-scale invasion affects ecosystem processes under different fire regimes.
- Practical outputs for decision-makers:
  - Evidence on whether prescribed fires reduce invader biomass and alter ecosystem processes at various invasion levels.
  - Guidance for management of invaded Cerrado landscapes in protected areas.

## References and methods (extracted from data documentation)
- Field and analytical methods cited in the dataset metadata, including:
  - P-TRAP and leaf trait measurement tools.
  - Braun-Blanquet cover-abundance approach.
  - Standard protocols for SLA, litter decomposition, and soil CO2 efflux measurements.
  - BACI design framework and related statistical considerations.