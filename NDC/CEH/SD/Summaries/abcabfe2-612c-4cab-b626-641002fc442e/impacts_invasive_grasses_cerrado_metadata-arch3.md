# Metadata - impact_invasive_grasses_cerrado

## Overview
- Dataset detailing a study on per-capita impacts of an invasive grass across ecological organization levels in a tropical savanna (Cerrado).
- Two protected areas (Estação Ecológica de Itirapina and Parque Nacional de Brasília) with invasion by Urochloa decumbens.
- Aims aligned with monitoring frameworks: identify environmental health measures, scrutinise policy decisions, and inform future management.
- Timeframe: field sampling in March–April 2019; microhabitat sensors deployed for ~130 days (rainy to mid-dry season).
- Data collected cover microhabitat conditions, vegetation structure, functional traits, biomass, decomposition, soil CO2 efflux, and species richness.

## Study design and sites
- Sites: Itirapina Ecological Station (EcEI) and Brasília National Park (PNB) in the Cerrado.
- Invasion gradient: five plots representing 0, 25, 50, 75, 100% IAS cover, across six gradients per area (total 12 gradients, 60 plots).
- plot design: each 5 x 5 m plot includes a core zone (3 x 3 m) and marginal 1 m strip; core subdivided into nine 1 m2 subplots for surveys.
- Sampling frames: ground cover and community structure assessed with Braun-Blanquet approach; native vs invasive species categorized; bare soil and dead biomass recorded.

## Measurements and data types
- Microhabitat (Table 1): hourly light (PAR), air temperature, humidity; sensors placed systematically to minimize heterogeneity; time-stamped measurements.
- Vegetation and ground cover (Tables 2–4): 
  - Species cover in communities; functional groups (graminoids, forbs, shrubs, etc.); percent cover estimates.
  - Specific leaf area (SLA) measurements for dominant species (SLA = area per leaf mass) following standard protocols; leaf area and weight recorded per leaf.
  - Biomass sampling: aboveground biomass per plot, sorted into native/invasive functional groups; live and dead components recorded; biomass per area (kg/m2).
- Ecosystem properties (Table 5): 
  - Biomass decomposition measured via litterbags; carbon dynamics inferred from CO2 efflux estimated by soda-lime incubation; decomposition rates calculated as k from weight changes over time.
  - Litter decomposition uses Urochloa decumbens material to standardize parental material across the gradient.
- Biodiversity and structure (Tables 6–7): 
  - Species richness by area, plot, and functional group (forbs, graminoids, palms, shrubs).
  - Soil CO2 efflux data per plot, including weight gains, blanks, chamber area, incubation time, and calculated efflux (g C m-2 d-1).

## Data structure and variables
- Seven tables capturing distinct facets:
  - Microhabitat: area, plot, block, sensor identifiers, time, PAR, humidity, temperature.
  - SLA (specific_leaf_area): area, block, plot, species, individual, leaf, area.mm2, weight.mg, SLA.mm2.mg.
  - Ground cover: area, block, plot, subplot, functional_group, cover (%).
  - Biomass: area, block, plot, subplot, functional_group, biomass (kg/m2).
  - Species richness: area, block, plot, functional_group, richness.
  - Decomposition rate: area, block, plot, weight.start, weight.end, time, interval, k.
  - Soil CO2 efflux: area, block, plot, weight_gain_g, blank_gain_g, time_h, chamber_area, CO2_efflux.
- Rows include facility-to-field mapping (e.g., area = Brasilia or Itirapina; block = B1–B3 or I1–I3; plot codes reflect burning/control design and invasion level).

## Methodologies and references
- Standardized trait and vegetation methods:
  - Specific Leaf Area: Pérez-Harguindeguy et al. (2013).
  - Litter decomposition: Karberg et al. (2008).
  - Soil CO2 efflux: Keith & Wong (2006).
  - Vegetation sampling and Braun-Blanquet approach: Wikum & Shanholtzer (1978); broader trait and ecological frameworks (Damgaard 2014).
- Data collection aligned with established protocols to support comparability and integration into monitoring frameworks.

## Data governance, accessibility, and provenance
- Metadata includes data identifier (EIDC) and project/funding details, enabling traceability and reuse.
- Multi-table structure with detailed field definitions and units enhances interoperability and policy-relevant analysis.
- Some fields contain NA values, and the design links field data to a transparent experimental gradient, improving auditability and use in monitoring dashboards.

## Relevance for monitoring frameworks
- Provides a comprehensive suite of environmental health indicators across scales:
  - Microhabitat conditions (light, temperature, humidity).
  - Biodiversity and community structure (functional group richness, percent cover).
  - Plant functional traits (SLA) and biomass dynamics.
  - Ecosystem processes (decomposition rates, soil CO2 efflux).
- Gradient-based approach supports evaluation of invasive grass impacts and the effectiveness of management interventions.
- Detailed, standardized metadata facilitates integration into monitoring platforms and policy assessments, supporting evidence-based decision making.

## Limitations and considerations for use in monitoring
- Data gaps (e.g., NA values in certain microhabitat fields) and extensive cross-table linkage requirements necessitate careful data management.
- Complex, multi-table schema requires robust data integration when comparing with other datasets.
- While richly documented, external use may depend on data-sharing policies beyond the metadata scope.