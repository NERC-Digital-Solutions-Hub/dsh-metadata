# UKCEH Countryside Survey QA metadata and analysis report 2022 - EIDC Topsoil physico-chemical data 2022

- A detailed description of topsoil (0-15 cm) physico-chemical metrics collected as part of UKCEH Countryside Survey, including sampling design, laboratory protocols, data quality assurance, and data structure for 2022.
- Supports exploration of soil condition and change across Great Britain within a rolling five-year survey framework, enabling national and sub-national comparisons and trend detection.

## Study design and sampling program

- Rolling survey introduced in 2019 to monitor soil and vegetation change with a five-year cycle; 500 1-km squares sampled per cycle, with 100 squares visited annually.
- Squares selected within strata defined by Land Classification of Great Britain; urban (>75%) or sea (>90%) squares excluded.
- Sampling aims to provide robust indicators at national/sub-national levels and capture spatial and temporal variation.
- 2020 Covid disruption reduced fieldwork; 50 English-only squares were added later to adjust the design.

## Sampling locations and collection methods

- In each 1-km square, five topsoil sampling locations are selected (co-incident with vegetation X-Plots) using a 15 cm long black plastic core from approximately 0-15 cm depth.
- Field protocol links to historical plot locations (1978 onward) with relocation markers and GPS-assisted verification; samples refrigerated and shipped to UKCEH Bangor for processing.
- Historical sampling point locations evolved (1990 markers, 1998/2007 resampling adjustments, 2019 Western corner relocation) to improve accuracy.

## Metrics, laboratory protocols and analytical methods (summary)

- Field methods are described in the Soils Manual; five cores per square are processed and stored in the UKCEH Soil Bank.
- Core-derived volumes and fine-earth fractions are used to compute carbon stocks and related metrics.
- Core data feed a suite of soil metrics measured in labs or derived from measurements on fine earth (FE).

### Key metrics and derived calculations

- pH in deionized water (PH): measured on field-moist bulk soil; QA includes internal standards and duplicates.
- Loss-on-Ignition (LOI) and derived carbon (C_CONC_LOI, C_STOCK_LOI):
  - LOI measured with a LECO TGA701 (105°C hold, then 375°C hold); LOI% and derived soil carbon concentration (g C kg-1) and carbon stock (t C ha-1) calculated with explicit conversion factors.
- Soil groups (SOIL_GROUP) based on LOI-derived categories (Mineral, Humus mineral, Organo-mineral, Organic).
- Bulk density (BULK_DENSITY): dry bulk density calculated from core mass, core volume, and stone content; essential for converting %C to C per unit volume and for C_stock calculations.
- Fine-earth moisture content:
  - MOISTURE (gravimetric water content per g of field-moist soil) and MOISTURE_DRY (per g of oven-dry soil).
- Olsen phosphorus (PO4_OLSEN): measured on arable/improved grassland soils; colorimetric determination with calibration and QA using blanks and duplicates.
- Total nitrogen (N_PERCENT, N_STOCK): measured by elemental analysis (Vario EL) on ball-milled, oven-dried samples; N_stock calculated per hectare similar to carbon stocks.
- All measurements include QA controls (internal standards, blanks, duplicates) and calibration checks.

## Data quality assurance (QA)

- A formal QA workflow developed using R-based processes to ensure data quality across rolling survey data.
- QA covers sample handling, laboratory processing, data entry, and cross-checks; internal standards and replicates used for each batch (e.g., pH, LOI, PO4, N).
- Regular calibration checks and reference materials used to maintain measurement accuracy.

## Data structure and accessibility

- Dataset consists of 18 columns and 465 rows; missing values denoted by -9999.
- Example columns:
  - SQUARE: 1-km survey square identifier (text)
  - PLOT: soil sampling location within square (number)
  - YEAR: year of sampling (number)
  - PH: soil pH in water (number)
  - LOI: LOI value (g LOI / 100 g soil; or %)
  - C_CONC_LOI: soil carbon concentration (g C per kg soil)
  - C_STOCK_LOI: carbon stock (t C per ha)
  - SOIL_GROUP: LOI-based soil carbon group category
  - BULK_DENSITY: soil bulk density (g soil per cm3)
  - MOISTURE: gravimetric water content (g water per g wet soil)
  - MOISTURE_DRY: gravimetric water content (g water per g dry soil)
  - N_PERCENT: total soil nitrogen content (%)
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07, LC07_NUM: ITE Land Classification and numeric code
  - COUNTRY: country (England, Scotland, Wales)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data structure is designed to support cross-year and cross-square analysis, including soil carbon stocks and nutrient metrics.

## Data interpretation and usage notes

- Data are intended for national and sub-national comparisons of soil health indicators (carbons, nitrogen, phosphorus) and physical properties (bulk density, moisture, LOI) across GB.
- LOI-based carbon groups provide a consistent framework for classifying soil carbon status.
- Products enable exploration of soil change over time, interactions with land class and environmental zones, and assessment of soil health in relation to vegetation and land-use changes.
- Data are suitable for integration with vegetation datasets and policy-relevant analyses within the Countryside Survey program.

## References and further reading

- Soils Manual and Countryside Survey methodological references (Emmett et al. 2008; 2010; related UKCEH and NERC publications).
- UKCEH Countryside Survey Environmental Zones, Land Classification descriptions, and related datasets.
- Contact and access details for UKCEH Countryside Survey and the Soil Bank for data access and support.