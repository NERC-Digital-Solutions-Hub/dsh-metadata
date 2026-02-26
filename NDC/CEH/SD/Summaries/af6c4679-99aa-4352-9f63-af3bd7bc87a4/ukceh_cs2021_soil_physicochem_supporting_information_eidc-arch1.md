# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

- Overview
  - A national, rolling survey of UK soil health, started in 2019 to monitor topsoil condition and its drivers over time.
  - Aims to quantify the direction and magnitude of soil change and how multiple pressures interact to affect soil condition and function.
  - Supports policy-relevant insights on soil carbon, pH, nutrients, and soil structure across Great Britain, with co-located vegetation data.

- Survey design and rolling program
  - Uses a rolling design: 500 x 1-km squares sampled over each 5-year cycle, with about 100 squares visited per year.
  - Squares are stratified within Land Classification (ITE LC07) based on climate, relief, geology, etc.
  - Urban (>75%) or sea-dominated (>90%) squares are excluded.
  - The program buffers against extreme climate years and enables year-to-year and long-term detection of spatial and temporal changes.

- Covid disruption 2020
  - Fieldwork delayed in early 2020; later sampling occurred in July–August with 50 England-only squares reselection to complete coverage.

- Sample collection methods
  - In each 1-km square, topsoil samples are taken from five pre-determined random locations near vegetation X-Plots.
  - Core depth is 0-15 cm (topsoil); five cores per square are collected and combined for analysis if possible.
  - Location references have evolved over years (e.g., 1978 baseline, 1990 markers, 1998/2007 resampling distances, 2019 plot relocation to the western corner).
  - Samples are refrigerated, shipped to UKCEH labs, and stored in the UKCEH Soil Bank.

- Metrics, laboratory protocols and analytical methods
  - Field methods and lab workflows are described in the Soils Manual; samples analyzed for soils and stored as needed.
  - Land Classification and Environmental Zones provide context for interpretation across GB.
  - Soil metrics measured (0-15 cm FE where applicable) include:
    - Soil pH (in deionised water)
    - Loss on Ignition (LOI) and derived soil carbon content (C_CONC_LOI) and C stock (C_STOCK_LOI)
    - Nitrogen content and stock (N_PERCENT, N_STOCK)
    - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils
    - Bulk density (BULK_DENSITY)
    - Gravimetric moisture content (MOISTURE, MOISTURE_DRY)
  - Soil groups are categorized by LOI into Mineral, Humus mineral, Organo-mineral, and Organic.
  - Carbon stocks and nitrogen stocks are calculated for fine earth (0-15 cm) using standard conversions.
  - Unit conversions and core volume calculations are provided to enable stock estimates.

- Data quality assurance
  - QA/QA procedures are embedded in a robust data workflow using R scripts and guidance documents.
  - Internal standards, duplicates, blanks, and calibration checks are used in laboratory analyses to ensure accuracy.
  - Data are subjected to regular QA checks during collection, processing, and integration into the UKCEH data systems.

- Details of data structure (Topsoil data 2021)
  - The dataset contains 18 columns and 496 rows; missing samples are denoted by -9999.
  - Key fields and descriptions:
    - SQUARE (text): 1-km survey square identifier
    - PLOT (number): Plot number for soil sampling location (X-Plot)
    - YEAR (number): Year of soil sampling
    - PH (number): Soil pH in water, field-moist bulk soil (B)
    - LOI (number): LOI, expressed as g LOI per 100 g of oven-dried soil, or percent
    - C_CONC_LOI (derived): Soil carbon concentration per kg of oven-dry soil (g C/kg)
    - C_STOCK_LOI (derived): Soil carbon stock per hectare (t C/ha)
    - SOIL_GROUP (category): UKCEH-Countryside Survey carbon group
    - BULK_DENSITY (number): Dry bulk density (g/cm3) of fine earth (0-15 cm)
    - MOISTURE (number): Gravimetric water content (g water per g field-moist soil)
    - MOISTURE_DRY (number): Gravimetric water content for oven-dry soil
    - N_PERCENT (number): Total nitrogen (% N per 100 g oven-dry soil)
    - N_STOCK (derived): Total nitrogen stock per hectare (t N/ha)
    - PO4_OLSEN (number): Olsen phosphorus (mg/kg) for arable/improved grassland only
    - LC07 (text): ITE Land Classification (2007) description
    - LC07_NUM (number): LC07 numeric code
    - COUNTRY (category): England, Scotland, or Wales
    - EZ_DESC_07 (category): Countryside Survey Environmental Zone description
  - Data sources and code references
    - Measurements follow standardized UKCEH methods and are designed to enable cross-year comparisons and national/sub-national reporting.
    - The dataset is associated with broader Countryside Survey environmental zones and land classifications to support stratified analyses.

- Data availability and usage notes
  - Data are part of UKCEH Soil Bank and Countryside Survey outputs; QA metadata and analysis reports accompany the dataset.
  - The rolling design supports ongoing monitoring of soil condition, carbon stocks, nutrient status, and soil physical properties across GB.
  - The dataset is intended for researchers and decision-makers seeking statistically robust patterns and changes in soil condition over time and space.

- References and further reading
  - Methods and QA procedures align with the Countryside Survey Soils Manual and related CEH/NERC documentation.
  - Related publications provide context on soil carbon, nitrogen dynamics, and long-term soil change across GB.