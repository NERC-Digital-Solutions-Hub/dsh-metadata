# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

## Purpose and scope
- National rolling soil-monitoring study focusing on topsoil condition and function, linked to vegetation assessments.
- Aims to quantify direction and magnitude of soil change across Great Britain and interpret interactions with multiple pressures (e.g., carbon pools, pH, compaction, phosphorus, vegetation feedback).
- Part of UKCEH-CS rolling program initiated in 2019 to provide data and maps of stock and change in GB soils (0–15 cm).

## Survey design and rolling program
- Rolling survey: repeats on a five-year cycle or after 500 squares completed; first cycle began in 2019.
- Sampling frame: 500 x 1-km squares per cycle, with 100 squares visited annually; stratified by Land Classification (ITE LC07) to capture environmental gradients.
- Exclusions: squares with >75% urban land or >90% sea excluded.
- Historical context: builds on 1978, 1998, and 2007 survey squares to enable long-term change detection.
- 2020 Covid disruption: partial year, second half surveys conducted; 50 England-only squares reselected.

## 2021 topsoil winter survey sampling
- Subset sampling: 30 (+5 reserve) squares from the 2021 rolling set selected for winter survey to reflect environmental zones.
- Hierarchical selection: prioritised squares surveyed in 1978, 1998, and 2007; included squares surveyed in 1978 and others ordered by land class and time of year.
- Sampling within squares: five randomly dispersed locations per square, using pre-defined X-Plots; topsoil (0–15 cm) collected with 15 cm cores at vegetation plot corners.
- Data recorded: for winter survey, only Broad Habitat was recorded.

## Sample collection and field methods
- Within each square: five soil samples collected from co-located vegetation plots; cores stored refrigerated and shipped to UKCEH laboratories.
- Legacy sampling details: location markers and plot re-relocation protocols maintained across survey years to aid future relocation and comparability.

## Metrics, laboratory protocols and analytical methods
- Core measurements and lab processing: five soil samples per location; processed or stored in UKCEH laboratories; soil data logged in lab systems and stored in the UKCEH Soil Bank.
- Key soil metrics and derived data products:
  - pH: measured in deionised water on field-moist bulk soil.
  - LOI (Loss on Ignition): used to estimate soil organic matter and carbon content via ThermoGravimetric Analysis (LECO TGA701) from 25°C to 1000°C in four steps.
  - Carbon concentration (C_CONC_LOI) and carbon stocks (C_STOCK_LOI) derived from LOI and bulk density, enabling carbon stock estimates per hectare.
  - Soil organic matter and LOI-based soil carbon grouping (SOIL_GROUP) based on LOI categories.
  - Bulk density (BULK_DENSITY): calculated from 15 cm cores, accounting for stones.
  - Moisture content (MOISTURE_DRY): gravimetric water content (dry basis) and related metrics.
  - Total nitrogen (N_PERCENT, N_STOCK): measured by elemental analysis (Vario-EL) after 105°C drying; stock calculated per hectare.
  - Olsen phosphorus (PO4_OLSEN): not measured in the 2021 winter survey; included in broader series for compatibility.
- Units and conversions: explicit definitions for core depth, area, bulk density, and carbon stock calculations.
- Quality control: routine use of internal standards, duplicates (about 10%), and batch checks for pH, LOI, and N analyses; QA steps ensure measurements meet historical variability expectations.

## Data quality assurance (QA) workflow
- End-to-end QA pipeline designed for rolling surveys to ensure high data standards:
  - Lab data QA: labs perform initial QA, flag anomalies, verify measurement standards, and document changes.
  - Analyst data QA1: cross-check lab data against measurement records; document queries and changes.
  - Calculation of derived soil metrics: via dedicated R scripts (calculate_soil_derived_metrics_function.R and Derive soil data.R) to ensure reproducibility and auditable calculations; integrate related habitat/vegetation metrics for QA.
  - Analyst data QA2: automated HTML QA report evaluating patterns, expected relationships, and consistency with prior data; collaboration with labs to resolve outstanding queries.
- Change tracking: all dataset updates are logged against the corresponding QA step to maintain transparency and auditability.

## Data structure and availability
- Dataset structure: 18 columns and 576 rows; missing samples denoted by -9999.
- 2021 winter survey specifics: PO4_OLSEN not measured for this dataset but reported for compatibility within the data series.
- Key dataset fields:
  - SQUARE: 1-km square identifier
  - PLOT: plot number within square
  - YEAR: survey year
  - PH: soil pH (in water)
  - LOI: soil organic matter content (g LOI per 100 g soil)
  - C_CONC_LOI: soil carbon concentration (g C per kg oven-dry soil)
  - C_STOCK_LOI: carbon stock density (t C per ha)
  - SOIL_GROUP: LOI-based soil carbon group
  - BULK_DENSITY: bulk density (g soil per cm3)
  - MOISTURE_DRY: gravimetric water content on a dry basis
  - N_PERCENT: total soil nitrogen (%)
  - N_STOCK: nitrogen stock (t N per ha)
  - PO4_OLSEN: Olsen phosphorus (not measured in 2021 winter survey)
  - LC07 / LC07_NUM: ITE Land Classification (2007)
  - COUNTRY: GB country designation
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Data availability: documented in the dataset metadata (Table 5) and supported by UKCEH communications; contact information provided for data access.

## Context, references and further reading
- The dataset sits within a broader national soil-monitoring program and literature on soil health, carbon dynamics, and ecosystem services.
- Related references include foundational Countryside Survey reports (2007, 2010), methodological manuals (Soils Manual, 2008), and subsequent science papers on soil health benchmarks and soil carbon dynamics (e.g., Feeney et al., 2023; Keith et al., 2020; Robinson et al., 2024).
- For data access and methodological documentation, see the Countryside Survey project materials and UKCEH Soil Bank resources.

## Contact and governance
- Primary inquiries and data requests managed through UK Centre for Ecology & Hydrology channels (enquiries@ceh.ac.uk; social/website references provided).
- Data and methods referenced through multiple CEH-hosted documents and the Countryside Survey program website.