# Countryside Survey: Soils Data 2019

## Purpose and scope
- National rolling survey of GB soils to track direction and magnitude of soil change under multiple pressures.
- Provides data and maps of soil stock and change; aims to fill critical gaps in national-scale soil status and dynamics.
- Supports understanding of soil health for food security, public health, and climate understanding.
- Focuses on soil condition and its interaction with vegetation, with emphasis on carbon pools, pH, nutrient status, and physical properties.

## Design: rolling program and sampling frame
- Rolling survey adopted in 2019 to repeat every five years or after 500 1km squares, prioritizing nationwide coverage and year-on-year monitoring.
- 500 x 1km squares sampled across a Land Classification of GB; 100 squares visited per year.
- Exclusions: any square with >75% urban land or >90% sea excluded.
- Sample selection builds on the Countryside Survey of 1978, 1998, and 2007 squares to enable long-term change detection.
- Sampling within each active square includes five predetermined soil core locations co-located with vegetation plots.

## Sampling methods and field procedures
- Within each annual 100 x 1km square, five randomly dispersed soil samples collected using a 15 cm C-core from the top 0–15 cm, in conjunction with vegetation X-Plots.
- Historical sampling locations adjusted across survey years (1978, 1990, 1998, 2007, 2019) with relocation markers to enable re-sampling.
- Samples chilled and shipped to UKCEH Bangor laboratories for analysis.
- Vegetation data are collected in parallel (available in accompanying vegetation data set).

## Metrics, laboratory protocols and analytical methods
- Field stratification: ITE Land Classification 2007 used to stratify and report changes by vegetation class/habitat.
- Soil carbon groups (UKCEH-CS): mineral, humus mineral, organo-mineral, organic soils based on Loss on Ignition (LOI).
- Depth of organic layers: measured to identify peaty horizons; classification into mineral, organo-mineral, organic, and peaty topsoil categories.
- Key soil metrics and analyses:
  - pH: in deionised water (DIW) and CaCl2; quality controlled with internal standards.
  - Electrical conductivity (EC) of soil slurry.
  - LOI and related components (hygroscopic water, CaCO3, soil organic carbon derived from LOI).
  - Soil carbon concentration and soil organic carbon (SOC) measurement via elemental analysis after removing inorganic carbon.
  - Bulk density, porosity, particle density, and stones content; derived soil density metrics for carbon stock calculations.
  - Fine-earth gravimetric and volumetric water content; derived volumetric water content and soil moisture relationships.
  - Olsen phosphorus (P Olsen) and total phosphorus (TP) via colorimetric methods and acid digestion, respectively.
  - Total soil organic carbon (SOC) and total nitrogen (TN) via elemental analyser (post inorganic carbon removal).
- Quality control practices include internal standards, repeated batches, duplicates, blanks, and moisture corrections.

## Data structure and dataset details
- Core dataset: UKCEHCS_SOIL_METRICS_2019.csv
- Key fields include:
  - SQ_ID (1km square identifier), PLOT_ID, YEAR, LC07 (Land Classification), habitat descriptors, depth of organic horizon, LOI groupings, soil carbon group classifications, pH (DIW and CaCl2), EC, moisture metrics, LOI, CaCO3, carbon concentrations, SOC stocks (tC/ha), bulk density, porosity, mass of stones, volume of stones, gravimetric and volumetric water contents, Olsen-P, total P, total C and nitrogen, CN ratio, and derived carbon fractions.
- Data are designed for rolling time-series analyses across survey years.

## Annual analysis and outputs
- The dataset contributes to a rolling time-series understanding of soil change since the first Countryside Survey in 1978.
- Outputs include summary figures (e.g., LOI and soil pH time series) and visualization of relationships among soil properties (porosity, bulk density, pH, LOI, etc.) across habitat types.
- Figures highlight relationships such as LOI vs. porosity, LOI vs. bulk density, pH vs. LOI, EC vs. LOI, calcite vs. LOI, and moisture relationships.

## Key research questions addressed
- How do multiple pressures interact to alter soil and vegetation condition and function?
- How is the topsoil carbon pool changing under various pressures?
- Are carbon-to-nitrogen ratios changing across habitats?
- Is soil pH changing in response to atmospheric deposition or land-management practices?
- Is there evidence of increased soil compaction or changes in phosphorus availability due to management?
- How does vegetation change (driven by land use or deposition) feedback on soil condition and function?

## Governance, team and data quality
- UKCEH staff and field survey teams oversee data collection, processing, lab analyses, archiving, and rolling-program design.
- Emphasis on standardized protocols, traceability, calibration, and rigorous QA/QC across all analyses.
- Data management includes detailed documentation, standardized classifications, and alignment with legacy CS datasets for comparability.

## Relevance for data leaders
- Demonstrates a robust, multi-scale data system integrating soil measurements with vegetation context, enabling both local and national insights.
- Rolling, repeat-sampling design improves resilience to climate variability and supports long-term trend detection.
- Comprehensive metadata and QC processes enhance data discoverability, reliability, and interoperability with legacy datasets.
- Provides a model for coordinating cross-disciplinary data collection (soil, vegetation) and for balancing field practicality with scientific rigor.