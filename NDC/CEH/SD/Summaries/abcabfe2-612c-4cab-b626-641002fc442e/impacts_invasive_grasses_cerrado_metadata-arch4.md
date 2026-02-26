# Metadata - impact_invasive_grasses_cerrado

- Overview of the dataset
  - Study title: Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna
  - Data identifier: abcabfe2-612c-4cab-b626-641002fc442e
  - Funders and partners: Neotropical Grassland Conservancy; FAPESP (grants 2018/09054-0, 2015/06743-0, 2018/14995-8); NERC Newton Grant (NE/S011641/1)
  - Study locations: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB), two protected Cerrado areas in Brazil
  - Sampling window: March–April 2019 (with sensors deployed through the transition from rainy to dry season into mid-dry season)
  - Scope: Gradient-based assessment of an invasive grass, Urochloa decumbens, across multiple ecological scales

- Study design and scope
  - Experimental design: Horizontal gradients of invasion with five plots representing 0, 25, 50, 75, and 100% IAS cover; six gradients per area, totaling 60 plots across 12 gradients
  - Plot structure: Each 5 x 5 m plot contains a central core (3 x 3 m) and a 1 m marginal zone; core subdivided into nine 1 x 1 m subplots for vegetation surveys
  - Microhabitat measurements: Hourly ambient light, temperature, and humidity using HOBO sensors; sensors placed consistently per plot to minimize micro-heterogeneity effects
  - Vegetation and functional groups: Dominant native and IAS species identified; classified native species into graminoids, forbs, and shrubs; bare soil and dead biomass recorded
  - Leaf trait measurements: Specific leaf area (SLA) measured for dominant species (top ~80% cover) following standardized protocols
  - Ecosystem properties: Aboveground biomass by functional group; soil CO2 efflux via soda-lime incubation; litter decomposition using IAS and native material; litter bags deployed for multiple durations
  - Data structure: Data organized into seven tables plus soil CO2 efflux data, with explicit metadata on area, plot, block, date/time, and measured variables

- Data assets and structure (seven core tables)
  - Microhabitat: Illuminance (PAR), temperature, humidity, time, sensor IDs, area, plot, block
  - Cover: Ground cover data by species and functional groups across plots (core and subplots)
  - Specific leaf area (SLA): SLA measurements for dominant species; leaf area, weight, and calculated SLA
  - Biomass: Live and dead biomass by native species and Urochloa decumbens, sorted by functional group
  - Decomposition: Decomposition bags with start/end weights, time intervals, and calculated k values
  - Richness: Species richness by functional group and plot-level context
  - CO2 efflux: Soil CO2 efflux measurements by plot/area, including incubation time, weight gains, chamber area, and calculated efflux
  - Additional decomposition data: A separate Decomposition rate table and Soil CO2 efflux table detailing weight changes, intervals, and derived rates

- Data collection details and quality control
  - Sampling dates and locations clearly documented; site coordinates provided for EcEI and PNB
  - Descriptions reference standard methods (e.g., Braun-Blanquet coverage, SLA protocols, P-TRAP, CO2 efflux methods)
  - Quality control notes: Some fields contain NA values; measurement units standardized (e.g., m, mg, g, %, lux, °C)
  - Data relationships: Data tables are cross-referenced by area, block, plot, and subplot to enable integrated analyses across scales

- Data fields and units (highlights)
  - Microhabitat: area, plot, block, sen.light, time, PAR (lux), humidity (%), temperature (°C)
  - SLA: area, block, plot, species, individual, area.mm2, weight.mg, SLA.mm2.mg
  - Biomass and richness: area, block, plot, subplot, functional_group, biomass (kg/m2) or richness (count)
  - Decomposition: area, block, plot, weight.start, weight.end, time, interval, k
  - CO2 efflux: area, block, plot, subplot, weight_gain_g, blank_gain_g, time_h, chamber_area, CO2_efflux
  - Cross-table linking: consistent use of area, block, plot identifiers to merge datasets

- Study areas and sampling coverage
  - Areas: Brasilia (PNB vicinity) and Itirapina (EcEI vicinity)
  - Gradients and plots: 12 invasion gradients (6 per area), totaling 60 plots; each plot includes core and marginal subplots for microhabitat and vegetation assessments
  - Microhabitat sensors: 20 sensors deployed (four gradients per area) to capture light, temperature, and humidity across time

- Practical implications for data usage and governance (Data Leaders perspective)
  - Data richness: Multiscale data (microhabitat, vegetation structure, leaf traits, biomass, decomposition, CO2 flux) enables cross-domain analyses of invasion impacts
  - Data discoverability and provenance: Clear metadata, data identifier, funding sources, and references support data governance and reuse
  - Data integration opportunities: Linkage across tables via area/block/plot enables comprehensive ecosystem-level analyses and policy-relevant syntheses
  - Quality considerations: Some missing values and complex, nested data structures require careful data wrangling, validation, and documentation for end users
  - Suggested data stewardship actions: 
    - Maintain a centralized data dictionary and data validation routines
    - Include geospatial coordinates and file-level metadata for reproducibility
    - Provide versioning and data provenance notes to track updates or corrections
    - Consider publishing derived, analysis-ready datasets (with clear methodology) to improve usability for cross-site comparisons

- Reference materials and methodological grounding
  - References for standard trait measurements and decomposition/CO2 methods cited (Pérez-Harguindeguy et al., Damgaard, Karberg et al., Keith & Wong, Al-Tam et al., Wikum & Shanholtzer)

- Reference
  - Al-Tam F, Adam H, Dos Anjos A, et al (2013) P-TRAP: a Panicle Trait Phenotyping tool. BMC Plant Biol 13:122
  - Damgaard C (2014) Quantitative plant ecology
  - Karberg NJ, Scott NA, Giardina CP (2008) Methods for Estimating Litter Decomposition
  - Keith H, Wong SC (2006) Soda lime CO2 efflux measurement
  - Pérez-Harguindeguy N, Díaz S, Garnier E, et al (2013) Handbook for trait measurement
  - Wikum DA, Shanholtzer GF (1978) Braun-Blanquet cover-abundance scale