# Soil physico-chemical properties 1998 [Countryside Survey], Great Britain

## Overview
- Dataset from Countryside Survey (1998/1999) providing soil physico-chemical properties for up to 256 1km squares across Great Britain.
- Supports environmental health monitoring and policy evaluation by supplying indicators of soil condition, carbon content, and nutrient status.
- Data owned by NERC - Centre for Ecology & Hydrology; requires acknowledgment in all uses and publications.

## Data content and structure
- File: CS1998_SOIL_PHYSICOCHEM.csv
- Sampling scope: top 15 cm of soil, 10 g samples, across up to 256 1km squares; year 1998/1999.
- Key columns and meanings:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot within each square
  - YEAR: Survey year
  - PH: Soil pH
  - LOI: Loss on ignition (%)
  - C_CONC_LOI: Carbon concentration calculated from LOI (g/kg) using 0.55 × LOI
  - C_STOCK_LOI: Carbon stock (t/ha) calculated from LOI using 0.55 × LOI
  - N_PERCENT: Total nitrogen (%)
  - PO4_OLSEN: Olsen phosphorus (mg/kg)
  - LC07 / LC07_NUM: ITE Land Classification 2007 (text and numeric code)
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: Administrative area (Eng/Wal) or Council (Sco)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- LOI and carbon metrics:
  - LOI-derived carbon concentration and stock use a conversion factor of 0.55 (updated from earlier 0.50 value).
- Data provenance references and methodological details are provided to support traceability and replication.

## Measurement methods

- Loss-on-ignition (LOI)
  - Purpose: estimate soil organic matter and approximate soil organic carbon concentration.
  - Protocol: samples from the top 15 cm; 10 g soil dried at 375°C for 16 h, then 1 g sub-sample combusted at 550°C for 3 h; LOI calculated from weight loss.
  - Conversion: LOI to soil carbon concentration uses a factor of 0.55 (revised from 0.50); carbon stock derived from LOI with the same factor.

- Soil pH
  - Method: measured in suspension with de-ionised water at soil-to-water ratio of 1:2.
  - Procedure: mix soil with water, allow to stand 30 minutes, measure pH after 30 seconds.

- Total nitrogen
  - Analysis: up to 1280 samples analysed with Elementar Vario-EL elemental analyser.
  - Principle: oxidative combustion followed by detection; QA using in-house reference materials.

- Olsen phosphorus (P)
  - Method: extract 5 g soil with 100 ml 0.5 M sodium bicarbonate (pH 8.5); determine phosphorus colorimetrically via molybdenum blue with dialysis to mitigate reagent effects.
  - QA: two in-house reference materials analysed with each batch.

## Data governance and provenance

- Data ownership and rights noted; all uses must acknowledge Countryside Survey data.
- Documentation includes extensive references and links to methodology and supporting publications.
- Data interoperability relies on metadata (where gaps exist, data originators may need to be contacted); data transformations (e.g., LOI to carbon metrics) are documented.

## Relevance for monitoring frameworks

- Provides standardized soil health indicators suitable for evaluating policy impacts and changes over time.
- Enables cross-site comparisons via consistent sampling depth, units, and conversion factors.
- Includes land classification and environmental zone descriptors to contextualize soil properties within landscape types.
- Highlights governance considerations relevant to monitoring programs, such as data sharing, metadata quality, and attribution requirements.

## References and further information

- Countryside Survey project overview and methodologies; CEH/Countryside Survey materials.
- Key publications and datasets related to soil quality and land classification (e.g., MASQ, ITE Land Classification 1996–2007, Carey et al. 2008 UK results).
- Data access and citation guidance provided within the dataset documentation.