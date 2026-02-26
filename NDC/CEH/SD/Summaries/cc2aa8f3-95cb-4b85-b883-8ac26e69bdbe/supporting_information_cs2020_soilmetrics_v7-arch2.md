# UKCEH Countryside Survey data 2020 Summary Figures

## Purpose and context
- Countryside Survey is a long-running UK audit of natural resources, with a rolling monitoring program since 2019 to detect direction and magnitude of soil change and how multiple pressures interact.
- Focuses on soil condition and function at national and sub-national scales, enabling comparisons over time with standardized methods.
- Outputs include data, maps, and figures to support policy and environmental health scrutiny.

## Design and sampling framework
- Rolling five-year cycle; 500 x 1km squares sampled across GB, with 100 squares visited per year.
- Squares are stratified by the Land Classification of Great Britain; 75% urban or 90% sea exclusions apply.
- In 2019–2020, sampling described for 49 x 1km sample squares (within-cycle representation), each visited with five soil samples and accompanying vegetation plots.
- The design aims to capture both spatial variation and temporal change, buffering against extreme climate years.

## 2020 Covid disruption
- Survey activity limited in May–June 2020; resumed in July–August.
- 2020 reallocation led to reselection of 50 squares from England only due to access limitations.

## Sample collection methods
- In each 1km square, 49 sample squares logistical setup is described, with soil samples collected from five randomly dispersed locations using a 15 cm C-core at top 0–15 cm, coincident with vegetation X-Plots.
- Soil cores collected during visits, then refrigerated and shipped to the UK Centre for Ecology & Hydrology ( Bangor ) for laboratory analysis.
- Historical relocation markers (1978, 1990, 1998, 2007) informed relocation and sampling practices; 2019 sampling moved to different plot corners within the central Main Plot.

## Metrics, laboratory protocols and analytical methods
- Field methods are documented in the accompanying field manual.
- Land classification: ITE Land Class 2007 used for stratification; broad vegetation metrics available in the accompanying vegetation data set.
- Soil carbon groups (LOI-based) categorize soils as Mineral, Humus mineral, Organo-mineral, Organic soils, with peaty horizon depth helping distinguish peat soils.
- Depth of peaty organic layers (average FH or peaty O horizon depth) used to classify soil type; measurements taken with an avalanche probe.
- Soil pH: measured in deionised water (DIW) and in CaCl2 (0.01 M) with a 1:2.5 soil-to-solution ratio; quality control using internal standards and duplicates.
- Electrical conductivity (EC): measured from a 10 g soil sample suspended in 25 mL DIW; QC with internal standards and duplicates.
- Loss on Ignition (LOI) and derived carbon: LOI measured via thermogravimetric analysis (TGA) from approximately 10 g sub-samples; hygroscopic water, LOI, and CaCO3 determined across multiple temperature steps (105°C, 375°C, 650°C, 1000°C). Carbon concentration derived from LOI using a regression (C = 0.5453*LOI + 0.4366) to yield gC per 100 g soil; additional conversions provide gC/kg and tC/ha.
- Quality control for LOI and CaCO3 includes internal standards, calcite recovery checks (95–100%), and batch repeats if QC criteria are not met.
- Bulk density, stones, and porosity: calculated from core mass and volumes; stone content measured; porosity derived from bulk and particle densities (assumed 2.7 g/cm3 for mineral and 1.4 g/cm3 for organic matter fractions).
- Water content: volumetric and gravimetric water contents computed from bulk density and measured gravimetric water content.
- Olsen phosphorus: 2 g soil extracted with 0.5 M NaHCO3 (pH 8.5); analysis via flow-injection with colorimetric molybdate-antimony reagent; QC with blanks, duplicates, and reference samples; reliable mainly for arable/improved grassland sites.
- Total phosphorus (TP): H2O2/H2SO4 digestion followed by colorimetric analysis for TP; moisture-corrected results reported in mg/kg.
- Soil organic carbon (SOC) and total nitrogen (TN): after inorganic carbon removal, SOC and TN measured using an Elementar Vario EL elemental analyzer; ball-milled samples dried at 105°C; QC with in-house references and standard compounds.
- Quality control across chemical analyses includes multiple internal standards, blanks, duplicates, and reference materials.

## Data structure and variables
- Data records include fields such as SQ_ID (1 km square ID), PLOT_ID (X-plot), YEAR, LAND CLASS descriptors, habitat classifications, and a comprehensive set of soil metrics.
- Key derived variables include:
  - Soil carbon concentration from LOI (gC/100 g soil and gC/kg)
  - SOC and TN (% by dry soil)
  - Bulk density, porosity, mass/volume of stones
  - LOI group classifications and depth-related peat indicators
  - pH_DIW and pH_CaCl2, EC
  - Olsen-P and total P
- Data records permit missing values denoted by -9999 and include detailed metadata for units and calculation methods.

## Annual analysis and outputs
- Data contribute to a rolling “soil change” analysis back to the 1978 baseline, focusing onLOI (soil organic matter) and soil pH in water, with methods described in Scott (2008) and Reynolds et al. (2013).
- UKCEH Countryside Survey 2020 Summary Figures include:
  - Relationships between porosity and LOI (and LOI vs porosity on log scales)
  - Relationships between bulk density and LOI
  - Relationships between pH (water and CaCl2) and LOI
  - Relationships between EC and LOI
  - Relationships between Calcite and LOI
  - LOI versus gravimetric and volumetric water content
  - Histograms of LOI fractions and pH (water)
- Figures are intended to illustrate patterns across different habitat/soil depth categories (e.g., non-peat, shallow peats, deep peats).

## Implications for monitoring and data reuse
- The rolling design and standardized methods enable consistent, long-term monitoring of soil condition and function across the UK.
- Emphasis on data quality control and comparability with legacy Countryside Survey data (since 1978) supports robust stock-and-change analyses.
- The data are structured to support accessibility and reuse, with clear pathways for data deposition, archiving, and cross-linking to vegetation and environmental datasets.

## References and further reading
- Core methodological references and data papers are cited throughout, guiding interpretation of LOI, SOC, P, pH, and other soil metrics, and detailing historical sampling and resampling protocols.