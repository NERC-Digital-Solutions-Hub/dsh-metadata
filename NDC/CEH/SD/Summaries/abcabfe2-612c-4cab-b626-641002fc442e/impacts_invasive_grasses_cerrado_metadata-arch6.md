# Metadata - impact_invasive_grasses_cerrado

## Overview
- Metadata for a field study on per-capita impacts of an invasive grass (Urochloa decumbens) in the Cerrado, Brazil.
- Projects and funding from Neotropical Grassland Conservancy, FAPESP, and NERC Newton grants.
- Data collected to compare ecological responses across multiple organizational levels (plot, community, ecosystem).

## Study design and scope
- Study areas: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB) in the Cerrado.
- Invasion gradient: plots spanning 0% to 100% cover by Urochloa decumbens (five 5 x 5 m plots per gradient; six gradients per area; total 12 gradients, 60 plots).
- Temporal frame: field sampling conducted March–April 2019; sensors deployed for at least 130 days from transition between rainy and dry seasons to mid-dry season.
- Plot design: each plot subdivided into a core zone (3 x 3 m) and marginal zone; core further subdivided into nine 1 m2 subplots for vegetation surveys.
- Core measurements include microhabitat, vegetation composition, leaf traits, biomass, decomposition, and soil CO2 flux.

## Data collection methods and quality control
- Microhabitat: hourly measurements of light (PAR), temperature, and humidity using HOBO sensors; one sensor kit per plot to avoid pseudoreplication.
- Vegetation surveys: Braun-Blanquet cover-abundance estimates for species; native species classified by growth form (graminoids, forbs, shrubs); records of bare soil and dead biomass (native and IAS).
- Specific leaf area (SLA): SLA measured for dominant species (covering ~80% of ground cover per plot) using leaf area and dry weight from multiple individuals; standardized leaf processing.
- Ecosystem properties:
  - Biomass: aboveground biomass sampled per plot and sorted into live/dead native and IAS categories.
  - CO2 soil efflux: soda-lime incubation method (24 h) as a proxy for soil carbon dynamics.
  - Litter decomposition: litterbags containing invasive grass material left for 90–160 days with multiple sampling intervals.
- Data quality: notes indicate variation in sampling by data type and potential data heterogeneity across plots and environments; standard protocols referenced (P-TRAP traits, Braun-Blanquet, etc.).

## Data structure and nature of recorded values
- Seven tables composing the dataset:
  - microhabitat: light (PAR), humidity, temperature; fields include area, plot, block, sen.light, sen.humi, time, PAR, humidity, temperature.
  - cover: ground- and species-level cover data; includes area, block, plot, subplot, functional_group, cover.
  - specific_leaf_area (SLA): measurements of SLA per species/plot; fields include area, block, plot, species, individual, leaf, area.mm2, weight.mg, SLA.mm2.mg.
  - biomass: aboveground biomass measurements; fields include area, block, plot, subplot, functional_group, biomass.
  - decomposition: decomposition rate data; includes area, block, plot, weight.start, weight.end, time interval, k (decomposition rate), interval.
  - richness (species richness): richness counts by area, block, plot, functional_group.
  - co2_efflux: soil CO2 efflux measurements; includes area, block, plot, subplot, weight_gain_g, blank_gain_g, time_h, chamber_area, CO2_efflux.
- Coding and structure notes:
  - Plot and block codes encode area (B = Brasilia, I = Itirapina) and gradient/season treatment indications.
  - Time and measurement units standardized (e.g., hours, days, mg, g, m2, mm2, percent).

## Key methodological details by data type
- Microhabitat: sensors placed consistently relative to plot vertices; hourly data over extended field period.
- SLA: dominant species (top ~80% cover) sampled from 10 individuals; leaves processed for area and dry weight to compute SLA.
- Ground cover and biomass: Braun-Blanquet approach for cover; biomass categorized by functional_group (e.g., live_urochloa, morta_native, shrub, graminoid, palm, etc.).
- Decomposition and CO2 efflux: standardized decomposition bags with known weights; CO2 efflux calculated using established methods; time and interval recorded for rate calculation.

## Data tables and representative fields
- Microhabitat: area, plot, block, sen.light, time, PAR, humidity, temperature.
- SLA: area, block, plot, species, individual, area.mm2, weight.mg, SLA.mm2.mg.
- Ground cover: area, block, plot, subplot, functional_group, cover.
- Biomass: area, block, plot, subplot, functional_group, biomass.
- Richness: area, block, plot, functional_group, richness.
- Decomposition rates: area, block, plot, weight.start, weight.end, time, interval, k.
- Soil CO2 efflux: area, block, plot, subplot, weight_gain_g, blank_gain_g, time_h, chamber_area, CO2_efflux.

## Potential uses and applications
- Multi-level analysis of IAS impacts across microhabitat, community, and ecosystem scales.
- Development of data products and dashboards to track invasion gradients, trait variation (SLA), biomass dynamics, decomposition rates, and soil carbon flux.
- Cross-dataset joins enabling exploration of relationships between microhabitat conditions, plant functional groups, biomass turnover, and soil CO2 efflux.
- Data suitable for quality checks, meta-analyses, and comparisons with other Cerrado or tropical savanna invasive grass studies.

## References and supporting materials
- Reference methods cited for trait measurement, vegetation analysis, litter decomposition, soil CO2 measurement, and data standards (e.g., Pérez-Harguindeguy et al., 2013; Braun-Blanquet; Karberg et al., 2008; Keith & Wong, 2006; Al-Tam et al., 2013; Damgaard, 2014; Wikum & Shanholtzer, 1978).