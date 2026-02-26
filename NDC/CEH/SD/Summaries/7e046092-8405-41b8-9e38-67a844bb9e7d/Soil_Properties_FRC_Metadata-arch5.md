# Dataset Description (Soil_Properties_FRC)

## Overview
- Describes soil properties from organic and mineral layers across unlogged tropical forest, logged tropical forest, and oil palm plantation in Sabah, Malaysia.
- Data collected March–April 2015 at Forest Research Centre, Sabah, as part of the NERC-funded BALI project.
- Contains a single dataset file, Soil_Properties.csv, with 15 measured variables.

## Dataset contents
- 15 columns in Soil_Properties.csv:
  - Identifier: Unique sample identifier (Text)
  - Site: Geographical site (Text)
  - Land_Use: Forest type (Unlogged, Logged, Oil Palm) (Text)
  - Plot_Name: Name of the 1 ha plot (Text)
  - Subplot: Subplot number within each plot (Numeric)
  - Horizon: Soil horizon sampled (Text)
  - Soil_pH: Measured soil pH (Numeric)
  - Total_C: Total carbon content (Numeric; percent)
  - Total_N: Total nitrogen content (Numeric; percent)
  - Total_P: Total phosphorus content (Numeric; µg/g)
  - inorganic_P: Inorganic phosphorus content (Numeric; µg/g)
  - C:N: Carbon to nitrogen ratio (Numeric)
  - Sand: Sand content (Numeric; percent)
  - Silt: Silt content (Numeric; percent)
  - Clay: Clay content (Numeric; percent)

## Sampling design and data collection
- 9 one-hectare plots across 3 sites representing forest types: Danum Valley Conservation Area (DVCA), Maliau Basin Conservation Area (MBCA), and SAFE project in Sabah.
- Stratified design: each plot subdivided into 25 subplots (20 m x 20 m); 5 subplots sampled per plot.
- 5 samples collected from each sampled subplot using gouge auger.
- Organic layer depth measured; horizons separated and sealed; 5 samples per subplot pooled to yield:
  - 20 organic and 20 mineral soil samples per forest type (Unlogged and Logged)
  - 5 organic and 5 mineral samples from oil palm
- Measurements:
  - pH in a 2.5:1 water suspension
  - Total C and N using an Elementar Vario MAX CN analyser
  - Total P via sulfuric-nitric-perchloric acid digest
  - Inorganic P via Bray No. 1 extraction
  - Concentrations measured with a spectrophotometer at 880 nm
  - Sand, Silt, and Clay by the pipette method
- Sampling window and location: March–April 2015, Forest Research Centre, Sabah, Malaysia.

## Metadata and provenance
- Identifier and Site provide traceable sample identity and origin.
- Land_Use documents forest type; Plot_Name and Subplot capture spatial context.
- Horizon records the soil layer sampled; Soil_pH and soil nutrient metrics describe chemical properties.
- Metadata references and data provenance align with methods and sources cited in the document.

## References and methods context
- Methods and analyses follow established soil science protocols:
  - Allen, 1989; Landon, 1984; Bray & Kurtz, 1945; Anderson & Ingram, 1993
- Riutta et al. 2018 provides context for regional forest disturbance effects (DK) and project background.

## Governance and stewardship considerations for Data Stewards
- Data quality and standardization
  - Ensure consistent units across all numeric columns (e.g., C, N in percent; P in µg/g; pH dimensionless).
  - Verify Horizon and Land_Use categorizations align with metadata definitions.
  - Maintain clear documentation of pooling design (how many samples combined per subplot and per forest type).
- Metadata completeness and discoverability
  - Preserve unique identifiers and clearly link Site, Plot_Name, Subplot, and Horizon to enable discovery and reuse.
  - Provide or maintain a metadata table with field descriptions, units, and acceptable value ranges.
- Provenance and reproducibility
  - Include project context (NERC BALI), sampling window, and site details to support data reuse and replication of analyses.
  - Reference measurement methods and instruments used (CN analyser, spectrophotometer, digestion method, pipette method).
- Data access, sharing, and updates
  - Ensure dataset is stored in an appropriate data portal or repository with versioning.
  - Document any data updates, corrections, or reprocessing steps; clearly indicate any limitations or uncertainties (e.g., pooling effect on individual sample resolution).
- Interoperability and future integration
  - Consider adopting standard schemas for soil property datasets to facilitate integration with other collections (consistent field naming, units, and ontologies).

## Notes on limitations and scope
- The dataset represents a specific temporal window (Mar–Apr 2015) and sites in Sabah, Malaysia; interpretation should consider potential temporal and spatial variability.
- Pooling of sub-samples prior to analysis reduces per-sample resolution but increases representativeness for plot-level estimates.