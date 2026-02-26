# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC Topsoil physico-chemical data 2018/2019

## Overview
- A QA metadata and analysis report for topsoil physico-chemical data from the UKCEH Countryside Survey (CS) 2018/2019, part of a rolling national soil monitoring program supported by NERC UK-SCAPE.
- Aims to track direction and magnitude of soil change across Great Britain (GB), focusing on topsoil condition (0–15 cm) and related vegetation context.
- Data are stored in the UKCEH Soil Bank; the 2019 cycle marks the start of a rolling sampling program with cycles of five years and up to 500 squares per cycle (100 squares visited annually).

## Design and Sampling (rolling program)
- Survey uses 1-km × 1-km squares across GB, with squares selected within strata defined by the Land Classification (LC07) and Environmental Zones (EZ) to enable robust national and sub-national indicators.
- Exclusion criteria: any square with more than 75% urban land or more than 90% sea is excluded.
- Sampling within each square: up to five sampling locations (PLOT) within a site, using vegetation X-Plots as reference points; soil cores collected to 15 cm depth.
- Rolling program specifics: 500 squares sampled in a five-year cycle; 100 squares are visited each year to balance spatial coverage and temporal monitoring.
- Relocation and older survey continuity: locations are tracked and relocated using maps, markers, photos, GPS; 2019 saw plots moved to a western corner of inner plots to improve relocation accuracy.

## Sample Collection and Laboratory Processing
- Field collection: five soil samples per square collected at predefined points; cores are refrigerated and shipped to UKCEH labs; samples stored in the UKCEH Soil Bank.
- Lab processing follows the Soils Manual; samples are analyzed for a suite of physico-chemical metrics; data are linked to long-term square and plot identifiers (SQUARE, PLOT, YEAR, COUNTRY).

## Metrics, Laboratory Protocols and Analytical Methods
- Core suite of metrics includes:
  - pH (soil in deionised water, field-moist bulk soil)
  - Loss-on-Ignition (LOI) and derived soil carbon concentration (C_CONC_LOI) and stock (C_STOCK_LOI)
  - Total soil nitrogen (N_PERCENT) and stock (N_STOCK)
  - Olsen phosphorus (PO4_OLSEN) for arable/improved grassland soils
  - Bulk density (BULK_DENSITY) and moisture content (MOISTURE, MOISTURE_DRY)
- LOI and carbon concentrations measured with a LECO ThermoGravimetric Analyser (TGA701), with four-step heating and 3-hour stabilization at 105°C to derive organic matter content.
- pH quality control includes internal standards and duplicate samples to ensure measurement accuracy.
- Olsen-P analysis uses standard colorimetric detection with calibration and moisture-corrected concentrations; QC includes duplicates and blanks.
- N_PERCENT measured with an accredited SOP using an elemental analyzer after ball-milling and drying; QC includes in-house references and standards.
- Calculations convert LOI to carbon stock, with explicit volume and area conversions (e.g., 0.15 m depth, 1 ha = 10,000 m²), accounting for bulk density and stones.

## Data Quality Assurance
- A formal QA workflow has been established for rolling surveys, implemented via R-based scripts and guidance documents to maintain high data standards.
- Quality control procedures cover all metrics: internal standards, duplicates, blanks, calibration checks, and batch-level QC for LOI, Olsen-P, and nitrogen analyses.

## Data Structure and Metadata
- Dataset characteristics: 18 columns, 562 rows; missing values denoted by -9999.
- Key columns include:
  - SQUARE (1-km square identifier), PLOT (soil sampling location within square), YEAR, PH (soil pH in water), LOI (g LOI per 100 g oven-dry soil), C_CONC_LOI (g C per kg soil), C_STOCK_LOI (t C per ha), SOIL_GROUP (LOI-based carbon grouping), BULK_DENSITY (g cm-3), MOISTURE (gravimetric water content), MOISTURE_DRY, N_PERCENT (g N per 100 g soil), N_STOCK (t N per ha), PO4_OLSEN (mg P per kg dry soil), LC07 (ITE Land Classification name), LC07_NUM (numeric code), COUNTRY (England/Scotland/Wales), EZ_DESC_07 (Environmental Zone description).
- Data are designed for integration with vegetation data and broader Countryside Survey analyses, enabling cross-metric, multi-scale interpretation.

## Access, Documentation and References
- Data are accompanied by extensive methodology and reference materials (CS Soils Manual and related Countryside Survey documents); contact and repository details are provided via the UKCEH and Soil Bank channels.
- The report includes extensive references to methodological manuals, QA procedures, and prior CS work, underscoring standardized, repeatable data collection and analysis.

## Relevance for Data Leaders (Data Strategy and Collaboration)
- Demonstrates a mature, scalable data system for national-scale environmental monitoring with rolling data collection, ensuring continuity and comparability over decades.
- Highlights the importance of robust metadata, standardized analytical protocols, and automated QA workflows to support reliable, reusable data assets.
- Illustrates effective data governance practices:
  - Clear data lineage (square/plot/year), standardized units, and explicit metadata about sampling design (LC07, EZ, country).
  - Data discoverability and reuse through centralized storage (Soil Bank) and consistent naming conventions for variables and carbon/nutrient stocks.
  - Ability to integrate soil data with vegetation and other environmental layers for holistic ecosystem assessments.
- Points to challenges and opportunities for data leaders:
  - Maintaining data standards across rolling cycles and evolving methodologies.
  - Ensuring accessibility while preserving data quality and traceability (QA documentation, calibration records, and QC results).
  - Leveraging stratification by Land Classification and Environmental Zones to enable targeted analyses and cross-network collaborations.
- Overall, provides a robust blueprint for managing complex, longitudinal environmental data assets, with strong emphasis on quality assurance, traceability, and cross-domain usefulness.