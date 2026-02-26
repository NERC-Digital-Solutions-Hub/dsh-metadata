# UKCEH Countryside Survey QA metadata and analysis report CS 2018/2019 - EIDC

## Overview and purpose
- A rolling, national-scale soil monitoring program ( Countryside Survey) designed to detect direction and magnitude of soil condition change across GB over time.
- Focuses on topsoil (0–15 cm) physico-chemical properties and co-located vegetation, to support understanding of soil function, carbon, nitrogen, and responses to multiple pressures.
- Supports policy-relevant questions and provides standardized data outputs (datasets, maps, charts) for scrutiny of environmental health and policy performance.

## Design and rolling programme
- Rolling survey adopted in 2019: repeats every five years or after 500 Squares completed, to capture change while buffering against extreme climate years.
- Sampling frame: 500 x 1-km squares per cycle, with 100 squares visited annually; strata defined by the Land Classification of GB.
- Exclusion criteria: squares with >75% urban land or >90% sea excluded.
- Past survey coordinates and sampling frames informed by 1978, 1998, and 2007 datasets to enable long-term comparisons.

## Sampling methods
- In each 1-km square, topsoil samples collected from five pre-determined randomly dispersed locations (X-Plots) within vegetation plots.
- Topsoil cores: 15 cm long, collected at 0–15 cm depth, co-located with vegetation surveys; samples stored and shipped to UKCEH laboratories.
- Location tracking and relocation: fixed plots marked since 1978; relocation accuracy checked via maps, photos, and GPS data.

## Metrics, laboratory protocols and analytical methods
- Core metrics (for fine earth and bulk soil): pH in deionised water; LOI (loss on ignition) to derive soil organic matter and carbon content; C_CONC_LOI (g C/kg soil); C_STOCK_LOI (t C/ha).
- Nutrients and soil properties: Olsen-phosphorus (PO4_OLSEN) for arable/improved grassland; total soil nitrogen (N_PERCENT and N_STOCK); bulk density (BULK_DENSITY); gravimetric water content (MOISTURE and MOISTURE_DRY); moisture content corrections.
- Land classification and zone data: ITE Land Classes (LC07, LC07_NUM) used for stratification; Environmental Zones (EZ_DESC_07) derived from multivariate analysis of Land Classes.
- Data processing: samples are logged, processed or stored in UKCEH laboratories; soil volume and stone corrections applied for carbon stock calculations; all units and conversions standardized (e.g., 0.15 m core depth, 1 ha = 10000 m2).

## Data quality assurance (QA)
- Robust QA workflow implemented with UKCEH laboratory staff and data scientists; uses R-based data processing and guidance documents.
- Field and lab QA controls include internal standards, duplicates (roughly 10%), blanks, and consistency checks for pH, LOI, and other metrics.
- LOI quality control relies on repeat measurements with internal standards and calcite checks; consistency thresholds applied to batching.

## Data structure and availability
- Dataset example described: 18 columns and 562 rows; missing samples denoted by -9999.
- Key schema includes: SQUARE (1-km square ID), PLOT (soil sampling location), YEAR (sampling year), PH, LOI, C_CONC_LOI, C_STOCK_LOI, SOIL_GROUP, BULK_DENSITY, MOISTURE, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN, LC07, LC07_NUM, COUNTRY, EZ_DESC_07.
- Data and metadata are designed for integration with GIS outputs (maps, charts) and for cross-year comparisons as part of the rolling programme.
- Primary data storage and access through UKCEH Soil Bank and relevant CEH data portals.

## Environmental zones and land classification context
- Environmental Zones (EZ_DESC_07) aggregate ITE Land Classes into ecologically coherent zones, enabling analysis of soil changes by landscape type.
- ITE Land Classification (LC07/LC07_NUM) provides the stratification framework across GB to support national and sub-national reporting.

## Practical implications for analysts
- Access to standardized, QA-validated topsoil metric data enables tracking of carbon stocks, nutrient status (P and N), pH, moisture, and bulk density over time and across environmental zones.
- Rolling programme design supports detecting medium-term changes and interactions between pressures (climate, deposition, land use).
- Data are suitable for producing national maps and trend analyses, supporting policy evaluation and environmental health scrutiny.
- Be aware of data structure conventions (e.g., -9999 missing values) and QA flags when combining datasets across years or zones.

## References and methodological basis
- Methods align with the Soils Manual (Emmett et al. 2008) and the Countryside Survey field and laboratory protocols; land classification (Bunce et al. 2007) and environmental zone frameworks underpin stratification and analysis.
- Supports integration with prior surveys (1978, 1998, 2007) for long-term trend assessment and policy-relevant reporting.