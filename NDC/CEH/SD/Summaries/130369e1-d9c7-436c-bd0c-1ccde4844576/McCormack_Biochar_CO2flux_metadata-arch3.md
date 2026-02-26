# Pot_number  Unique identifier for each individual mesocosm

- Purpose: Describes a mesocosm experiment dataset capturing CO2 flux and photosynthesis under different treatments to support environmental health monitoring, policy scrutiny, and informing future decisions.

- Data scope and structure:
  - Identifiers and layout:
    - Pot_number: Unique identifier for each mesocosm.
    - Block: Spatial block within the enclosure; in a fully factorial design, one replicate of each treatment is represented in each of four blocks.
  - Treatments and environmental factors:
    - Presence of 2% biochar in soil (Block field; + indicates presence, blank indicates absence).
    - Crop_type: Barley (seeded at 1.8 t ha-1), Ryegrass (seeded at 2.0 t ha-1), or Unvegetated.
    - Soil_texture: SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
  - Temporal context:
    - Month: Calendar month of sampling (1 = January, 2 = February, etc.).
    - Year: Year of sampling.
    - Day_of_year: Numerical day of year (1 = 1 January, 365 = 31 December).
  - Measurements:
    - Light_flux: CO2 flux rate from the mesocosm during light exposure (g CO2 m-2 h-1) measured with an IRGA; positive = net efflux, negative = net uptake.
    - Dark_flux: CO2 flux rate from the mesocosm during light exclusion (g CO2 m-2 h-1) measured with an IRGA; positive = net efflux, negative = net uptake.
    - Photosynthes: Derived photosynthetic rate within the mesocosm (g CO2 m-2 h-1), calculated as Light_flux minus Dark_flux.
  - Data conventions:
    - '.' indicates a missing sample (no data collected for that field in that record).

- Experimental design details:
  - Fully factorial arrangement with four spatial blocks to represent each treatment combination.
  - Measurements are made under two conditions (light vs. dark) to partition photosynthetic uptake from respiration and other CO2 flux processes.

- Data quality and governance considerations for monitoring frameworks:
  - Metadata and provenance:
    - Some metadata may require supplementation from dataset originators; ensure clear documentation of data sources and measurement methods (IRGA, units, timing).
  - Data quality steps:
    - Ensure QA/QC processes to clean and transform data, verify unit consistency (g CO2 m-2 h-1), and maintain versioned datasets.
  - data accessibility:
    - Public sharing of underlying data may be constrained; plan governance to balance openness with confidentiality or rights considerations.
  - Data interoperability:
    - Standardize variable definitions and units to enable integration with other environmental health indicators and dashboards.

- Relevance for monitoring and decision-making:
  - The dataset provides empirical measures of carbon flux under varying agricultural practices (biochar presence, crop type) and soil textures, enabling assessment of environmental health impacts and informing policy decisions related to soil amendments and crop management.
  - Output products (reports, charts, dashboards) can convey net ecosystem exchange and photosynthesis dynamics across treatments and time.