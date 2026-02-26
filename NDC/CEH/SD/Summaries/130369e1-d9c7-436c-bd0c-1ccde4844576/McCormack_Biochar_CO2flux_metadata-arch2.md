# Mesocosm CO2 Flux Dataset: Metadata and Measurements

## Purpose and Scope
- Records CO2 flux and photosynthesis in mesocosms under varying biochar presence, crop type, and soil texture.
- Includes temporal metadata (Month, Year, Day_of_year) and spatial metadata (Block within enclosure).
- Intended to support monitoring environmental processes and policy-relevant analyses over time.

## Key Variables (Fields)
- Pot_number: Unique identifier for each individual mesocosm.
- Block: Spatial block of mesocosm within the enclosure; in the fully factorial design, one replicate of each treatment in each of four spatial blocks.
- Biochar: Presence of 2% biochar (w/w) in soil; + indicates presence, - indicates absence.
- Crop_type: Crop treatment (Barley seeded at 1.8 t ha-1, Ryegrass seeded at 2.0 t ha-1, or Unvegetated).
- Soil_texture: Soil texture treatment (SC = sandy clay, SZL = sandy silt loam, or CL = clay loam).
- Month: Calendar month of sampling (1 = January, etc.).
- Year: Year of sampling.
- Day_of_year: Day of year when the sample was taken (1–365).
- Light_flux: CO2 flux rate during light exposure (g CO2 m-2 h-1); measured with IRGA; positive = net efflux, negative = net uptake.
- Dark_flux: CO2 flux rate during light exclusion (g CO2 m-2 h-1); positive = net efflux, negative = net uptake.
- Photosynthes: Photosynthetic rate within the mesocosm (g CO2 m-2 h-1), derived by subtracting Dark_flux from Light_flux.
- Note: "." indicates no sample taken (period).

## Data Quality and Format
- Data are collected using standardized methods with explicit units.
- Derived metric (Photosynthes) provided to facilitate analysis.
- Metadata supports storage and sharing in appropriate data portals.

## Use Cases and Analysis
- Compare carbon flux across crop types, biochar presence, and soil textures.
- Track environmental health indicators and carbon dynamics in agroecosystems over time.
- Create clear outputs (reports, maps, charts) to communicate findings and policy relevance.

## Challenges and Opportunities
- Increase dataset value by linking with other environmental datasets (e.g., climate, soil properties).
- Improve access to underlying data, including raw infrared gas analyzer readings, to support broader reuse.