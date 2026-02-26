# Dataset Description (Soil_Properties_FRC)

## Overview
- Describes soil properties across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Data collected March–April 2015 at Forest Research Centre, Sabah as part of the NERC-funded BALI project.
- 15-variable dataset capturing chemical properties (pH, carbon, nitrogen, phosphorus) and particle size (sand, silt, clay) across soil horizons.

## Sampling design
- 9 one-hectare plots across 3 sites representing land-use types: unlogged forest, logged forest, and oil palm.
- Sites include Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified design: each 1 Ha plot subdivided into 25 subplots (20 m x 20 m); 5 subplots sampled per plot.
- 5 samples per subplot collected using gouge augur; organic layer depth measured; organic and mineral horizons separated and sealed.
- Within each subplot, 5 samples pooled to yield:
  - 20 organic and 20 mineral soil samples per forest type (unlogged and logged)
  - 5 organic and 5 mineral soil samples from oil palm
- pH measured in fresh soils (2.5:1 water suspension); Total C and N via CN analyser; Total P via acid digest; inorganic P via Bray No. 1; concentrations measured with spectrophotometer; texture by pipette method.

## Measurements and columns
- 15 columns in Soil_Properties.csv:
  - Identifier (Unique Sample Identifier)
  - Site (Geographical area/site)
  - Land_Use (Unlogged tropical forest, Logged tropical forest, or Oil Palm)
  - Plot_Name (1 Ha plot name)
  - Subplot (Subplot number within plot)
  - Horizon (Soil horizon sampled)
  - Soil_pH (Measured pH)
  - Total_C (Total carbon content; %)
  - Total_N (Total nitrogen content; %)
  - Total_P (Total phosphorus content; µg/g)
  - inorganic_P (Inorganic phosphorus content; µg/g)
  - C:N (Carbon to nitrogen ratio)
  - Sand (Sand content; %)
  - Silt (Silt content; %)
  - Clay (Clay content; %)

## Metadata details
- Each field includes:
  - Description (textual explanation)
  - Unit/format (Text or numeric, with specified units)
- Ensures consistent interpretation and facilitates data integration with other datasets.

## Data provenance and references
- Collected under the NERC-funded BALI project.
- Key references:
  - Allen, S.E. 1989. Chemical Analysis of Ecological Materials
  - Anderson, J.M. & Ingram, J.S.I. 1993. Tropical soil biology and fertility
  - Bray, R.H. & Kurtz, L.T. 1945. Determination of phosphorus in soils
  - Landon, J.R. 1984. Booker Tropical Soil Manual
  - Riutta et al. 2018. Logging disturbance and net primary productivity (Global Change Biology)

## Relevance for monitoring frameworks
- Provides a robust, well-documented data source for soil health and forest management monitoring.
- Clear sampling design and standardized measurement methods support comparability across studies.
- Comprehensive metadata aids data governance, quality assurance, and data sharing considerations.

## Data quality and governance considerations
- Metadata is explicit, improving data verifiability and reuse.
- Data collection methods and laboratory analyses are specified, supporting quality control.
- Potential governance considerations include data accessibility (openness), consistent data formats, and ongoing data maintenance, in line with typical monitoring framework challenges.