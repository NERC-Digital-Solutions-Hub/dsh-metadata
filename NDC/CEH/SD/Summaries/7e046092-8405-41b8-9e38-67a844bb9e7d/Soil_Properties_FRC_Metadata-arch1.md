# Dataset Description (Soil_Properties_FRC)

- Purpose: Describes soil properties across organic and mineral soil layers in unlogged tropical forest, logged tropical forest, and oil palm plantations in Sabah, Malaysia. Data collected March–April 2015 at Forest Research Centre, Sabah as part of the NERC-funded BALI project.

- Sampling design:
  - Nine 1-hectare plots across three sites representing forest types: unlogged tropical forest, logged tropical forest, and oil palm.
  - Sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
  - Stratified sampling: each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 5 subplots randomly sampled per plot.
  - Within each sampled subplot, 5 samples collected with gouge augur; organic layer depth measured; horizons separated into organic and mineral soil and sealed.
  - Samples pooled by subplot: yielding 20 organic and 20 mineral soil samples per forest type (unlogged and logged) and 5 organic + 5 mineral samples for oil palm.

- Measurements and laboratory methods:
  - pH measured on fresh soils in a 2.5:1 water suspension.
  - Total Carbon (Total C) and Total Nitrogen (Total N) measured with an elemental CN analyser.
  - Total Phosphorus (Total P) determined via sulphuric-nitric-perchloric acid digest; concentration read on a spectrophotometer.
  - Inorganic Phosphorus (inorganic P) extracted with Bray No. 1 solution; concentration read similarly.
  - Particle size analysis (Sand, Silt, Clay) by pipette method.
  - Data units: Soil_pH (numeric), Total_C (%), Total_N (%), Total_P (µg/g), inorganic_P (µg/g), C:N (numeric), Sand/Silt/Clay (percent).

- Variables / Metadata:
  - Identifier: Unique sample ID (text).
  - Site: Geographical site (text).
  - Land_Use: Unlogged tropical forest, Logged tropical forest, or Oil Palm (text).
  - Plot_Name: Name of the 1 Ha plot (text).
  - Subplot: Subplot number within each plot (numeric).
  - Horizon: Soil horizon sampled (text).
  - Soil_pH: pH value (numeric).
  - Total_C, Total_N, Total_P, inorganic_P: respective soil nutrient contents with specified units.
  - C:N: Carbon to nitrogen ratio (numeric).
  - Sand, Silt, Clay: texture components (percent or appropriate units).

- Context and references:
  - Part of Riutta et al. 2018 work on logging disturbance and productivity in Bornean tropical forests.
  - Key analytical references for methods: Allen (1989), Anderson & Ingram (1993), Bray & Kurtz (1945), Landon (1984).

- Practical considerations for analysts:
  - Data allow cross-comparison of organic vs mineral horizons and across land-use types (unlogged, logged, oil palm).
  - Metadata clarifies units, sampling structure, and pooling strategy, aiding reproducibility and integration with other datasets.
  - Potential limitations to consider: pooling of samples within subplots reduces within-subplot variability; specific sites are regionally focused ( Sabah, Malaysia).