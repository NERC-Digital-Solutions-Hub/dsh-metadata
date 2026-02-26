# Metadata - impact_invasive_grasses_cerrado

## Overview
- Metadata for a study on per-capita impacts of an invasive grass (Urochloa decumbens) across ecological organization levels in the Cerrado.
- Data identifier: abcabfe2-612c-4cab-b626-641002fc442e.
- Projects and funding: Neotropical Grassland Conservancy; FAPESP (grants 2018/09054-0, 2015/06743-0, 2018/14995-8); NERC Newton Grant NE/S011641/1.
- Data collected March–April 2019; includes measurements across microhabitat, vegetation structure, leaf traits, biomass, litter decomposition, soil CO2 efflux, and species richness.
- Study design covers invasion gradients (0, 25, 50, 75, 100% IAS cover) in two protected Cerrado areas.

## Study context and aims
- Aims to characterize how IAS abundance varies with invasion level and influences ecosystem properties across scales (microhabitat to community).
- Focus on making datasets usable and discoverable for others, with attention to user needs and data governance.

## Data collection and quality control
- Multi-step sampling along horizontal invasion gradients in 12 gradients (60 plots total; 5 x 5 m plots).
- Microhabitat: hourly light (PAR), air temperature, and humidity using HOBO sensors; sensors placed consistently within plots to avoid pseudoreplication.
- Vegetation: nine 1 m2 subplots per plot surveyed for cover using a Braun-Blanquet method; native species assigned to functional groups (graminoids, forbs, shrubs); bare soil and dead biomass recorded separately for native species and IAS.
- Specific leaf area (SLA): measured for dominant species (top ~80% ground cover) using leaf area and dry weight following standard protocols; 10 individuals per species; SLA computed as area mm2 per mg.
- Ecosystem properties: aboveground biomass (sorted by functional group), CO2 soil efflux via soda-lime incubation (24 h), litter decomposition using Urochloa decumbens litterbags (90–160 days).
- Documentation includes data structure, units, and standard references; QA steps implemented (metadata, consistent sampling, controlled procedures).

## Study areas
- Estação Ecológica de Itirapina (EcEI), Brazil, and Parque Nacional de Brasília (PNB), Brazil.
- Locations characterized by non-converted landscapes invaded by Urochloa decumbens; long invasion history (30+ years in EcEI; 1990s in PNB).
- Vegetation: continuous herbaceous layer of C4 grasses with scattered shrubs/trees; invaded patches selected to cover invasion gradient.

## Data structure and content (7 tables)
- microhabitat: hourly environmental measurements per plot (area, plot, block, sensor IDs, time, PAR, humidity, temperature).
- specific_leaf_area (SLA): SLA measurements for dominant species; entries include area, weight, leaf identifiers, and SLA value (SLA.mm2.mg).
- cover (Ground cover): percent cover by functional_group within plots/subplots; includes area, block, plot, subplot, functional_group, cover.
- biomass: biomass data by area, block, plot, subplot, and functional_group; biomass given per area.
- richness (Plant richness): counts of richness by area, block, plot, functional_group.
- decomposition rate: -log(weight.end/weight.start)/time (k) per block/plot, with time interval and weights for decomposition bags.
- co2_efflux (Soil CO2 efflux): CO2 efflux via soda-lime method per block/plot/subplot, including weights gained, blank gains, incubation time, chamber area, and computed CO2 efflux.

## Key variables and units (selected examples)
- microhabitat: area (Brasilia or Itirapina), plot (Q0, C0, etc.), block (B1–B3, I1–I3), PAR (lux), humidity (%), temperature (°C), time stamps.
- SLA: area.mm2 (leaf area in mm2), weigth.mg (leaf weight in mg), SLA.mm2.mg (SLA value).
- Ground cover: functional_group categories (bare_soil, graminoid, shrubs, live_urochloa, etc.), cover (%).
- Biomass: biomass (kg/m2) by area, block, plot, subplot, and functional_group.
- Richness: richness counts by area, block, plot, functional_group.
- Decomposition: weight.start (mg), weight.end (mg), time (days), k (decomposition rate).
- CO2 efflux: CO2_efflux (g C m-2 day), weight_gain_g, blank_gain_g, time_h, chamber_area (m2).

## Data governance, provenance, and notes for maintainers
- Data provenance captured via a persistent dataset identifier and explicit study metadata (title, identifier, projects, funding, collection period, sites).
- Clear documentation of data collection protocols, measurement methods, and units to support interoperability and reuse.
- Funding sources and collaborations documented to aid attribution and governance.
- Potential data quality considerations:
  - Occasional missing values (e.g., NA for temperature or other sensors).
  - Complex, multi-table structure requiring careful integration (consistent keys across tables: area, block, plot, subplot, etc.).
  - Gradient-based grouping uses coded plot and block identifiers (Q/C, 0/2/5/7/1), which should be harmonized with any downstream ontology or data catalog.
- Recommended data stewardship actions:
  - Validate and harmonize categorical encodings across tables (e.g., plot codes, functional_group terms).
  - Maintain consistent time formats and UTC localization for timestamps.
  - Provide data dictionaries with explicit value domains, especially for encoded fields (plot, block, etc.).
  - Ensure traceability of SLA measurements to dominant species per plot and documentation of sampling dates.
  - Link to reference materials and standardized trait methodologies (P-TRAP, Braun-Blanquet, SLA guidelines, etc.).
- Reference list included to support methodological transparency and reproducibility.

## Reference materials
- Al-Tam F, Adam H, Dos Anjos A, et al (2013) P-TRAP: a Panicle Trait Phenotyping tool.
- Damgaard C (2014) Quantitative plant ecology: Statistical and ecological modelling of plant abundance.
- Karberg NJ, Scott NA, Giardina CP (2008) Methods for Estimating Litter Decomposition.
- Keith H, Wong SC (2006) Measurement of soil CO2 efflux using soda lime absorption.
- Pérez-Harguindeguy N, Díaz S, Garnier E, et al (2013) New handbook for standardized measurement of plant functional traits.
- Wikum DA, Shanholtzer GF (1978) Braun-Blanquet cover-abundance scale methodology.