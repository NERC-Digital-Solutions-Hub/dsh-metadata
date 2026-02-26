# Dataset: Mesocosm Experiment Data on Biochar, Crop Type, Soil Texture, and CO2 Flux

- Overview
  - The dataset records mesocosm-level measurements from a fully factorial experiment examining the effects of biochar presence, crop type, and soil texture on CO2 flux and photosynthesis.
  - Each row corresponds to an individual mesocosm with associated treatment and time information, plus gas exchange measurements.

- Key variables and what they capture
  - Pot_number: Unique identifier for each mesocosm.
  - Block: Spatial block within the enclosure; in the fully factorial design, one replicate of each treatment combination is represented in each of four spatial blocks.
  - Biochar presence (2% biochar w/w): Indicates whether biochar is present in the soil (presence vs absence).
  - Crop_type: Treatment type consisting of Barley, Ryegrass, or Unvegetated.
  - Soil_texture: Soil texture category (SC = sandy clay, SZL = sandy silt loam, CL = clay loam).
  - Month: Calendar month of sampling (1 = January, 2 = February, …).
  - Year: Year of sampling.
  - Day_of_year: Day of year when the sample was taken (1 = Jan 1, 365 = Dec 31).
  - Light_flux: CO2 flux rate during light exposure (g CO2 m-2 h-1); measured with IRGA; positive values indicate net efflux, negative values indicate net uptake.
  - Dark_flux: CO2 flux rate during darkness (g CO2 m-2 h-1); measured with IRGA; positive values indicate net efflux, negative values indicate net uptake.
  - Photosynthes: Derived rate of photosynthesis within the mesocosm, calculated as light_flux minus dark_flux (g CO2 m-2 h-1).

- Experimental design details
  - Fully factorial arrangement with four spatial blocks.
  - Treatments combine biochar presence/absence, crop type (Barley, Ryegrass, Unvegetated), and soil textures (SC, SZL, CL).
  - Each treatment combination is represented in each block.

- Temporal and sampling information
  - Time is captured via Month, Day_of_year, and Year, enabling temporal analyses and seasonal pattern exploration.

- Data quality and notes
  - Note: "." indicates a missing sample (no data recorded for that field on that occasion).
  - Units for flux measurements are grams of CO2 per square meter per hour (g CO2 m-2 h-1).
  - Derived metric (Photosynthes) depends on accurate measurements of Light_flux and Dark_flux.

- How this data supports analysis
  - Enables identification of correlations between biochar presence, crop type, soil texture, and CO2 flux/photosynthesis.
  - Supports predictive modeling of gas exchange based on treatment combinations and time.
  - Facilitates comparison across spatial blocks to assess experimental consistency and potential block effects.
  - Suitable for regression analyses, ANOVA-like investigations, and time-series-like explorations of seasonal patterns.

- Potential caveats for analysts
  - Missing samples (indicated by '.') reduce data density for certain combinations or time points.
  - Derived Photosynthes values depend on the accuracy of two measurements (Light_flux and Dark_flux) and their error propagation.
  - Spatial and temporal alignment of samples within blocks should be considered to avoid confounding block effects with treatment effects.