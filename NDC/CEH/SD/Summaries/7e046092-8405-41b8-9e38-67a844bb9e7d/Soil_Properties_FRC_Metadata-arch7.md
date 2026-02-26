# Dataset Description (Soil_Properties_FRC)

## Overview
- Dataset describing soil properties from organic and mineral soil across unlogged tropical forest, logged tropical forest, and oil palm plantations in Sabah, Malaysia.
- Sampling occurred in March–April 2015 at Forest Research Centre, Sabah; part of the NERC-funded BALI project.
- Data stored in Soil_Properties.csv with 15 columns capturing site, land use, plot, horizon, and soil chemistry.

## Data file and structure
- Soil_Properties.csv includes 15 columns: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_pH, Total_C, Total_N, Total_P, inorganic_P, C:N, Sand, Silt, Clay.
- Metadata provides descriptions, units, and formats for each field (e.g., Soil_pH numeric; Total_C and Total_N in %; Total_P and inorganic_P in µg/g; C:N numeric; Sand/Silt/Clay in %).

## Sampling design
- 9 one-hectare plots across 3 sites representing forest types: unlogged tropical forest, logged tropical forest, and oil palm (Davan Valley Conservation Area, Maliau Basin Conservation Area, SAFE project in Sabah).
- Stratified sampling: each 1 Ha plot divided into 25 subplots of 20 x 20 m; 5 subplots sampled per plot.
- From each sampled subplot, 5 soil samples were collected using a gouge auger; organic layer depth measured; horizons (organic and mineral) separated and pooled.
- Pooling yields:
  - For unlogged and logged forest: 20 organic + 20 mineral soil samples per forest type.
  - For oil palm: 5 organic + 5 mineral soil samples.

## Measurements and methods
- pH measured on a fresh soil-water suspension (ratio 2.5:1).
- Total Carbon (Total_C) and Total Nitrogen (Total_N) measured with an elemental analyzer (CN analysis).
- Total Phosphorus (Total_P) determined via sulfuric-nitric-perchloric acid digest; concentration read on a spectrophotometer at 880 nm.
- Inorganic Phosphorus (inorganic_P) extracted with Bray No. 1 solution; concentration in µg/g.
- Particle size (Sand, Silt, Clay) determined using the pipette method.

## Variables and units (metadata details)
- Identifier: Unique sample identifier (text).
- Site: Geographical site (text).
- Land_Use: Forest type or land use (text: Unlogged tropical forest, Logged tropical forest, Oil Palm).
- Plot_Name: Name of the 1 Ha plot (text).
- Subplot: Subplot number within each plot (numeric).
- Horizon: Soil horizon sampled (text).
- Soil_pH: pH of soil sample (numeric).
- Total_C: Total carbon content (numeric; %).
- Total_N: Total nitrogen content (numeric; %).
- Total_P: Total phosphorus content (numeric; µg/g).
- inorganic_P: Inorganic phosphorus content (numeric; µg/g).
- C:N: Carbon-to-nitrogen ratio (numeric).
- Sand: Sand content (numeric; %).
- Silt: Silt content (numeric; %).
- Clay: Clay content (numeric; %).

## GIS relevance and usage
- The dataset provides plot-level and horizon-level soil properties that can be mapped across Sabah’s forest types.
- Suitable for creating spatially informed soil maps, comparing soil chemistry among land uses, and integrating with other GIS layers (plots, sites, forest type).
- Be mindful that pooling during sampling reduces within-plot variability; dataset is structured for comparative analyses across forest types rather than high-resolution, per-subplot variability.

## Metadata and provenance
- Data collected as part of the BALI project; aligns with methodological references for soil analysis (Allen 1989; Anderson & Ingram 1993; Bray & Kurtz 1945; Landon 1984).
- Sampling design, measurement protocols, and cited references provided to support reproducibility and integration with GIS analyses.

## References
- Allen, S.E. 1989. Chemical Analysis of Ecological Materials.
- Anderson, J.M. & Ingram, J.S.I. 1993. Tropical soil biology and fertility – A handbook of methods.
- Bray, R.H. & Kurtz, L.T. 1945. Determination of total organic and available forms of phosphorus in soils.
- Landon, J.R. 1984. Booker Tropical Soil Manual.
- Riutta, T. et al. 2018. Logging disturbance shifts net primary productivity in Bornean tropical forests. Global Change Biology.