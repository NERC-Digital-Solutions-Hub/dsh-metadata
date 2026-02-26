# Pot_number  Unique identifier for each individual mesocosm Block       Presence of 2 % biochar (w/w) in soil; + indicates presence, indicates absence Crop_type   Crop treatment consisting of Barley (Hordeum vulgare L.) seeded at 1.8 t ha-1, Ryegrass (Lolium perenne) seeded at 2.0 t ha-1, or Unvegetated treatment Soil_textureSoil texture treatment consisting of SC (sandy clay), SZL (sandy silt loam) or CL (clay loam) Month       Calendar month of sampling (1 = January, 2 = February…) Year        Year of sampling Day_of_year Numerical day of year when sample was taken (1 = 1 January, 2 = 2 January... 365 = 31 December) Block       Spatial block of mesocosm within the enclosure (in the fullyfactorial experiment, one replicate of each treatment combination was represented in each of four spatial blocks) Light_flux  CO2 flux rate from mesocosm during light exposure (g CO2 m-2 h-1) measured using an IRGA, with positive value indicating net efflux and negative value indicating net uptake by the system Dark_flux   CO2 flux rate from mesocosm during light exclusion (g CO2 m-2 h-1) measured using an IRGA, with positive value indicating net efflux and negative value indicating net uptake by the system PhotosynthesPhotosynthetic rate within the mesocosm (g CO2 m-2 h-1), derived by subtracting dark_flux value from light_flux value
note: '.' = 'period' indicates no sample taken. 

- Dataset purpose and scope
  - Captures CO2 flux and photosynthesis measurements in a mesocosm experiment across different crop treatments, soil textures, and biochar presence.
  - Temporal coverage includes month, year, and day of year to enable time-series analysis.

- Key variables and measurements
  - Identifiers and experimental design
    - Pot_number: unique id for each mesocosm
    - Block: spatial block within the enclosure (4 blocks in the fully factorial design)
    - Biochar presence: indicator for 2% biochar in soil
    - Crop_type: Barley, Ryegrass, or Unvegetated
    - Soil_texture: SC, SZL, or CL
  - Temporal context
    - Month, Year, Day_of_year
  - Gas exchange measurements
    - Light_flux: CO2 flux during light exposure (g CO2 m-2 h-1); positive = net efflux, negative = net uptake
    - Dark_flux: CO2 flux during darkness (g CO2 m-2 h-1); same interpretation
    - Photosynthes: derived as Light_flux minus Dark_flux (g CO2 m-2 h-1)

- Data quality notes
  - A dot ('.') indicates a sample not taken, important for handling missing data during analysis.

- Practical uses for data support
  - Build self-serve dashboards and reports to compare CO2 flux and photosynthesis across Crop_type, Soil_texture, and Biochar treatments over time.
  - Create summarized views by month/year or by block, and produce visuals to communicate environmental effects of treatments.
  - Ensure appropriate data cleaning, unit consistency, and explicit handling of missing samples as indicated by the '.' marker.