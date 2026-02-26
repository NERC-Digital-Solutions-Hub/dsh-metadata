# UKCEH Countryside Survey: Soils Metrics 2019

- Purpose and scope
  - Countryside Survey (CS) is a long-running audit of UK countryside resources; the 2019 survey marks the start of a rolling monitoring program (UKCEH-CS) to track soil condition and function at national to sub-national scales.
  - Aims to quantify direction and magnitude of soil changes and how multiple pressures interact, with outputs including data and maps of stock and change in GB soils.
  - Rolling program selects 1 km squares across GB, enabling year-on-year monitoring and longer-term change detection.

- Sampling design and geographic coverage
  - 500 x 1 km squares sampled over a five-year cycle; 100 squares visited each year.
  - Squares selected within strata defined by the Land Classification of Great Britain; historic CS squares from 1978, plus 1998 and 2007 cohorts, are included to maximize change detection.
  - Exclusions: any square with >75% urban land or >90% sea; distribution mapped at 10 km resolution for confidentiality.
  - Within each annual square, 5 predetermined, randomly dispersed soil sampling locations plus vegetation X-Plots are used for coordinated multi-metric assessment.

- Field sampling and laboratory methods
  - Within each annual 1 km square: five soil cores collected from the top 0–15 cm at five Main X-Plots locations using a 15 cm C-core; cores are refrigerated and sent to UKCEH labs.
  - Soil horizon assessment includes FHO horizons and peaty depth determinations to classify soils (mineral, organo-mineral, organic, and peat categories).
  - Key lab metrics include:
    - pH in deionised water and in CaCl2; electrical conductivity (EC).
    - Hygroscopic water content, Loss on Ignition (LOI), CaCO3; soil carbon concentration derived from LOI.
    - Bulk density, porosity, mass stones, and volume stones.
    - Olsen-P (phosphorus) and Total P; soil organic carbon (SOC) and total nitrogen (TN); CN ratio.
    - Gravimetric and volumetric water content; carbon stock calculations (SOC t/ha) using depth assumptions and bulk density.
  - Measurement specifics:
    - LOI and CaCO3 analyzed with thermogravimetric analysis (TGA) on ~10 g sub-samples; LOI conversion to %C follows established CS methods (0.55 × LOI or regression-based, as per legacy workflows).
    - SOC and TN measured using elemental analyser after removing inorganic carbon; QA includes in-house references and standard checks.

- Data structure and contents
  - Main data file: UKCEHCS_SOIL_METRICS_2019.csv; missing sample values denoted by -9999.
  - Core fields include:
    - SQ_ID (1 km square ID), PLOT_ID (X-plot number), YEAR, LC07 (ITE Land Classification), EZ_DESC (Environmental Zone), BROAD_HABITAT, and related descriptors.
    - Physical and chemical soil metrics: average depth of peaty horizon, soil carbon groups, pH_DIW, pH_CaCl2, EC, Hygroscopic moisture, LOI, CaCO3, C_conc_LOI_gC_per_100g_soil, C_conc_LOI_gC_per_kg, SOC_stock (t C/ha), bulk density, porosity, mass and volume of stones, VWC (volumetric water content), GWC (gravimetric water content), Olsen-P, Total P, Total C, Total N, CN ratio, and related derived fields.
  - Derived calculations and units are standardized to align with CS legacy datasets (e.g., 0.15 m representative depth for cores, area of 1 ha equals 10,000 m2, bulk density to convert %C to C per unit area).

- Quality control and data quality
  - pH and LOI QA: internal standards in every batch; acceptance within ±2 SD of batch mean; duplicates ~10% of samples.
  - Olsen-P and Total P QA: blanks, reference materials, and duplicates with specified QC frequency (every ~25 samples); moisture-corrected results and calibration-based reporting.
  - CaCO3 recovery targets 95–100%; samples retested if outside range.
  - Overall QA integrates multiple internal standards, duplicates, and calibration checks to ensure consistency across years and sites.

- Analysis, time-series and outputs
  - Annual analyses contribute to a rolling time-series (since 1978 CS baseline) to monitor soil organic matter (LOI) and soil pH trajectories.
  - UKCEH Countryside Survey 2019 provides figures and summaries illustrating relationships among soil properties (e.g., LOI vs. porosity, LOI vs. bulk density, LOI vs. pH, LOI vs. EC, LOI vs calcite) and distributions (histograms for LOI, pH, bulk density).
  - Outputs are designed to support spatial analysis and visualization across GB, including site-level and aggregated trends by habitat and land-class categories.

- GIS-specific considerations and usage
  - Spatial resolution: 1 km grid with annual sampling of 100 squares; national-scale mapping and sub-national stratification by land classification.
  - Data can be joined with land classification, environmental zones, and vegetation data to map soil condition, change over time, and habitat-specific patterns.
  - Confidentiality: spatial plots displayed at broader scales (e.g., 10 km) for map outputs; raw site-level locations are aggregated to respect confidentiality.
  - Suitable for GIS tasks such as:
    - Creating national and regional soil condition maps (e.g., LOI, SOC, pH, P stocks) across 2019 and subsequent years.
    - Analyzing relationships between soil properties and land classes, habitats, or vegetation types.
    - Time-series analyses to identify trends and responses to pressures (e.g., land management, deposition, climate fluctuations).
  - Data limitations to consider in GIS:
    - 1 km square sampling means within-square heterogeneity may be smoothed; ensure temporal and spatial aggregation matches policy questions.
    - Exclusion criteria (urban/sea) and confidentiality constraints in map products.

- References and data provenance
  - Core methodological references include Emmett et al. (2010), Reynolds et al. (2013), Scott (2008), Bunce et al. (2007), and related Countryside Survey documentation.
  - Vegetation metrics are in accompanying datasets; sample design and rolling program are described in the UKCEH-CS framework and 2019 field methods.

- Additional notes for practitioners
  - The dataset supports integrated soil condition assessments within a national monitoring framework, enabling policy-relevant spatial analysis and evidence-based soil management decisions.
  - For reproducibility and cross-year comparisons, adhere to the CS-derived definitions for soil groups, horizons, and unit conversions as outlined in the data structure and quality control sections.