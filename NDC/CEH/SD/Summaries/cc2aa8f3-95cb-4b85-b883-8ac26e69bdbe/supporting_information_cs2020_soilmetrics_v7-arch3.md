# UKCEH Countryside Survey data 2020 Summary Figures

## Purpose and scope
- Countryside Survey (CS) is a long-running audit of the UK countryside’s natural resources, with soil and vegetation monitoring designed to detect change over time.
- 2019 onwards, CS adopted a rolling program to provide data and maps of soil status and change, addressing questions about interactions of multiple pressures, soil carbon pools, pH shifts, compaction, phosphorus, and vegetation feedbacks.
- Goals include informing policy, monitoring environmental health, and guiding future decisions with nationally representative indicators at GB and sub-national scales.

## Monitoring design and rolling program
- Rolling survey: 500 x 1 km squares across Great Britain per 5-year cycle; 100 squares visited per year, randomised within strata defined by the Land Classification of GB.
- 1 km squares are drawn from the 1978 baseline plus later additions to maximise longitudinal change detection.
- Within each selected square, 49 x 1 km sample squares are surveyed (veg and soil data integrated where possible); in 2020, Covid disruptions led to reselection of 50 squares from England only.
- Exclusions: squares with >75% urban land or >90% sea are excluded.
- Objective: maximize site coverage and detect spatial/temporal change while buffering against extreme climate years.

## Sampling design and field methods
- Within each sample square, measurements are taken at 5 pre-determined, randomly dispersed locations (Main X-Plots) for soil sampling and vegetation surveys.
- Soil cores collected to approximately 15 cm depth using standardized C-core method; cores refrigerated and sent to UKCEH for analysis.
- Vegetation data are captured via X-Plots; accompanying vegetation dataset available separately.
- Historical sampling locations and marker placements have evolved since 1978 to support relocation and repeat sampling.

## Metrics, laboratory protocols and analytical methods
- Field manual governs methods; soil metrics include carbon, pH, conductivity, bulk density, porosity, mineral/organic fractions, and phosphorus species.
- Soil carbon and related metrics:
  - Loss on Ignition (LOI) as a primary measure of soil organic matter, with derived soil carbon concentrations.
  - Conversion from LOI to %C and to carbon stocks per hectare.
  - Soil pH measured in deionised water and in CaCl2; both with quality control standards.
  - Soil solution electrical conductivity (EC) measured from soil-water suspensions.
  - Hygroscopic water content, LOI fractions, calcite (CaCO3) content, bulk density, porosity, mass of stones, gravimetric and volumetric water contents.
  - Olsen phosphorus (P Olsen) and total phosphorus (P total) measured with standardized digestion and colorimetric methods.
  - Total soil organic carbon (SOC) and total nitrogen (TN) measured post inorganic carbon removal using an elemental analyser; quality control with in-house references and standard checks.
- Data handling and conversions:
  - Numerous derived variables (e.g., C concentration from LOI; SOC stocks per hectare; soil density and porosity calculations) with explicit formulas and assumptions.
  - Consistent data units and scaling to enable comparison with legacy Countryside Survey data (e.g., 0.55 LOI approximations aligned to earlier methods).
- Quality assurance:
  - Internal standards, blanks, duplicates (≈10% of samples), and repeat measurements when QC criteria are not met.
  - Regular instrument calibration checks and batch-level QC for LOI, CaCO3, Olsen P, and SOC/N total analyses.

## Data structure and management
- Data structure includes fields such as SQ_ID (1 km square identifier), PLOT_ID (plot within square), YEAR, LC07 land classification, habitat descriptors, depth and horizon information, and all measured and derived soil metrics.
- Data rows correspond to sample events with missing data flagged as -9999.
- The data dictionary and field descriptions provide metadata for each variable (units, definitions, and calculation methods).
- Data management team and rolling-program governance are described, emphasizing archiving, traceability, and data accessibility.

## Annual analysis and outputs
- Analyses contribute to a rolling time series from 1978 onward, focusing on soil organic matter (LOI) and soil pH in water over time.
- Figures and summary outputs (e.g., UKCEH Countryside Survey data 2020 Summary Figures) illustrate relationships among soil properties:
  - LOI vs porosity
  - LOI vs bulk density
  - pH (water and CaCl2) vs LOI
  - EC vs LOI
  - Calcite vs LOI
  - LOI vs gravimetric and volumetric water contents
- The dataset underpins national and sub-national indicators, and supports cross-wave comparisons with prior CS reports (1978–2007).

## Covid disruption and adaptation
- 2020 field season impacted by Covid-19; surveys could not be conducted in early 2020, but partial fieldwork occurred later in the year.
- Resulted in reselection of a subset of squares, with England-only adjustments to ensure continued coverage and data viability.

## Policy relevance and governance implications
- Rolling monitoring framework provides timely, spatially explicit data on soil condition and function, enabling assessment of multiple pressures and land-management effects.
- Emphasizes the importance of data quality, metadata, open data sharing where possible, and transparent governance to support evidence-based policy decisions.
- The methodology supports future decision-making by identifying sample design, measurement standardization, and data pipelines suitable for dashboards, reports, and policy-facing outputs.

## References and further reading
- Core methodologies and reporting from Countryside Survey through 1978–2007, 2007 soils reports, and CEH-led analyses.
- Key supporting documentation includes Land Classification (ITE), LOI to carbon conversions, soil horizon descriptions, and QC practices.
- Foundational papers on soil carbon, nitrogen, and deposition effects, plus data management and rolling program design (Scott 2008; Reynolds et al. 2013; Ruehlmann 2020; Emmett et al. 2010).