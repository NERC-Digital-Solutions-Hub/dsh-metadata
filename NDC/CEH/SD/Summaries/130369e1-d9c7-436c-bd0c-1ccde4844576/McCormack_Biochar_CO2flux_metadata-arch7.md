# Mesocosm CO2 Flux Measurements Data Dictionary

- Purpose
  - Provides a structured set of variables describing mesocosm experiments and associated CO2 flux measurements, enabling map-based visualization and spatial analysis of treatment effects and flux dynamics.

- Key variables and descriptions
  - Pot_number: Unique identifier for each individual mesocosm.
  - Biochar (implied by text): Presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence.
  - Crop_type: Crop treatment categories — Barley (Hordeum vulgare L.) seeded at 1.8 t ha-1, Ryegrass (Lolium perenne) seeded at 2.0 t ha-1, or Unvegetated.
  - Soil_texture: Soil texture categories — SC (sandy clay), SZL (sandy silt loam), or CL (clay loam).
  - Month: Calendar month of sampling (1 = January, 2 = February, …).
  - Year: Year of sampling.
  - Day_of_year: Day of year when the sample was taken (1 = 1 January, up to 365/366).
  - Block (spatial block): Spatial block of a mesocosm within the enclosure; in a fully factorial design, one replicate of each treatment combination is represented in each of four spatial blocks.
  - Light_flux: CO2 flux rate from the mesocosm during light exposure (g CO2 m-2 h-1); positive = net efflux, negative = net uptake.
  - Dark_flux: CO2 flux rate from the mesocosm during light exclusion (g CO2 m-2 h-1); positive = net efflux, negative = net uptake.
  - Photosynthes: Photosynthetic rate within the mesocosm (g CO2 m-2 h-1); derived as Light_flux minus Dark_flux.
  - Note on data completeness: A value of '.' indicates no sample was taken for that measurement.

- Data characteristics relevant to GIS work
  - Temporal context: Month, Year, Day_of_year allow time-based mapping and time-series visualization.
  - Spatial structure: Block provides a clear spatial subdivision within the enclosure, enabling mapping of treatment effects across blocks.
  - Derived metric: Photosynthes (derived from Light_flux and Dark_flux) can be used for summarized flux analyses in map-based dashboards.
  - Measurement units: Fluxes in g CO2 m-2 h-1; ensure unit consistency when integrating with other spatial data layers.

- Practical considerations for use
  - Missing data: Handle '.' entries as missing values during geospatial analysis and visualization.
  - Treatment replication: Fully factorial design with four spatial blocks; map analyses can incorporate block-level effects.
  - Data integration: Combine with crop, soil texture, and biochar indicators to explore spatial patterns of CO2 flux across treatments.