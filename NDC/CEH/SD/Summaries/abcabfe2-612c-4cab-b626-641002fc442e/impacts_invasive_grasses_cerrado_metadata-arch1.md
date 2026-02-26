# Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna

- A dataset describing cross-scale effects of the invasive grass Urochloa decumbens in the Cerrado, designed to support correlation analyses, model development, and predictions of action impacts.
- Coverage spans microhabitat conditions, vegetation structure, functional traits, biomass and decomposition processes, soil carbon dynamics, and species richness.
- Study conducted in 2019 across two protected Cerrado areas in Brazil: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB).

## Study context and scope

- Title of the study: Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna.
- Projects and funding: Neotropical Grassland Conservancy; FAPESP-supported projects; NERC Newton Grant.
- Data identifier: abcabfe2-612c-4cab-b626-641002fc442e.
- Sampling window: March–April 2019 (fieldwork extended to a period spanning the transition from rainy to dry season and into mid-dry season).

## Study areas and invasion gradient design

- Locations:
  - Estação Ecológica de Itirapina (EcEI), Brazil.
  - Parque Nacional de Brasília (PNB), Brazil.
- Invasive species focus: Urochloa decumbens (monitoring invasion across gradients).
- Experimental design:
  - Horizontal gradient with five invasion levels: 0, 25, 50, 75, 100% IAS cover.
  - 12 invasion gradients in total (6 per area), giving 60 plots (5 plots per gradient × 6 gradients × 2 areas).
  - Plot size: 5 × 5 m with core (3 × 3 m) and marginal strip; nine 1 × 1 m subplots per plot used for surveys.
  - Gradients spaced to capture spatial heterogeneity (plots > 10 m apart; gradients > 50 m apart).
- Microhabitat sampling:
  - Sensors deployed in a subset of plots (40 kits total; 20 kits per area) to avoid plot-level pseudo-replication.
  - Hourly measurements of light, temperature, and humidity (soil surface) from early transition through mid-dry season (≥130 days in the field).

## Measurements and data components

- Microhabitat (Table 1):
  - Variables include area, plot, block, sensor IDs, time stamps, PAR (lux), humidity (%), and temperature (°C).
- Vegetation and functional traits (Table 2: SLA):
  - Dominant species identification (top ~80% ground cover) with leaf-level measurements.
  - SLA calculated as SLA.mm2.mg; data include area, block, plot, species, leaf, leaf-area measurements, weight, and SLA values.
- Ground cover and vegetation structure (Table 3):
  - Ground cover surveys across plots and subplots, including functional groups (bare soil, grasses, forbs, shrubs, live/dead components, invasive/native groups, palms, bromeliads, etc.).
  - Also documents more granular cover estimates per subplot and plot.
- Biomass and decomposition (Tables 4–6):
  - Biomass (Table 4): live and dead biomass allocated to functional groups; biomass per area and plot recorded.
  - Ground cover, biomass, and richness data integrated to describe community composition and structural changes along invasion gradient.
  - Decomposition rates (Table 6): bag-based decomposition with weight start/end, time interval, and resulting decomposition rate k calculated as -ln(weight.end/weight.start)/time.
- Richness and community metrics (Tables 5–6):
  - Richness data by area, plot, block, and functional group; includes counts of shrubs, forbs, graminoids, palms, etc.
- Soil CO2 efflux (Soil respiration) (Table 7):
  - Incubation-based CO2 efflux measurements (g C m-2 day-1) with weight gain, blank controls, chamber area, incubation time, and calculated efflux.
  - Includes multiple plots across areas, with decomposition of the data by plot and treatment context.
- Data structure summary:
  - Seven tables: microhabitat, cover, specific_leaf_area (SLA), biomass, decomposition, richness, and co2_efflux.

## Data structure and key variables by table (highlights)

- Microhabitat:
  - Columns include area, plot (coding 0/2/5/7/1 for invasion levels), block, sensor IDs, time, PAR, humidity, temperature.
- SLA (Table 2):
  - Columns include area, block, plot, species, individual, leaf, area.mm2, weight.mg, SLA.mm2.mg.
- Ground cover (Table 3):
  - Block/area/plot identifiers; subplot; functional_group; cover (%).
- Biomass (Table 4):
  - Area, block, plot, subplot; functional_group; biomass (kg/m2).
- Diversity/Richness (Table 5):
  - Area, block, plot; functional_group; richness (count).
- Decomposition rates (Table 6):
  - Area, block, plot; weight.start, weight.end; interval; k; time; etc.
- Soil CO2 efflux (Table 7):
  - Area, block, plot; weight_gain_g; blank_gain_g; time_h; chamber_area; CO2_efflux.

## Temporal and spatial scale

- Temporal scale:
  - Microhabitat sensors collected hourly over ~130 days per area; decomposition and CO2 measurements conducted across defined intervals (days to weeks) within the same season frame.
- Spatial scale:
  - Two conservation units (Brasilia and Itirapina) spanning distinct elevational and ecological contexts within the Cerrado.
  - Gradient design captures invasion levels from uninvaded to fully invaded patches.

## Data provenance, access, and references

- Funding and project provenance are specified, including multiple FAPESP and NERC grants.
- Reference methods cited for standardized trait measurement, litter decomposition, soil CO2 efflux methodology, and Braun-Blanquet cover-abundance methodology.
- Data identifier and metadata indicate careful data management, traceability, and plans to make datasets discoverable with metadata.

## Potential analyses and analytic opportunities for analysts

- Cross-scale relationships:
  - Link microhabitat conditions to invasion level and vegetation structure.
  - Explore how SLA of dominant species relates to biomass, decomposition, and CO2 efflux across invasion gradients.
- Functional-group dynamics:
  - Assess how invasive grass invasion shifts the relative abundance and richness of native functional groups (graminoids, forbs, shrubs, palms, bromeliads, etc.).
- Ecosystem processes:
  - Examine relationships between invasion level and carbon dynamics (biomass carbon pools, decomposition rates, soil CO2 efflux).
- Temporal dynamics:
  - Analyze how microclimate (light, temperature, humidity) variability over time correlates with invasion progression and ecosystem responses.
- Spatial heterogeneity:
  - Compare responses between the two areas (EcEI vs PNB) to infer context-dependent effects.

## Quality, limitations, and considerations for users

- Data quality considerations:
  - Some entries show missing values (NA) for certain sensors (temperature/humidity) or time stamps.
  - The multi-table structure requires careful data linking via area, block, plot, and subplot identifiers.
- Scale and scope:
  - The dataset emphasizes cross-scale integration (microhabitat to ecosystem processes) but is context-specific to two protected Cerrado areas and one invasive grass species.
- Documentation and reproducibility:
  - Detailed descriptions of measurement protocols and data structure support reproducibility and meta-analyses.

## Metadata and reference materials

- Data identifiers and references provided for measurement techniques (P-TRAP, Braun-Blanquet method, SLA measurement, soda-lime CO2 efflux, litter decomposition).
- Reference list includes standard methods for trait measurement, decomposition, CO2 efflux, and vegetation analysis.