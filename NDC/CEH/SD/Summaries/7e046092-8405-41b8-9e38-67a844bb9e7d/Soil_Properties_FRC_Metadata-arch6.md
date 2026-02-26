# Dataset Description (Soil_Properties_FRC)

- The dataset documents soil properties from organic and mineral soil across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Sampling occurred in March–April 2015 and was conducted at Forest Research Centre, Sabah, as part of the NERC-funded BALI project.
- Primary file: Soil_Properties.csv with 15 columns describing sample identity, location, land use, soil horizon, and measured soil properties.

## Data Content

- 15 columns: Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon, Soil_pH, Total_C, Total_N, Total_P, inorganic_P, C:N, Sand, Silt, Clay.
- Data types: mix of text (e.g., Identifier, Site, Land_Use, Plot_Name, Subplot, Horizon) and numeric measurements (e.g., Soil_pH, Total_C, Total_N, Total_P, inorganic_P, C:N, Sand, Silt, Clay).
- Units (where applicable) provided in metadata (e.g., Total_P in µg/g; inorganic_P in µg/g; C:N ratio; Sand/Silt/Clay percentages).

## Sampling Design and Collection

- Study design: 9 one-hectare plots across 3 sites representing three land uses (unlogged tropical forest, logged tropical forest, oil palm).
  - Sites: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), SAFE project in Sabah.
- Sampling scheme: stratified sampling within each 1-ha plot.
  - Each plot subdivided into 25 subplots (20 x 20 m); 5 subplots randomly selected for sampling.
  - 5 samples collected from each subset/subplot using a gouge augur.
  - Organic layer depth measured; horizons (organic and mineral soil) separated and sealed.
  - Pooling: five samples from each subplot pooled to yield 20 organic and 20 mineral soil samples per forest type (unlogged and logged); for oil palm, 5 organic and 5 mineral samples.
- Purpose: generate representative soil-property data across forest types and land uses for comparative analyses.

## Measurements and Laboratory Methods

- pH: measured on fresh soils in a 2.5:1 water suspension.
- Total Carbon (C) and Total Nitrogen (N): measured with an Elementar Vario MAX CN analyser.
- Total Phosphorus (P): extracted with a sulfuric-nitric-perchloric acid digest; concentration measured spectrophotometrically at 880 nm.
- Inorganic Phosphorus (inorganic_P): extracted with Bray No. 1 solution.
- Phosphorus measurements: total and inorganic P concentrations reported per sample.
- Particle-size (texture): Sand, Silt, and Clay determined using the pipette method.
- References for methods include Landon (1984), Allen (1989), Bray & Kurtz (1945), Anderson & Ingram (1993).

## Metadata and Variables

- Metadata fields provide descriptions and units for each column:
  - Identifier: Unique sample identifier (text).
  - Site: Geographical site (text).
  - Land_Use: Unlogged tropical forest, Logged tropical forest, or Oil Palm (text).
  - Plot_Name: Name of the 1-ha plot (text).
  - Subplot: Subplot number within each plot (numeric).
  - Horizon: Soil horizon sampled (text).
  - Soil_pH: pH value (numeric).
  - Total_C: Total carbon content (numeric; percent).
  - Total_N: Total nitrogen content (numeric; percent).
  - Total_P: Total phosphorus content (numeric; µg/g).
  - inorganic_P: Inorganic phosphorus content (numeric; µg/g).
  - C:N: Carbon-to-nitrogen ratio (numeric).
  - Sand: Sand content (numeric; percent).
  - Silt: Silt content (numeric; percent).
  - Clay: Clay content (numeric; percent).

## Data Structure and File Details

- File: Soil_Properties.csv containing 15 columns with data aggregated by horizon (organic and mineral) and subplot pooling as described.
- Sampling scope: 9 plots across 3 sites; multiple horizons and land-use types represented.
- Data provenance: dataset collected under the BALI project framework; references include methodological standards for soil analysis.

## Provenance and References

- Allen, S.E. 1989; Anderson, J.M. & Ingram, J.S.I. 1993; Bray, R.H. & Kurtz, L.T. 1945; Landon, J.R. 1984.
- Riutta et al. 2018: Logging disturbance shifts net primary productivity and its allocation in Bornean tropical forests (contextual reference for site selection/implications).

## Potential Data Support Opportunities

- Quality assurance and data cleaning:
  - Verify data types and handle missing values across columns.
  - Check consistency of horizon labels and pooling scheme across subplots.
  - Validate unit consistency for P measurements (µg/g) and C/N ratios.
- Metadata alignment and enrichment:
  - Ensure complete metadata for each sample (plot coordinates, horizon details, sampling dates).
  - Link to external site-level metadata or additional soil properties if available.
- Data product development:
  - Create self-serve dashboards comparing soil properties by land use and horizon (organic vs mineral) across sites.
  - Generate pivot tables and charts for pH, C, N, P, and texture (Sand/Silt/Clay) by Land_Use.
- Documentation and reproducibility:
  - Document pooling logic and subplots selection workflow for transparent reproducibility.
  - Provide data provenance notes and method references for traceability.
- Integration potential:
  - Combine with climate, vegetation, or productivity data from BALI project to explore relationships with soil properties.