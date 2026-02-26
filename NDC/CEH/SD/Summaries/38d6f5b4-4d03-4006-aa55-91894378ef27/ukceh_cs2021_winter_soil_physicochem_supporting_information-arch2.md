# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

## Summary
- Long-running national soil monitoring program (Countryside Survey) transitioned to a rolling five-year cycle starting in 2019 to detect change in topsoil condition and function.
- The 2021 winter topsoil survey used a subset of the complete square population, prioritising historic (1978/1998/2007) squares and reflective environmental zones.
- Data support policy-relevant questions on how multiple pressures affect soil properties, carbon dynamics, nutrient status, and soil physical condition.

## Study design and scope
- Rolling program: 500 x 1-km2 squares sampled over five years; 100 squares visited annually.
- Stratification: squares drawn within Land Classification (ITE LC07) strata; urban/seas excluded (max 75% urban; >90% sea excluded).
- Environmental context: environments defined by Countryside Survey Environmental Zones (EZ_DESC_07) derived from ITE Land Classes.
- 2020 Covid disruption: survey paused in early 2020; rescheduled sampling in late 2020 with 50 England-only squares.
- Winter 2021 sampling: focused on topsoil 0–15 cm within five randomly dispersed plots per square; 30 (+5 reserve) squares selected to represent environmental zones for winter survey.

## Sampling methodology
- Within each square: five randomly dispersed sampling locations aligned with vegetation X-Plots.
- Core depth and sampling: 15 cm long black plastic core collected from each location; field-moist bulk soil used for measurements.
- Plot relocation: historic markers used for relocalisation; uniform protocols for sample location relative to vegetation quadrats.
- Data capture: field data include Broad Habitat for winter sampling; precise location coordinates stored via Square/Plot identifiers.

## Metrics, laboratory protocols and analytical methods
- Core processing: five soil samples per location stored and transported to UKCEH laboratories; soil bank storage for processed/frozen samples.
- Key metrics measured (0–15 cm fine earth):
  - pH in deionised water (PH)
  - Loss-on-Ignition (LOI) as soil organic matter; LOI-derived carbon concentration (C_CONC_LOI) and carbon stock (C_STOCK_LOI)
  - Bulk density (BULK_DENSITY) and stone content for porosity calculations
  - Moisture content: MOISTURE_DRY (gravimetric dry basis) and MOISTURE (wet basis)
  - Total nitrogen (N_PERCENT, N_STOCK)
  - Olsen phosphorus (PO4_OLSEN) not measured in 2021 winter survey; reported for compatibility with other datasets
- LOI-based carbon calculations: C_CONC_LOI = 0.55 × C_FE_LOI × 10; C_STOCK_LOI derived per hectare using LOI-derived carbon and bulk density
- Data units and conversions detailed (depth, area, density) to enable stock calculations
- Land Classification (LC07) and country-level identifiers (ENG/SCO/WAL) underpin data structure

## Quality assurance and data management
- Multi-stage QA workflow:
  - Lab data QA: internal checks on values, gaps, relationships, and standards; flag and correct as needed
  - Analyst QA1: cross-check lab data against measurement records; document changes
  - Derivation of soil metrics via two R scripts to ensure reproducibility
  - Analyst QA2: automated HTML QA report assessing patterns, outliers, and historical comparators
- Transparent audit trail: all dataset changes linked to QA steps and logged for reproducibility
- Data integration: derived soil metrics linked with habitat/vegetation data for holistic QA

## Data structure and accessibility
- Dataset characteristics: 18 columns, 576 rows; missing samples denoted by -9999
- Variables include: SQUARE, PLOT, YEAR, PH, LOI, C_CONC_LOI, C_STOCK_LOI, SOIL_GROUP, BULK_DENSITY, MOISTURE_DRY, N_PERCENT, N_STOCK, PO4_OLSEN (not measured in 2021 winter), LC07, LC07_NUM, COUNTRY, EZ_DESC_07
- Data schema supports cross-reference with ITE Land Classification, Environmental Zones, and regional identifiers
- Data are stored and managed via UKCEH Soil Bank and standard Countryside Survey data portals

## Context and implications for monitoring
- Aims address interactions among multiple pressures on soil condition, carbon pools, and nutrient dynamics, with attention to land-use change and atmospheric deposition effects
- Rolling design buffers against climate year variability and increases site coverage while enabling year-on-year trend detection
- The 2021 winter dataset focuses on baseline conditions for carbon, nitrogen, moisture, pH, and LOI-derived metrics, enabling comparisons with historical surveys and future cycles
- Data quality and standardised protocols support robust monitoring of soil health and contribute to policy-relevant assessments of soil status across Great Britain