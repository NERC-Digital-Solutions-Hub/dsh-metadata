# Countryside Survey

- A long-running UK study (since 1978) auditing natural countryside resources to detect changes over time by comparing with previous surveys.
- The 2019–onward surveys operate under a rolling program funded by NERC/UK-SCAPE to monitor soil condition and function at national scales.

## Purpose and scope for data leaders

- Transform legacy Countryside Survey data into a rolling, scalable dataset focused on soil condition and vegetation change, enabling analysis of direction and magnitude of change and interactions with multiple pressures.
- Data are collected to support policy relevance and international research, with emphasis on national and sub-national indicators across GB and its countries.

## Rolling program design and sampling

- Rolling survey: repeats every five years or after 500 squares completed; 100 squares visited per year to balance spatial coverage and annual monitoring.
- Sampling units: 500 x 1km squares within strata defined by the Land Classification of Great Britain; 1978 squares retained for long-term repeat sampling.
- Exclusions: squares with urban >75% or sea >90% excluded.
- 2020 Covid disruption: fieldwork delayed; 50 England-only squares added due to access constraints.

## Sample collection and site layout

- Within each 1km square (49 sub-squares used for soil sampling in many years), soils are sampled from 5 randomly dispersed locations coincident with vegetation plots.
- Soil core: 15 cm long, taken from top 0–15 cm, using a black C-core; vegetation X-Plots used for site context.
- Location history: sampling points have historical markers and mapped coordinates to aid future relocation.

## Soil and vegetation metrics (scope of data)

- Core soil metrics include: soil organic matter (loss on ignition, LOI), soil pH (in deionised water and CaCl2), soil solution electrical conductivity (EC), hygroscopic water, CaCO3, soil carbon concentration, bulk density, porosity, stones volume, gravimetric and volumetric water content, Olsen-P (for arable/improved grassland), total phosphorus (TP), total soil organic carbon (SOC) and total nitrogen (TN), and CN ratio.
- Soil carbon groups and depths: soils categorized by LOI-derived groups (mineral, humus mineral, organo-mineral, organic soils) and peaty horizons depth to classify peat presence.
- Derived calculations: carbon concentration (%C) derived from LOI via regression (0.5453*LOI + 0.4366); carbon stocks per hectare calculated from SOC/LOI with bulk density and depth factors; porosity and densities computed using LOI fractions and assumed densities (organic matter 1.4 g/cm3, mineral 2.7 g/cm3).
- Vegetation data: summarized in an accompanying vegetation data set (not detailed here).

## Laboratory protocols and data processing

- Field methods documented in an accompanying field manual; laboratory analyses performed at UKCEH laboratories.
- Key procedures include:
  - LOI and hygroscopic water via thermogravimetric analysis (TGA) with stepwise heating.
  - pH in DIW and CaCl2 suspensions; strict quality control using internal standards and duplicates.
  - EC measurement from soil slurry, with QA checks.
  - Carbon and nitrogen analyses using CEH-standard SOP (elemental analysis) after removal of inorganic carbon.
  - Olsen-P measurements using 0.5 M NaHCO3 extraction and colorimetric analysis; QA with references and blanks.
  - Total phosphorus measured by H2O2/H2SO4 digestion followed by colorimetric analysis; QA with standards and blanks.
  - Bulk density, porosity, stones, and related metrics calculated from core data; QA ensured via training and fixed-volume sampling sleeves.
- Data units and conversions are defined to maintain compatibility with legacy Countryside Survey data (e.g., 0.55 LOI ≈ %C, with explicit regression-based conversion used here).

## Data structure and metadata

- Core data fields include:
  - SQ_ID (1km survey square identifier), PLOT_ID (X-plot), YEAR, LC07 (ITE Land Classification), broad habitat descriptors, average peat horizon depth, LOI groupings, pH, EC, CaCO3, Olsen-P, TP, SOC, TN, CN ratio, bulk density, porosity, mass/stones/volume of stones, water contents (gravimetric and volumetric), and carbon-related derived metrics (gC/100g soil, gC/kg, tC/ha).
- Data are organized with explicit derived fields for stock calculations and soil carbon density per hectare, enabling stock-change analyses.
- Sample condition: -9999 denotes missing sample.

## Quality control and data integrity

- Rigorous QA across chemical and physical measurements:
  - Internal standards in each batch; duplicates and blanks; calibration checks.
  - Acceptable pH and LOI/CACO3 recoveries within defined tolerances; moisture corrections applied where needed.
  - For Olsen-P and TP: calibration ranges, blanks, and reference samples included; results moisture-corrected.
- Procedures emphasize traceability, repeatability, and compatibility with historical CS data.

## Analysis approach and temporal context

- Annual analyses contribute to a rolling time-series dataset spanning back to 1978.
- Output includes time-series figures for soil organic matter (LOI) and soil pH in water, illustrating long-term trends.
- 2020 data release includes a set of summary figures exploring relationships among porosity, LOI, bulk density, pH, EC, calcite, and water content, as part of ongoing data exploration and quality assessment.

## Data stewardship, accessibility, and references

- Data are managed under UKCEH/CEH frameworks, with rolling program sampling design and data analysis coordinated by CEH/Known staff.
- Data are linked to a broader Countryside Survey ecosystem, with vegetation metrics available in related data sets.
- Central references and methodological documents include historical CS reports, field manuals, land-class classifications, and related peer-reviewed work, underscoring data lineage and methodological continuity.

## Practical takeaways for Data Leaders

- The Countryside Survey provides a robust, long-running national soil dataset built on a well-documented rolling design, enabling timely detection of spatial-temporal soil changes and interactions with multiple pressures.
- Key data governance elements:
  - Rolling sampling design with explicit spatial stratification and annual site visitation targets.
  - Comprehensive metadata and derived fields to support stock assessments and policy-relevant analyses.
  - Rigorous QA/QC protocols and standardized conversions to align with legacy CS data.
  - Clear data structure that supports aggregation at national/sub-national levels and cross-year comparisons.
- Considerations for future data strategy:
  - Maintain linkage between soil and vegetation data through integrated data pipelines.
  - Ensure transparent documentation of sampling adjustments (e.g., Covid-era changes) and their effects on time-series.
  - Continue publishing annual time-series visuals and maintain accessibility to both raw and derived metrics for policy and research use.