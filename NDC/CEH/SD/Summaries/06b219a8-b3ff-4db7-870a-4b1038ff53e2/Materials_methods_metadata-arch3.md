# Global data for soil water, groundwater and riverine freshwater DO14C data taken from 'Linking soil solution and riverine DO14C to soil carbon turnover', Adams et al, 2019 Biogeochemistry.

## Overview
- Compiles global datasets of dissolved organic carbon (DOC) concentration and DO14C (radiocarbon content) in soil water, groundwater, and riverine freshwater.
- Literature data span: soil water DOC/DO14C (1989–2015), groundwater DO14C (1988–2008), riverine DO14C (1962–2015), building on Marwick et al. 2015 with additional data before/after that collection.
- Includes new UK river sampling (2013–2015) to extend temporal coverage and data depth.

## Data sources and compilation
- Literature data:
  - DOC concentration and DO14C in soil solutions; river data linked to Marwick et al. (2015) with added pre/post data.
  - Data extraction from graphs when necessary using ENGAUGE digitizer.
  - River discharge data compiled where available for single-site records.
- New measurements (TableS3_River_Surface_Water_New):
  - UK river sampling by CEH, JHI, and UEA (2013–2015).
  - Rigorous sample collection, filtration, and storage protocols; use of new or acid-washed equipment.
  - DOC determinations and radiocarbon analyses conducted at specialized facilities (e.g., SUERC AMS).
  - δ13C and δ14C measurements; graphite target preparation; quality checks, re-analyses as needed.
- Site information:
  - Land class assignments (per TableS1_Soil_water_data.csv) to categorize catchments (pure, NSN, F, W).
  - Discharge data used for hypothesis testing only when quantified.

## Metadata and data structure
- TableS1_Soil_water_data.csv and TableS2_Groundwater_data.csv:
  - Comprehensive column definitions covering location, country, coordinates, date, vegetation, land class, soil/aquifer details, [DOC], 13C, delta14C, notes, and references.
- TableS3_River_Surface_Water_New.csv:
  - Data_line, country/region, site, year, coordinates, [DOC]_mg/L, delta13C, delta14C, land_class, publication_code.
- Additional datasets referenced:
  - TableS3_Marwick_River_Surface_Water.csv and TableS3_Extra_Published_River_Surface_Water_Data.csv with similarly structured metadata and data fields.
- References:
  - Extensive citations for soil water, groundwater, riverine DOC and radiocarbon data (original publications and theses) to support data provenance.

## Data processing, quality control, and isotopic corrections
- Radiocarbon (14C) data:
  - Reported as pMC and converted to Δ14C with corrections for decay since 1950.
  - 14C enrichment calibrated against international standards; precision typically around ±0.1‰ for δ13C and ~0.45 pMC for 14C measurements, with adjustments for potential carbonate contamination.
  - Samples with high δ13C values (indicative of incomplete carbonate purge) re-analysed with more stringent purge (pH adjustments) and, in some cases, δ13C values treated as not representative.
- Quality assurance:
  - Size-matched process blanks and age standards used; cross-checks against established laboratories and references.
  - Archival samples (from 1960s–1970s) included with consistent processing analogies to contemporary methods.

## Data sharing, metadata, and governance
- Metadata completeness and accessibility are central considerations:
  - Detailed metadata schemas included (TableS1/S2 column explanations) to facilitate reuse and verification.
  - Public sharing of underlying data is emphasized, with explicit requirements to document data provenance and processing steps.
  - Acknowledges and documents data gaps, access barriers, and the need for harmonized data governance when integrating datasets from multiple sources.
- Dataset scope and reproducibility:
  - Clear documentation of sampling methods, analytical procedures, and data transformation steps to support reproducibility in monitoring frameworks.
  - Data compilation draws on multiple sources and includes digitization steps to maximize usable coverage.

## Statistical analyses
- Methods:
  - t-tests and linear regressions conducted in Microsoft Excel.
  - Normality checks and variance assessments; log transformations applied as needed prior to regression analyses.

## Implications for monitoring frameworks
- Demonstrates the value of assembling multi-source environmental health data (soil, groundwater, rivers) with consistent metadata to support policy scrutiny and decision-making.
- Highlights practical challenges relevant to monitoring programs:
  - Data gaps and access limitations; data silos across organizations.
  - Importance of metadata quality, standardized data formats, and transparent data governance.
  - Barriers to sharing underlying data publicly, and the need for clear provenance and versioning.
- Provides a model for data integration, metadata documentation, QA/QC, and reproducible analyses that can inform future monitoring approaches and policy evaluations.