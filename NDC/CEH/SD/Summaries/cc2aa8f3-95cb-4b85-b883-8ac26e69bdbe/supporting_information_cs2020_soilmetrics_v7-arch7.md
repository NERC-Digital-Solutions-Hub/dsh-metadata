# UKCEH Countryside Survey data 2020 Summary Figures

- A rolling national program (Countryside Survey) to monitor soil and vegetation change across Great Britain, with 2019 marking the start of the current rolling sampling cycle.
- Objective for GIS: produce data products and map-based visuals that show stock and change in soil condition, and how multiple pressures drive spatial and temporal patterns.
- Outputs include spatial layers and time-series suitable for national and sub-national (regional) mapping and policy-informed analysis.

## Spatial design and sampling framework

- 500 x 1 km squares are randomly sampled over a five-year cycle; about 100 squares are visited each year.
- Sampling stratified by the Land Classification of Great Britain (ITE Land Class 2007); designed to enable national and sub-national indicators across GB and its countries.
- Urban (>75% urban land) or seabed (>90% sea) squares are excluded from sampling.
- In practice, soil sampling occurs within selected 1 km squares, using a set of five pre-determined locations per square, co-located with vegetation X-Plots.
- 2020 disruption due to Covid-19 led to re-selection of 50 squares in England after reduced field activity in early 2020.

## Field methods and sampling details

- Soil sampling: within each 1 km square, five cores are collected from random locations, using a black plastic C-core (15 cm long) to sample the top 0–15 cm.
- Vegetation data are collected alongside soil sampling (documented in the vegetation dataset).
- Historical site relocation and marking have evolved since 1978, with standardized coordinates and permanent markers used for future resampling.

## Metrics, laboratory protocols, and analytical methods

- Core soil metrics and related measurements (field and lab) include:
  - Soil pH (in deionised water and in CaCl2; measured with quality control checks).
  - Electrical conductivity (EC) of soil slurry.
  - Loss on Ignition (LOI) and soil organic matter proxies; derived soil carbon concentration.
  - Depth of peat horizons (peaty organic layers) and soil horizon classifications (Mineral, Humus mineral, Organo-mineral, Organic soils, Peaty topsoil, Peat).
  - Soil carbon stock calculations (SOC stocks per area; derived from LOI and bulk density).
  - Bulk density, porosity, mass of stones, and volume of stones.
  - Gravimetric and volumetric water content (GWC, VWC).
  - Calcium carbonate (CaCO3) content.
  - Olsen phosphorus (P Olsen) and total phosphorus (P total).
  - Total soil organic carbon (SOC) and total nitrogen (TN) with CN ratio.
- Derived calculations and conversions:
  - Carbon concentration (%C) from LOI using established regression (0.5453 × LOI + 0.4366).
  - SOC stocks per hectare derived from %C, LOI, bulk density, and depth.
  - Particle density and porosity calculations based on LOI and mineral fractions.
  - Depth and classification-based Groupings for soil types (Mineral, Humus mineral, Organo-mineral, Organic, Peat categories).
- Quality control (QA) procedures:
  - Internal standards and duplicate samples (about 10% of repetitions).
  - QA checks for pH, LOI, CaCO3 recoveries (95–100% for CaCO3 recovery; ±2 SD for internal standards).
  - Blanks and reference materials included in batches to monitor accuracy and precision.

## Land classification, soil groupings, and data descriptors

- Land Classification 2007 (ITE Land Class) used to stratify and interpret soil condition changes.
- UKCEH-CS soil carbon groups based on LOI-derived categories (Mineral, Humus mineral, Organo-mineral, Organic soils) and sub-groupings for horizon depth and peat depth.
- Data include both raw measurements and derived indicators (e.g., SOC stock per hectare, C:N ratios, pore fraction, bulk density, porosity).

## Data structure and availability

- Core dataset structure includes fields such as:
  - SQ_ID (1 km survey square ID)
  - PLOT_ID (X plot within the square)
  - YEAR (survey year)
  - LC07 / LC07_NUM (ITE Land Classification)
  - Habitat descriptors (BROAD_HABITAT, BROAD_HABITAT_DESC)
  - AVERAGE_O_DEPTH (peat horizon depth)
  - LOI-based soil carbon groups (SOIL_LOI_CS_GROUP, SOIL_GP_LOI_CS_1_4, etc.)
  - pH_DIW (pH in water), pH_CACL2 (pH in CaCl2)
  - EC, bulk density, porosity, mass of stones, volume of stones
  - GWC, VWC, Olsen P, total P, SOC, NTOTAL, CTOTAL, CN_RATIO_FE
  - Derived metrics: C_CONC_LOI_GCPER100G, C_CONC_LOI_GCPERKG, SOC_TC_HA, PD_GPERCM3, P_TOTAL, etc.
- Uses a missing value flag of -9999 where data are not available.
- Data are linked to annual reports and field/analysis manuals; figures illustrate time series of LOI and pH and relationships among LOI, porosity, bulk density, pH, EC, and calcite.

## Time series, analysis, and GIS-ready outputs

- Annual analysis forms a rolling time series from 1978 onward, focusing on soil organic matter (LOI) and soil pH (in water) over time.
- The 2020 UKCEH Countryside Survey data summary provides figures and relationships suitable for GIS visualization, including:
  - LOI versus porosity
  - LOI versus bulk density
  - pH versus LOI (water) and pH versus LOI (CaCl2)
  - EC versus LOI
  - Calcite versus LOI
  - LOI versus gravimetric and volumetric water content
- Data products can be mapped as:
  - Spatial layers of soil carbon stocks (t/ha) and soil carbon concentration (%C)
  - Maps of soil pH (DIW and CaCl2), EC
  - LOI-based soil carbon groups and peat depth layers
  - Olsen-P and Total-P distributions
  - Bulk density, porosity, and soil moisture indicators
- The dataset supports integration with vegetation data and other UKCEH-CS outputs for multi-layer GIS analyses.

## Covid disruption note

- 2020 field season affected by Covid-19; initial spring sampling limited, leading to reallocation of some squares (50 from England) in the latter part of the year to complete field work.

## Practical considerations for GIS specialists

- Strengths:
  - Spatially explicit 1 km square data with five soil cores per square and five soil metrics per core, enabling robust national- and sub-national-scale mapping.
  - Rich suite of soil properties, with both measured and derived indicators, suitable for stock-and-change mapping and scenario analyses.
  - Rolling five-year cycle design improves comparability across years and resilience to climate year-to-year variation.
- Considerations:
  - Sampling density is designed for national indicators; interpret maps with awareness of stratification by Land Classification and the rolling cycle.
  - Data are accompanied by field manuals, QA procedures, and references to standardized methods for reproducibility and cross-study comparisons.
  - Covid-related adjustments in 2020 may affect year-to-year comparability for certain squares; document year-specific changes when producing time-series maps.

## References and supporting materials

- Methodologies and historical context are grounded in Countryside Survey reports and technical manuals (e.g., 1978–2007 series; soils manual; rolling program design).
- Supporting literature includes Land Classification (ITE), LOI-based carbon conversions, and soil physics/chemistry references used for QA and interpretation.