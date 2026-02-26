# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC Topsoil physico-chemical data 2018/2019

## Overview and purpose
- Countryside Survey is a long-running UK audit of natural resources, conducted regularly since 1978 to detect changes over time.
- The 2019 survey marks the start of a rolling monitoring program focused on topsoil condition and vegetation, enabling comparison with earlier surveys.
- Aims include: understanding how multiple pressures interact to affect topsoil and vegetation condition and function; tracking changes in the topsoil carbon pool and soil chemistry (pH, nutrients); and informing policy and management decisions.
- The program is supported by NERC under the UK-SCAPE national capability program.

## Sampling design and rolling program
- Rolling survey: 500 1-km x 1-km squares sampled over a five-year cycle; 100 squares visited each year.
- Stratified by Land Classification (ITE LC07) to provide national and sub-national indicators; squares exclude highly urbanized or sea-dominated areas (remove >75% urban or >90% sea).
- Sampling locations within each square: up to five points (PLOTs) where soils are collected alongside vegetation surveys (X-Plots).
- Historical sampling reference: 1978 baseline squares retained; resampling occurs in subsequent cycles (1998, 2007) with relocation adjustments.
- 2019 adjustments: plots moved to the western corner of the inner 2 m x 2 m plot; relocation accuracy verified with photos, maps, and GPS data.

## Sample collection methods
- In each square, five topsoil samples are collected from 0–15 cm depth using a 15 cm core at randomly dispersed locations coincident with vegetation plots.
- Core location is tied to a central 2x2 m vegetation quadrat; prior methods used soil pits and fixed corner references for relocation.
- Collected samples are refrigerated, shipped to UKCEH laboratories, and stored in the UKCEH Soil Bank.

## Metrics, laboratory protocols and analytical methods
- General field methods are described in the Soils Manual; samples are processed or stored at UKCEH sites.
- Key measured metrics (for fine earth; 0–15 cm): 
  - pH in deionised water
  - Loss-on-Ignition (LOI) as a proxy for soil organic matter
  - Soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Bulk density (BULK_DENSITY), soil moisture (MOISTURE, MOISTURE_DRY)
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils
  - Total nitrogen (N_PERCENT) and nitrogen stock (N_STOCK)
- Calculations and units:
  - LOI derived from ThermoGravimetric Analysis (TGA) with four heating steps
  - C_CONC_LOI and C_STOCK_LOI derived from LOI and bulk density (C_STOCK_LOI in t C ha-1)
  - Stone-free fine-earth volume and soil stock calculations account for core geometry and density
  - Conversions include 0.15 m representative depth, 1 ha = 10,000 m2, bulk density in kg m-3, and conversion of g C to t C
- Quality control:
  - pH: internal standards and duplicates; acceptance within ±2 SD of batch mean
  - LOI: internal standards and calcite checks; repeat batches if standards deviate beyond 2 SD
  - PO4_OLSEN: blanks and duplicates every 25 samples
  - N: in-house reference materials; calibration checks with standard material
- Soil groups:
  - LOI-based soil groups: Mineral, Humus mineral, Organo-mineral, Organic, defined by LOI percentage ranges

## Data quality assurance
- A formal QA workflow supports rolling data collection and processing to maintain high data standards.
- Data processing uses R scripts and documented procedures to ensure consistency across surveys.
- The approach emphasizes traceability of data sources, standardized metrics, and rigorous QC at each stage.

## Data structure and metadata
- The topsoil dataset contains 18 columns and 562 rows; missing values are coded as -9999.
- Key columns and descriptors include:
  - SQUARE: 1-km square identifier
  - PLOT: soil sampling location within the square
  - YEAR: survey year
  - PH: soil pH (water, field-moist bulk soil)
  - LOI: LOI value (g LOI per 100 g soil) and LOI percentage
  - C_CONC_LOI: soil carbon concentration (g C per kg soil)
  - C_STOCK_LOI: soil carbon stock (t C per ha)
  - N_PERCENT: total soil nitrogen content (%)
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus concentration (mg kg-1)
  - BULK_DENSITY: bulk density (g cm-3)
  - MOISTURE / MOISTURE_DRY: gravimetric water content (as % and g water per g soil)
  - LC07 / LC07_NUM: ITE Land Classification (2007) identifiers
  - COUNTRY: GB country
  - EZ_DESC_07: Countryside Survey Environmental Zone descriptor
  - SOIL_GROUP: carbon/LOI-based soil group category
- Additional structure notes:
  - Land Classification and Environmental Zones link soils to environmental context for cross-tab analyses.
  - The dataset is aligned with UKCEH Soil Bank and related metadata for discoverability and reuse.

## Use cases and potential questions for analysts
- Assess how topsoil carbon stocks (C_STOCK_LOI) have changed over time across different land classes and environmental zones.
- Examine trends in soil organic matter (LOI) and pH in relation to atmospheric deposition, land management, or climate variables.
- Evaluate phosphorus and nitrogen dynamics (PO4_OLSEN, N_PERCENT, N_STOCK) and their associations with habitat types and soil groups.
- Explore the interaction of multiple pressures (e.g., deposition, land use change) on soil condition and function at national or sub-national scales.
- Integrate soil metrics with vegetation data from accompanying datasets to understand feedbacks between soil condition and vegetation change.

## References and further reading
- The dataset is part of UKCEH Countryside Survey outputs, with methodologies and QA processes described in the Countryside Survey Soils Manual and related CS technical reports.
- Related background and context include reports on soil change 1978–2007, environmental zones, land classification, and soil carbon research within the Countryside Survey program.