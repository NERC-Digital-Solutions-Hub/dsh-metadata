# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC Topsoil physico-chemical data 2018/2019

- Background: Countryside Survey is a national audit of UK countryside resources, conducted since 1978, with a rolling program starting in 2019 to monitor soil and vegetation changes over time. The project is part of UK-SCAPE and aims to quantify direction and magnitude of soil change and interactions with multiple pressures.
- Purpose for GIS: Provides map-ready, multi-parameter topsoil data and environmental classifications suitable for spatial analysis, trending, and policy-relevant visualization.

## Design and sampling framework

- Rolling survey design: 5-year cycle, 500 1-km x 1-km squares per cycle; 100 squares surveyed annually to balance spatial coverage and year-on-year monitoring.
- Stratification: Squares selected within Land Classification (LC07) strata; excludes squares with >75% urban land or >90% sea.
- Spatial scope: Data cover Great Britain (England, Scotland, Wales); includes country and environmental zone annotations.
- Sampling unit inside each square: up to five sampling locations (PLOTs) aligned with vegetation X-Plots; soil cores collected at 0–15 cm depth.

## Sample collection and field methods

- Topsoil sampling: five 15 cm cores per square/location, co-located with vegetation surveys; cores collected with standardized black plastic core.
- Relocation and consistency: historical plot markers and relocation procedures used (198 mines, 1990 markers; 1998/2007 resampling; 2019 relocations near plot centers); post-collection samples sent to UKCEH laboratories.
- Processing: samples refrigerated, transported to UKCEH Soil Bank; standard field manuals referenced for general methods.

## Metrics, laboratory protocols and analytics

- Core metrics (measured on fine earth or bulk soil): pH (in deionized water), LOI (Loss-on-Ignition) for soil organic matter and carbon estimates, bulk density, gravimetric moisture content (MOISTURE, MOISTURE_DRY), Olsen phosphorus (PO4_OLSEN) for arable/improved grassland, total nitrogen (N_PERCENT, N_STOCK).
- Calculations and units:
  - LOI-derived carbon: C_CONC_LOI (g C per kg soil), C_STOCK_LOI (t C per ha).
  - Stock calculations rely on soil depth (0–15 cm), bulk density, core volume, and area conversions.
  - Soil carbon stocks and nitrogen stocks expressed per hectare; LOI conversions use 0.55 multiplier for carbon after LOI.
- Land classification and environmental zones:
  - LC07: ITE Land Classification (2007) with numeric codes (LC07_NUM) to support habitat- or vegetation-class based analyses.
  - EZ_DESC_07: Countryside Survey Environmental Zones derived from environmental data and LC07 classes.
- Data structure for the dataset:
  - Columns include SQUARE (1-km square ID), PLOT (plot number within square), YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, N_PERCENT, N_STOCK, PO4_OLSEN, BULK_DENSITY, MOISTURE, MOISTURE_DRY, LC07, LC07_NUM, COUNTRY, EZ_DESC_07, SOIL_GROUP.
  - SOIL_GROUP categories based on LOI (e.g., Mineral, Humus mineral, Organo-mineral, Organic).
  - Data are reported in consistent SI units with defined conversion factors.

## Data quality assurance and QA workflow

- Robust QA framework: rolling survey requires continuous data checking; QA workflows implemented by UKCEH laboratory staff and data scientists.
- Quality controls:
  - pH: internal standards included; duplicates ~10%; readings accepted if within ±2 SD of batch mean.
  - LOI: internal standards and calcite checks; duplicate checks every 25 samples; batch-level QC applied.
  - Olsen-P and N analyses: standardized reference materials, blanks, and calibration corrections applied; instrument checks with known standards.
- Documentation and reproducibility: QA metadata and analysis procedures documented; data processing workflows implemented in R.

## Data structure and data use for GIS

- Dataset characteristics:
  - 18 columns, 562 rows; missing samples denoted by -9999.
- Spatial context for GIS applications:
  - 1-km square grid across GB; each square contains up to five sampling locations tied to vegetation plots.
  - Country codes (ENG, SCO, WAL) and environmental zone classifications (EZ_DESC_07) enable regional mapping.
  - LC07 land classification and EZs facilitate stratified spatial analyses of soil properties across environmental gradients.
- Derived and core metrics suitable for maps:
  - Topsoil pH, LOI-derived carbon metrics (C_CONC_LOI, C_STOCK_LOI), nitrogen stocks (N_STOCK), Olsen phosphorus (PO4_OLSEN), bulk density (BULK_DENSITY), and moisture metrics (MOISTURE, MOISTURE_DRY).
  - SOIL_GROUP categories provide rapid soil health/organic matter context for thematic mapping.
- Data availability and references:
  - UKCEH Soil Bank referenced as a repository for soil data; project documentation and methods available via Countryside Survey resources and UKCEH publications.

## Practical implications for GIS specialists

- Use 1-km resolution data to create national and regional soil condition maps, trends, and change detection over rolling 5-year cycles.
- Combine soil metrics with environmental zones and land classifications to explore how soil condition relates to environmental gradients and land use.
- Leverage the QA-rich metadata (units, methods, QC checks) to ensure metadata-driven provenance and reproducibility of map products.
- Consider integrating with vegetation data (accompanying datasets) to analyze soil-vegetation interactions over time.

## References and further reading

- Emmett et al. methods and soil manuals; Countryside Survey Soils reports (2007, 2010s) and rolling program documentation.
- UKCEH Environmental Zones and ITE Land Classification (LC07) documentation.
- Soil Bank data availability and associated QA metadata.
- Key journals and reports cited for background on soil carbon, nitrogen, and analytical methods.