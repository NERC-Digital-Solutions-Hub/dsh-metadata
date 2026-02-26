# Winter topsoil physicochemical properties from the UKCEH Countryside Survey, Great Britain, 2021

## Purpose and context
- Countryside Survey is a long-term audit of the UK’s countryside (since 1978) to detect gradual changes over time.
- The 2019+ rolling programme aims to quantify direction and magnitude of soil change and how multiple pressures interact, with emphasis on topsoil condition, carbon, pH, compaction, nutrients, and vegetation feedback.
- The 2021 dataset contributes to national-scale soil health understanding and supports comparisons with previous surveys (1998, 2007, 2019+).

## Survey design and rolling program
- Rolling survey: 5-year cycle across 500 randomly selected 1-km x 1-km squares; 100 squares visited per year, with stratification by Land Classification (ITE Land Classes, 2007).
- Exclusions: squares with >75% urban land or >90% sea were removed.
- Covid disruption in 2020 led to partial resampling; 50 England-only squares were added later.
- Winter-sampling subset: hierarchical selection prioritising historic survey squares (1978, 1998, 2007) and environmental zones; 30 (+5 reserve) winter squares from the 2021 rolling survey to reflect environmental zones.

## Sample collection methods
- Within each 1-km square, topsoil samples were collected from up to five randomly dispersed locations aligned with vegetation X-Plots.
- Core depth: 15 cm; standard location relative to the 2 m x 2 m vegetation quadrat.
- Winter survey recorded Broad Habitat only; historical and relocation details provided for longitudinal consistency.
- Post-collection handling: cores refrigerated, then shipped to UKCEH laboratories for processing and storage in the Soil Bank.

## Metrics, laboratory protocols and analytical methods
- Key soil metrics (0–15 cm fine earth): pH (in deionised water), LOI (loss on ignition) for organic matter and carbon content, carbon stock calculations, bulk density, and moisture.
- LOI method: ThermoGravimetric Analyser (LECO TGA701) with four heating steps; LOI% and derived soil carbon concentrations (C_CONC_LOI) and carbon stocks (C_STOCK_LOI) computed using specified formulas.
- Carbon group classification (SOIL_GROUP) based on LOI levels (Mineral, Humus mineral, Organo-mineral, Organic).
- Nutrients: Total nitrogen (N_PERCENT and N_STOCK) measured via elemental analysis (Vario-EL), with calibration standards and references.
- Olsen phosphorus (PO4_OLSEN) not measured in the 2021 winter survey but included in related datasets for compatibility.
- pH quality control: internal standards and duplicates; calibration checks using standard references.
- Units and conversions: depth 0.15 m considered for core; soil area and density conversions detailed (e.g., C_STOCK_LOI per hectare).

## Data quality assurance
- Multi-layer QA workflow to ensure data integrity:
  - Lab data QA: initial checks for outliers, data gaps, and standard stability.
  - Analyst QA1: cross-check lab data against measurement records; document queries and changes.
  - Derivation of soil metrics via two R scripts to ensure reproducibility and traceability.
  - Analyst QA2: automated HTML QA report assessing patterns, expected relationships, and comparisons with past data; coordination with labs for outstanding queries.
- All data changes are recorded for transparency and auditability; QA processes link soil data with vegetation and habitat data.

## Details of data structure
- Dataset characteristics: 18 columns, 576 rows; missing samples denoted by -9999.
- 2021 winter survey focuses on topsoil (0–15 cm); Olsen-P not measured but data included for compatibility.
- Key fields in the dataset:
  - SQUARE (1-km survey square ID)
  - PLOT (plot number within the square)
  - YEAR (year of survey; dataset notes suggest 2022 in metadata)
  - PH (soil pH in deionised water)
  - LOI (g LOI per 100 g oven-dry soil; %)
  - C_CONC_LOI (g C per kg oven-dry soil)
  - C_STOCK_LOI (t C per ha)
  - SOIL_GROUP (carbon group classification)
  - BULK_DENSITY (g soil per cm^3)
  - MOISTURE_DRY (gravimetric water content per g dry soil)
  - N_PERCENT (g N per 100 g soil)
  - N_STOCK (t N per ha)
  - PO4_OLSEN (not measured in 2021 winter; NA for this survey)
  - LC07, LC07_NUM (ITE Land Classification 2007)
  - COUNTRY (GB country)
  - EZ_DESC_07 (Environmental Zone description)
- Data processing: carbon stocks derived from LOI-derived carbon concentrations; volume and density calculations standardised (e.g., core volume, stone corrections).

## Limitations and caveats
- Olsen phosphorus not measured in the 2021 winter survey.
- Data reflect a winter/topsoil snapshot; seasonal and spatial coverage may influence comparability with other surveys.
- Covid-related disruptions affected the sampling effort in 2020.

## Accessibility and usage notes
- Data are part of the UKCEH Soil Bank and Countryside Survey program, with detailed metadata and QA documentation available.
- Suitable for analyses of topsoil condition change, carbon dynamics, nutrient status, and relationships with environmental zones and land classes; designed to support cross-year comparisons within the rolling survey framework.