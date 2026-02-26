# UKCEH Countryside Survey QA metadata and analysis report CS 2020 - EIDC Topsoil physico-chemical data 2020

- Purpose and scope
  - Documents QA metadata and analysis methods for the UKCEH Countryside Survey topsoil data from 2020.
  - Part of a rolling national soil monitoring program (since 2019) to track changes in topsoil condition and function across Great Britain and to understand interactions with vegetation and pressures.
  - Supports analyses of soil health, carbon pools, nutrient status, and responses to management and environmental pressures.

- Background and program context
  - Countryside Survey: ongoing national audit of UK countryside resources, with a history dating back to 1978; enables comparisons from 2019+ with earlier surveys to detect changes over time.
  - Rolling survey design: repeats every five years or after 500 squares completed; includes 100 squares visited annually; aims to maximize spatial coverage while capturing year-to-year change.
  - Major focus areas: topsoil condition and vegetation interactions, soil carbon pool changes, pH changes, nutrient dynamics (e.g., phosphorus), soil compaction, and responses to land use change and atmospheric deposition.

- Covid disruption in 2020
  - Restrictions in May–June limited fieldwork; later activity resumed in July–August.
  - 50 squares were reselected in England to accommodate disruption.

- Sampling design and locations
  - Sampling unit: 1-km x 1-km squares; up to five sampling locations (PLOTs) per square, aligned with vegetation X-Plots.
  - Soil depth: topsoil cores from approximately 0–15 cm.
  - Location tracking: long-term squares identified by SQUARE; within-square sampling by PLOT_ID; country coded as ENG, SCO, WAL.
  - Land classification and stratification: 2007 ITE Land Classes (LC07) used for stratification across GB; Environmental Zones (EZ_DESC_07) derived from multivariate analysis of environmental data.
  - Exclusions: squares with >75% urban land or >90% sea excluded from selection.

- Sample collection methods
  - Five topsoil samples collected per square from predefined random locations, with cores taken at the corner of a 2x2 m vegetation quadrat.
  - Sample handling: cores refrigerated and shipped to UKCEH laboratories (Bangor) for processing and storage in the UKCEH Soil Bank.
  - Plot relocation: 1998/2007 sampling locations resampled within 2–3 m; 2019 plots moved to a fixed western corner of the inner 2x2 m plot to aid relocation accuracy (with verification via photos, maps, GPS).

- Metrics, laboratory protocols, and analytical methods
  - Field-to-lab workflow: five soil cores per square (locations tagged by SQUARE/PLOT/YEAR); samples analyzed for soil metrics; processed samples stored in the Soil Bank.
  - Key soil metrics and derivations:
    - pH (PH): measured in deionised water using field-moist bulk soil; QA includes internal pH standards and duplicate samples (~10%).
    - Loss-on-Ignition (LOI) and soil carbon (C_CONC_LOI, C_STOCK_LOI): LOI determined by ThermoGravimetric Analysis (LECO TGA701) from 25°C to 1000°C with four steps; LOI% used to derive soil organic matter and carbon concentrations; C_STOCK_LOI calculated per hectare using soil volume and bulk density.
    - Soil bulk density (BULK_DENSITY): calculated from 15 cm core with adjustments for stones; used to convert %C to carbon stock per volume.
    - Fine earth moisture (MOISTURE, MOISTURE_DRY): gravimetric water content for field-moist and oven-dried soil, respectively.
    - Olsen phosphorus (PO4_OLSEN): measured on arable/improved grassland soils; extraction with 0.5 M NaHCO3 and colorimetric analysis; QA includes blanks and duplicates.
    - Total soil nitrogen (N_PERCENT, N_STOCK): measured with an Elementar VarioEL elemental analyzer after ball-milling and drying; units are % N and t N per ha; QA uses internal references and calibration checks.
  - Quality control (QC) framework
    - pH QC: internal standards with ±2 SD acceptance.
    - LOI QC: internal standards and calcite checks; batches flagged if LOI standards deviate beyond 2 SD.
    - P and N QC: in-house reference materials and calibration checks; regular use of blanks and duplicates.
  - Data processing and QA workflow
    - Large-scale QA and data processing conducted with R-based workflows and guidance documents to ensure consistency and traceability.
    - Emphasis on robust data quality, clear documentation, and repeatable procedures.

- Data structure and metadata
  - Dataset composition: 18 columns and 194 rows; missing samples denoted by -9999.
  - Principal columns and meanings:
    - SQUARE: 1-km square identifier (text)
    - PLOT: plot number within square (numeric)
    - YEAR: year of soil sampling (numeric)
    - PH: soil pH in water (numeric)
    - LOI: Loss-on-Ignition (g LOI per 100 g or % LOI depending on context)
    - C_CONC_LOI: soil carbon concentration (g C per kg oven-dry soil)
    - C_STOCK_LOI: soil carbon stock (t C per ha)
    - SOIL_GROUP: LOI-based soil carbon grouping
    - BULK_DENSITY: bulk density (g soil per cm3)
    - MOISTURE: gravimetric water content (wet basis)
    - MOISTURE_DRY: gravimetric water content (dry basis)
    - N_PERCENT: total soil nitrogen (%)
    - N_STOCK: total soil nitrogen stock (t N per ha)
    - PO4_OLSEN: Olsen phosphorus concentration (mg/kg)
    - LC07: ITE Land Classification description (text)
    - LC07_NUM: Land Classification numeric code
    - COUNTRY: country code (ENG/SCO/WAL)
    - EZ_DESC_07: Environmental Zone description
  - Reference framework and data lineage
    - Land Classification (ITE) and Environmental Zones are derived classifications linked to long-running GB soil mapping efforts.
    - The dataset aligns with UKCEH soil banking and Countryside Survey documentation and is designed for cross-year comparability (1978, 1998, 2007, 2018–2019, 2020).
  - Availability and references
    - Data and methodology referenced to CEH/UKCEH Countryside Survey reports and associated manuals (Soils Manual, 2007; Soil Change analyses; environmental zones documentation).

- Application and implications for analysis
  - The dataset enables correlations between topsoil physico-chemical properties and vegetation/habitat classifications, land use, and environmental pressures.
  - Facilitates examination of trends in soil carbon stocks, pH shifts, nitrogen status, phosphorus availability, moisture regimes, and soil structural changes (bulk density, porosity) across GB.
  - Designed to support modeling of drivers of soil change, interactions between pressures, and spatial-temporal mapping of soil condition and function at national and sub-national levels.
  - QA and standardized metadata enhance reproducibility, data discoverability, and cross-study comparisons, addressing typical data-access and standardization challenges highlighted for Analysts working with large environmental datasets.