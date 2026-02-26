# Introduction

- This document describes the data assets underlying three related studies on Daphnia magna, detailing multiple CSV data files and their contents.
- Data cover palaeolimnological records, environmental and life-history traits, experimental traits under multiple stressors, and cross-study measurements from Lake Ring, Denmark (coordinates provided).
- Data sources include Danish pesticide records (1955–2010) and Danish national archives, with several laboratory-controlled experiments and factorial treatments.
- Common data-quality notes: many fields include Na or empty cells indicating missing data.

## Dataset overview

- Dataset 1: three CSV files
  - a) Cambronero_etal_Environmental_metadata.csv
    - Paleolimnological and historical data from Lake Ring sediment archive.
    - For each radiometrically dated year: nine columns include Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi depth, total nitrates (TN), total phosphates (TP).
    - Location: Lake Ring, Denmark (coordinates given). Time range for transparency, TN, TP: 1971–1999. Na denotes missing data.
  - b) Cambronero_etal_pesticides.csv
    - List of insecticides sold in Denmark by county authority (1955–2010).
    - Value: total amount (tons/year). Highlighted cells indicate carbamate insecticides; Carbaryl used in this study.
  - c) Cambronero_etal_life_history_traits_sr.csv
    - Life-history traits from eight columns: IndividualID, populationID, experimental exposure, and traits (mortality, size at maturity, age at maturity, fecundity).
    - Data collected after maternal effect control in three common garden experiments (CGE1–CGE3) with varying temperatures, food levels, and Carbaryl concentrations.
    - Experimental temperatures include 18°C and 24°C; food levels and Carbaryl concentrations specified; multiple exposure combinations (e.g., T18, T24, TFH/TFL variants, TIH/TIL variants).

- Dataset 2: three CSV files
  - d) Cambronero_etal_CTmax_bodysize.csv
    - 22 columns describing CTmax (temperature of maximum tolerance) and body size for 30 Daphnia magna genotypes.
    - Exposures include temperature alone (CGE1) and in combination with food levels (CGE2) or Carbaryl (CGE3).
    - Experimental temperatures: 18°C and 24°C; nutrient levels: 0.2 and 2.4 mg C/L; Carbaryl: 4 and 10 µg/L. Empty cells are missing data.
  - e) Cambronero_etal_Hb.csv
    - Total haemoglobin (Hb) content in µmol/L for the 30 genotypes at control (20°C) and after hyper-thermal stress (30°C).
    - Columns include GenotypeID, PopulationID, average Hb across replicates, and log2 fold change between temperatures.
  - f) Cambronero_etal_HSP_expression.csv
    - 27 columns detailing log2 fold-change in expression of four HSPs (HSP20, HSP60, HSP70, HSP90).
    - Measured under temperature ramping after common garden experiments and under non-ramped conditions.
    - Treatments include warming alone, warming with high/low food, and warming with Carbaryl; missing values indicated by empty cells.

- Dataset 3: two CSV files
  - g) Cambronero_etal_Environmental_data.csv
    - Paleolimnological and historical Lake Ring data.
    - Carbaryl usage (tons/year) from Danish national archives (1955–2010); LOI measured; ephippia of D. magna (N. ephippia/m2) hatched under standard lab conditions.
    - Na denotes missing data.
  - h) Cambronero_etal_life_history_traits_eva.csv
    - Individual and population-level life-history traits by experiment and treatment.
    - Full factorial design: two algae concentrations (high/low) and two insecticide concentrations (high/low) across two levels (single stress vs. pairs: HA/LA with HI/LI and combinations HALI, LAHI, LALI).
    - Includes mortality, age at maturity, fecundity, and size at maturity; Na indicates missing values.

## Data context and provenance

- Location and pressure history: Lake Ring, Denmark (geographic coordinates provided).
- Data sources: Danish pesticide records and national archives; laboratory experiments to study stressor effects on Daphnia magna.
- Data formats: CSV files (multiple per dataset) containing experimental, environmental, and life-history measurements.
- Metadata and annotations: explicit variable names, units, exposure conditions, and treatment combinations; several fields explicitly note missing data (Na or empty cells).

## Implications for data leadership and governance

- Data discovery and provenance
  - Clear linkage between datasets and published studies facilitates traceability and reuse.
  - Where data sources originate (national archives, published literature) should be captured in metadata for proper attribution.
- Data quality and completeness
  - Several fields include missing values; document gaps and consider imputation strategies or data completeness metrics for analyses.
  - Explicit treatment conditions (temperatures, nutrient levels, pesticide concentrations) enable reproducibility and cross-study comparisons.
- Data standards and interoperability
  - Consistent naming across files (Cambronero_etal_*.csv) supports integration; consider a centralized data catalog or data dictionary to enhance discoverability.
  - Metadata should capture units, coordinate references, experimental designs (full factorials), and processing steps.
- Data access and stewardship
  - Some data originate from archives and publications; ensure ongoing access paths and any usage restrictions are documented.
  - The dataset structure supports cross-study analyses of multiple stressors, aligning with broader data-system goals of understanding data utility across partners and communities.

## Takeaways for applying this in practice

- When planning data strategy, use this collection as a model for organizing multi-study, multi-file datasets with clear provenance, experimental conditions, and environmental measurements.
- Emphasize comprehensive metadata (variables, units, treatments, missing data notes) to improve discoverability, validation, and reuse.
- Prioritize establishing a data catalog entry for each dataset and file, including source references to the associated publications and archival records.
- Consider data quality dashboards to track missing data patterns and data completeness across datasets to inform prioritization and future data collection.