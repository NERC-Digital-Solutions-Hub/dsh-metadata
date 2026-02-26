# UKCEH Countryside Survey QA metadata and analysis report 2021 - EIDC Topsoil physico-chemical data 2021

## Purpose and scope
- Presents QA metadata, sampling design, laboratory protocols, and data structure for the 2021 topsoil physico-chemical data (0–15 cm) from UKCEH Countryside Survey.
- Part of the rolling Countryside Survey program (post-2019) funded by NERC UK-SCAPE to monitor soil condition and function across GB and detect changes over time.
- Data intended to support national-scale assessments of soil health, carbon pools, nutrients, and related ecosystem services.

## Survey design and rolling programme
- Rolling survey adopted in 2019: repeats every five years or after 500 squares completed; aims to maximize site coverage while capturing year-to-year change.
- 1-km x 1-km squares selected across GB within strata defined by Land Classification (LC07) to provide robust national and sub-national indicators.
- 100 squares visited annually; excludes squares with >75% urban land or >90% sea.
- Covid-19 disruption in 2020 led to partial resampling (50 squares reselected in England).

## Sample collection methods
- In each 1-km square, five topsoil samples collected at pre-determined locations coincident with vegetation X-Plots (5 locations per square where possible).
- Soil cores: 15 cm long, collected from field-moist surface within the 0–15 cm horizon; samples stored refrigerated and shipped to UKCEH laboratories.
- Historical context: sampling locations have maintained relocation and mapping records (e.g., 1978 central pits; 1998/2007 resampling 2–3 m apart; 2019 plots adjusted to inner corner of central 2 m x 2 m plot).

## Metrics, laboratory protocols and analytical methods
- Five soil cores per square sent for processing and analysis; soils stored in the UKCEH Soil Bank.
- Core-based measurements include:
  - pH (in deionised water) with field-moist bulk soil suspension; QA uses internal pH standards and duplicates.
  - Loss-on-Ignition (LOI) to estimate soil organic matter and carbon content (via LECO TGA701, 25–1000°C with defined heating steps).
  - Derived soil carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI) in fine earth (FE) at 0–15 cm.
  - Bulk density (BULK_DENSITY) and stone content to account for pore volume and to convert %C to C per unit volume.
  - Moisture contents: gravimetric water content (MOISTURE) and moisture on oven-dry basis (MOISTURE_DRY).
  - Olsen phosphorus (PO4_OLSEN) measured for arable/improved grassland soils only, via colorimetric molybdenum blue method.
  - Total nitrogen (N_PERCENT; % N) measured with Elementar VarioEL after ball milling and combustion.
- Units and conversions are defined for all measured and derived metrics (e.g., C stocks per hectare, volumes, and conversion factors).

## Data quality assurance (QA)
- Robust QA workflows implemented by UKCEH laboratory staff and data scientists; QA is performed regularly as part of the rolling survey framework.
- Quality controls embedded at multiple stages:
  - pH: internal standards, batch-level acceptance within ±2 standard deviations.
  - LOI: internal standards and calcite checks; batches repeated if controls deviate beyond thresholds.
  - Olsen-P and N analyses: use of blanks, duplicates, and reference materials; instrument calibration checks with standard materials.
- QA documentation and guidance implemented via R-based data workflows and supplementary documents.
- Data are stored in the UKCEH Soil Bank with traceable provenance and processing steps.

## Details of data structure
- Dataset comprises 18 columns and 496 rows; missing samples denoted by -9999.
- Key fields include:
  - SQUARE: 1-km survey square identifier (text)
  - PLOT: plot/ sampling location identifier within square (numeric)
  - YEAR: year of sampling (numeric)
  - PH: soil pH in water (numeric)
  - LOI: Loss-on-Ignition (% or g LOI per 100 g soil) (numeric)
  - C_CONC_LOI: derived soil carbon concentration (g C per kg soil) (numeric)
  - C_STOCK_LOI: carbon stock per hectare (t C ha-1) (numeric)
  - SOIL_GROUP: LOI-based carbon group category (categorical)
  - BULK_DENSITY: bulk density (g cm-3) (numeric)
  - MOISTURE: gravimetric water content (g water per g field-moist soil) (numeric)
  - MOISTURE_DRY: gravimetric water content on oven-dry basis (g water per g dry soil) (numeric)
  - N_PERCENT: total soil nitrogen percentage (g N per 100 g soil) (numeric)
  - N_STOCK: nitrogen stock per hectare (t N ha-1) (numeric)
  - PO4_OLSEN: Olsen phosphorus (mg/kg) (numeric)
  - LC07, LC07_NUM: ITE Land Classification (text and numeric) per 2007 scheme
  - COUNTRY: GB country (England/Scotland/Wales) (categorical)
  - EZ_DESC_07: Countryside Survey Environmental Zone description (text)
- Metadata indicates measurement methods, units, and data lineage (e.g., year, sampling location, lab methods).

## Data processing, storage and provenance
- Samples processed and stored at UKCEH laboratories; processed/stored samples may be frozen and archived in the Soil Bank.
- Data workflow and QA implemented using R scripts; documentation supports reproducibility and auditability.
- Data are intended for updating and integration with ongoing Countryside Survey outputs, enabling temporal comparisons (2019+ rolling dataset).

## Accessibility, usage, and limitations
- Data linked to Countryside Survey portals and UKCEH Soil Bank; contact details provided for access and inquiries.
- Data include some missing entries (-9999) and are subject to the rolling program’s updates; users should consider the 2020 Covid disruption and planned annual/5-year cycles when interpreting time series.
- Environmental Zones and Land Class categorizations enable stratified analyses across GB regions and habitat types.

## Implications for data stewardship
- Emphasize consistent metadata standards, clear provenance, and versioning across rolling survey cycles.
- Maintain alignment between sample collection methods, lab protocols, and derived metrics to ensure comparability over time.
- Monitor and document plot relocation, sampling point redefinitions, and any changes in sampling density (e.g., Covid-related resampling) to preserve temporal integrity.
- Ensure QA workflows and reference materials are up to date; keep detailed records of batch-level controls for traceability.
- Facilitate data access through established portals, with appropriate governance for sensitive or embargoed data as needed.