# Metadata - impact_invasive_grasses_cerrado

- Overview
  - Metadata for a study titled Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna, detailing all data associated with the project.
  - EIDC data identifier: abcabfe2-612c-4cab-b626-641002fc442e
  - Funders and collaborators include Neotropical Grassland Conservancy, FAPESP (multiple grants), NERC Newton, among others.

- Study aims and GIS relevance
  - Provides map-ready data and tabular datasets to assess how an invasive grass (Urochloa decumbens) affects vegetation structure, function, and ecosystem processes across invasion gradients.
  - Enables spatial analyses of invasion effects at multiple ecological levels (microhabitat, vegetation structure, biomass, decomposition, and soil CO2 flux).

- Collection methods and quality control
  - Sampling conducted in March/April 2019; two-step, scale-aware experimental design to characterize IAS abundance.
  - Horizontal invasion-gradient design with five plots along each 5 x 5 m gradient representing 0, 25, 50, 75, 100% IAS cover.
  - Two study areas: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB), both within protected areas and invaded for 30+ years.
  - Each plot subdivided into core (3 x 3 m) and marginal zones; core further divided into nine 1 m2 subplots for vegetation surveys.
  - Microhabitat: hourly light, temperature, and humidity using HOBO sensors; at least 130 days in-field per plot.
  - Data organized into seven tables with explicit data structures and units; QA/validation described in collection sections.

- Study areas (spatial scope)
  - Estação Ecológica de Itirapina (EcEI): ~700 m a.s.l.; coordinates 22°14'40"S, 47°52'29"W; invaded campo sujo with continuous herbaceous layer.
  - Parque Nacional de Brasília (PNB): ~100 m a.s.l.; coordinates 15°41'43"S, 47°54'18"W; similar invasion by Urochloa decumbens.
  - Invasions began in the 1980s (EcEI) and 1990s (PNB).

- Data structure and contents (seven tables)
  - Microhabitat: illuminance (PAR), air temperature, humidity; sensor identifiers; time stamps; area/plot/block identifiers.
  - Specific leaf area (SLA): SLA measurements for dominant species; species, individual, leaf, area (mm2), weight (mg), SLA (mm2/mg).
  - Ground cover: cover estimates by plot, block, subplot, functional group (bare soil, bromelia, dead, live vegetation, palms, shrubs, etc.).
  - Biomass: biomass by area/block/plot/subplot and functional group; live/dead distinctions.
  - Richness: species richness by area/block/plot and functional group (forbs, graminoids, shrubs, palms).
  - Decomposition rate: weight start/end, time interval, decomposition constant k, and related metadata for each plot/interval.
  - Soil CO2 efflux: CO2 efflux measurements with weight gains, blank gains, incubation time, chamber area, and derived CO2 efflux values.

- Experimental design details (key points for GIS use)
  - Gradient design: six gradients per area; 12 gradients total; 60 plots (5 x gradients x 6 gradients per area).
  - Plot structure: 5 x 5 m plots; a central core (3 x 3 m) and surrounding marginal zone; nine 1 m2 subplots per plot for vegetation surveys.
  - Microhabitat sampling: one sensor kit per plot to reduce pseudoreplication; sensors placed consistently relative to plot vertices.
  - Temporal coverage: sensors deployed for at least 130 days; decomposition and CO2 sampling involve multiple intervals (weights, times, and k-values).

- Variables, units, and data conventions (highlights)
  - Microhabitat: PAR (lux), temperature (°C), humidity (%), time stamps, area/plot/block codes.
  - SLA: area (mm2), weight (mg), SLA (mm2/mg), species and individual identifiers.
  - Ground cover and biomass: percent cover (0–100%), biomass in kg/m2 for biomass table subsets, functional groups.
  - Richness: counts of species per functional group.
  - Decomposition: weight start/end (mg), time (days), k (decomposition rate), interval labels.
  - CO2 efflux: CO2 flux (g C m^-2 d^-1), incubation time (h), chamber area (m2), weight gains (g).

- Data provenance and references
  - Reference list includes standardized trait measurement methodologies and soil/biomass analysis protocols (P-TRAP, Braun-Blanquet, SLA protocols, soda-lime CO2 efflux method, litter decomposition methods).

- Practical GIS considerations and usage
  - Suitable for creating map layers of invasion gradient intensity (0–100% IAS cover) per plot, across two protected-area sites.
  - Can be joined with microhabitat variables (PAR, temperature, humidity) to explore spatial patterns of IAS impact on habitat conditions.
  - SLA and biomass data enable thematic layers of plant functional groups and productivity across gradients.
  - Ground cover and richness tables support spatial summaries of native vs. invasive dominance and species diversity across plots.
  - Decomposition and soil CO2 efflux provide ecosystem-process layers that can be interpolated or modeled spatially to assess carbon dynamics relative to invasion intensity.
  - Note on spatial granularity: plot- and gradient-level data are available; precise plot coordinates are implied by the study areas and plot layout but may require the original field maps or supplementary metadata to georeference exactly. Coordinates at the area level are provided, which supports approximate-area mapping and site-level analyses.