# Dataset Description (Soil_Properties_FRC)

- Describes soil properties from organic and mineral soil across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Sampling period: March–April 2015; measurements conducted at Forest Research Centre, Sabah, Malaysia.
- Part of the NERC-funded BALI project.

- Content and variables
  - Data file: Soil_Properties.csv with 15 columns: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_pH, Total_C, Total_N, Total_P, inorganic_P, C:N, Sand, Silt, Clay.
  - Metadata for each column includes description and units/formats (e.g., Soil_pH numeric, Total_C %/numeric, Total_P µg/g, Sand/Silt/Clay %).

- Sampling design
  - 9 one-hectare plots across 3 sites representing unlogged forest (DVCA), logged forest (MBCA), and oil palm (SAFE).
  - Stratified sampling: each 1 Ha plot subdivided into 25 subplots (20 x 20 m); 5 subplots randomly sampled per plot.
  - From each subplot: 5 samples collected with a gouge augur; organic layer depth measured; horizons separated and sealed.
  - Sampling yields: 20 organic and 20 mineral soil samples per forest type (Unlogged and Logged); 5 organic and 5 mineral per oil palm.
  - Measurements:
    - pH on fresh soils in a 2.5:1 water suspension.
    - Total C and N with an elementar vario max CN analyser.
    - Total P via sulfuric-nitric-perchloric acid digest; inorganic P via Bray No. 1 extract.
    - Concentrations measured spectrophotometrically at 880 nm.
    - Sand, silt, and clay determined by the pipette method.

- Data structure and key fields
  - Identifier: unique sample ID (text).
  - Site: geographic area/site (text).
  - Land_Use: Unlogged tropical forest, Logged tropical forest, or Oil Palm (text).
  - Plot_Name: name of the 1 Ha plot (text).
  - Subplot: subplot number within the plot (numeric).
  - Horizon: soil horizon sampled (text).
  - Soil_pH: pH value (numeric).
  - Total_C, Total_N, Total_P: soil nutrient contents (Total_C and Total_N as %; Total_P as µg/g).
  - inorganic_P: inorganic phosphorus content (µg/g).
  - C:N: carbon-to-nitrogen ratio (numeric).
  - Sand, Silt, Clay: texture components (Sand and Silt as %; Clay as %).

- Reuse considerations and methodology references
  - Methods and references for analyses include: Landon (1984) for pH in soil suspensions; Allen (1989) for total C and N analysis; Bray & Kurtz (1945) for total P extraction; Anderson & Ingram (1993) for tropical soil methods.
  - Riutta et al. (2018) provides context on logging disturbance and productivity, relevant for comparative analyses across land-use types.

- Source and provenance
  - Data collected as part of the NERC-funded BALI project, with sampling conducted in 2015 and analyses conducted at the Forest Research Centre, Sabah, Malaysia.