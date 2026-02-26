# Dataset Description (Soil_Properties_FRC)

## Scope and Purpose
- Describes soil properties across organic and mineral soil in unlogged tropical forest, logged tropical forest, and oil palm plantations in Sabah, Malaysia.
- Collected March–April 2015; measurements conducted at Forest Research Centre, Sabah.
- Part of the NERC-funded BALI project.
- Designed to support standardised environmental monitoring and policy performance assessment over time.

## Study Design and Sites
- 9 one-hectare plots across 3 sites representing forest types: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified sampling: each 1 ha plot subdivided into 25 subplots (20 m × 20 m); 5 subplots sampled per plot.
- Within each sampled subplot: 5 samples collected using a gouge augur; organic layer depth measured; horizons separated into organic and mineral soil.
- Samples pooled by horizon and land-use type:
  - 20 organic and 20 mineral soil samples per forest type (unlogged and logged).
  - 5 organic and 5 mineral soil samples for oil palm.

## Sampling and Laboratory Processing
- pH measured on fresh soils in a 2.5:1 water suspension.
- Total Carbon (C) and Total Nitrogen (N) measured with an Elementar vario MAX CN analyser.
- Total Phosphorus (P) extracted using a sulphuric-nitric-perchloric acid digest; concentration measured spectrophotometrically at 880 nm.
- Inorganic Phosphorus extracted with Bray No. 1 solution; measured spectrophotometrically at 880 nm.
- Sand, Silt, and Clay determined by the pipette method.

## Data Structure and Metadata
- File: Soil_Properties.csv with 15 columns:
  - Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_pH, Total_C, Total_N, Total_P, inorganic_P, C:N, Sand, Silt, Clay.
- Metadata field descriptions:
  - Identifier: Unique sample ID (text).
  - Site: Geographical site (text).
  - Land_Use: Unlogged tropical forest, Logged tropical forest, or Oil Palm (text).
  - Plot_Name: Name of the 1 ha plot (text).
  - Subplot: Subplot number within each plot (numeric).
  - Horizon: Soil horizon sampled (text).
  - Soil_pH: pH value (numeric).
  - Total_C/N/P and inorganic_P: content values with corresponding units (numeric; C in % or numeric as specified, N in %, P in µg/g or numeric as specified).
  - C:N: Carbon-to-nitrogen ratio (numeric).
  - Sand/Silt/Clay: particle size fractions (numeric; units as described).
- Units and formats provided for each numeric column; explicit land-use categories documented.

## Data Quality, Provenance, and Standards
- Data collected following established soil-analytical methods and referenced protocols.
- Metadata aligns with standard environmental monitoring practices to enable data verification and reuse.
- Part of a broader monitoring effort and designed to be stored and uploaded to appropriate data portals for accessibility.

## References and Methods Context
- Allen, S.E. 1989; Anderson & Ingram 1993; Bray & Kurtz 1945; Landon 1984; Riutta et al. 2018 (logging disturbance effects on net primary productivity).
- Sampling and analysis reflect these standardized methods and prior scientific frameworks.

## Applications for Monitoring and Policy Performance
- Enables cross-site comparison of soil properties among unlogged, logged, and oil palm landscapes.
- Supports monitoring of soil fertility, carbon, and nutrient dynamics over time.
- Provides structured data and documentation suitable for integration with other datasets to enhance evidence-based environmental monitoring and policy assessment.

## Practical Considerations for Analysts
- The dataset is designed for standardised outputs (maps, charts, reports) and straightforward incorporation into monitoring portals.
- There is an emphasis on increasing the value of the dataset by linking with complementary data sources and ensuring underlying data accessibility for downstream analysis.