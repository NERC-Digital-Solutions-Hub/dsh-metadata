# Countryside Survey: Soils 2019

- Purpose and context
  - Nationwide soil monitoring under UK-SCAPE; aims to quantify direction and magnitude of soil change across Great Britain and how multiple pressures interact.
  - Rolling, five-year survey cycle (first cycle 2019) to provide data and maps of stock and change in GB soils, with co-located vegetation assessments.
  - Data support policy-relevant insights into soil health, carbon dynamics, nutrient status, and responses to land management and atmospheric deposition.

- Sampling design and coverage
  - 500 x 1 km squares selected per five-year cycle, randomly within strata defined by the Land Classification of Great Britain; 100 squares visited annually.
  - Exclusions: any square with >75% urban land or >90% sea excluded.
  - Historical sampling continuity: includes 1978, 1998, and 2007 squares to enable long-term comparability.
  - Rolling design buffers against climate-year extremes and optimizes national coverage.

- Field sampling and data collection
  - Within each annual 100 x 1 km square:
    - Soil samples collected from 5 randomly dispersed locations using a 15 cm C-core (0–15 cm depth) alongside vegetation X-Plots.
    - Samplings relocated using previously mapped plots and markers; methods updated across survey years, with 2019 plotting adjusted to the western corner.
    - Samples refrigerated and shipped to UKCEH Bangor laboratories within days.
  - Vegetation data collected in parallel (data in accompanying vegetation dataset).

- Metrics, laboratory protocols, and methods
  - Soil carbon and organic matter
    - Loss on ignition (LOI) to classify soil carbon groups; depth profiling of organic horizons (F, H, and peaty horizons) to identify peat status.
    - Depth of organic top horizons measured with an avalanche probe.
  - Soil chemical properties
    - pH in deionised water (DIW) and in CaCl2; EC in DIW.
    - Olsen-P (phosphorus) and total phosphorus (TP) via standard digestion and colorimetric analysis.
    - Total soil organic carbon (SOC) and total nitrogen (TN) using CEH-standard elemental analysis after inorganic carbon removal.
  - Soil physical properties
    - Bulk density, stones, porosity; particle density derived from LOI and assumed densities; porosity = 1 − (BD / ρ_soil).
    - Gravimetric and volumetric water content; derived soil water content metrics.
  - Peat and carbon stock calculations
    - Carbon concentration derived from LOI with 0.55 factor (consistent with legacy CS data) and alternative conversions per Ruehlmann et al. for cross-study compatibility.
    - SOC stocks computed per hectare using bulk density, depth, and carbon concentration.
  - Quality control
    - Internal standards, duplicate samples (~10%), blanks; calibration standards and moisture corrections; CaCO3 recovery checks (95–100% target).
    - QC references run with batches to ensure accuracy (pH, LOI, CaCO3, Olsen-P, TP).

- Data structure and availability
  - Primary dataset: UKCEHCS_SOIL_METRICS_2019.csv with fields for square ID, plot ID, land classification, habitat descriptors, depth and horizon metrics, soil carbon groups, pH, EC, moisture, LOI, CaCO3, Olsen-P, total P, SOC, TN, and derived ratios (e.g., CN_RATIO_FE).
  - Units and derived measures documented (e.g., g C per 100 g soil, mg/kg P, t C/ha stocks).
  - Data tables align with long-running Countryside Survey methodologies; vegetation metrics available in a separate data set.

- Outputs and interpretation
  - Annual analyses feed a rolling time series of soil change (back to 1978) using standardized methods (Scott 2008; Reynolds et al. 2013).
  - UKCEH Countryside Survey 2019 summary figures illustrate relationships and distributions, including:
    - LOI vs porosity and bulk density relationships
    - pH (water) vs LOI and pH (CaCl2) vs LOI
    - EC vs LOI; calcite vs LOI
    - LOI vs gravimetric and volumetric water content; histograms for LOI and pH
  - Outputs support national and sub-national indicators of soil condition and inform assessments of pressures on soil health.

- Key questions addressed (through the rolling program)
  - How do multiple pressures interact to alter soil and vegetation condition and function?
  - How is the topsoil carbon pool changing under varying pressures?
  - Are carbon-to-nitrogen ratios shifting across habitats?
  - Is soil pH changing in response to atmospheric deposition or land management?
  - Is there evidence of increased soil compaction or phosphorus availability shifts with management changes?
  - How does vegetation change influence soil condition and function?

- Challenges and opportunities for Analysts
  - Increasing the value of datasets by integrating CS soil data with other environmental datasets to enable broader analyses beyond single-use outputs.
  - Providing access to underlying data to support broader reuse and policy evaluation.
  - Ensuring standardized methods and rolling-cycle design continue to deliver robust, comparable indicators over time.

- References and supporting material
  - Methodological foundations and prior CS reports (e.g., Emmett et al. 2010; Scott 2008; Reynolds et al. 2013) and related soil science literature.
  - Data and documentation available through CEH/UKCEH channels and the Countryside Survey portals.