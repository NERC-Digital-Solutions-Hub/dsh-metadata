# Introduction Dataset 1, Dataset 2 comprises three excel files each and Dataset 3 comprises 2 Comma separated values (.csv) files.

## Overview
- Three datasets (Dataset 1, Dataset 2, Dataset 3) correspond to three separate publications focusing on Daphnia magna and responses to multiple stressors.
- Data formats across files are CSV (Datasets 1–3) and CSVs linked to published studies; some entries contain missing data (noted as Na or empty cells).
- Key geographic reference: Lake Ring, Denmark (coordinates provided in several files).

## Dataset 1
- Files:
  - Cambronero_etal_Environmental_metadata.csv
  - Cambronero_etal_pesticides.csv
  - Cambronero_etal_life_history_traits_sr.csv
- What they contain:
  - Environmental_metadata: paleolimnological and historical data from the sedimentary archive of Lake Ring; for each radiometrically dated year, includes nine columns: Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi depth (transparency), total nitrates (TN), total phosphates (TP); Na indicates missing data; transparency/TN/TP data cover 1971–1999.
  - Pesticides: list of insecticides sold in Denmark (1955–2010) with tons/year; highlighted cells denote carbamate insecticides; Carbaryl specifically used in the study.
  - Life_history_traits_sr: life history data from experimental setups across eight columns per observation (IndividualID, populationID, experimental exposure and life history traits such as mortality, size at maturity, age at maturity, fecundity); maternal effects controlled; three common garden experiments (CGE1–CGE3) differing in temperature, food level, and Carbaryl concentration.
- Purpose/usage context:
  - Provides environmental context, pesticide exposure data, and organismal life-history responses to single and combined stressors, enabling analyses of environmental change impacts on Daphnia through multiple lines of evidence.

## Dataset 2
- Files:
  - Cambronero_etal_CTmax_bodysize.csv
  - Cambronero_etal_Hb.csv
  - Cambronero_etal_HSP_expression.csv
- What they contain:
  - CTmax_bodysize: 22 columns summarizing CTmax (temperature of maximum tolerance) and body size for 30 Daphnia magna genotypes from Lake Ring; data collected after exposure to temperature alone (CGE1) and with either food levels (CGE2) or Carbaryl (CGE3). Experimental temperatures: 18°C and 24°C; nutrient levels: 0.2 mg C/L and 2.4 mg C/L; Carbaryl concentrations: 4 μg/L and 10 μg/L; missing data indicated by empty cells.
  - Hb: total haemoglobin content (µmol/L) for the 30 genotypes at control (20°C) and after hyper-thermal stress (30°C); columns include GenotypeID, PopulationID, average Hb across replicates, and log2 fold change between temperatures.
  - HSP_expression: 27 columns describing log2 fold changes in expression of four heat shock proteins (HSP20, HSP60, HSP70, HSP90); measured for genotypes under temperature ramping after common garden experiments, including single stress (warming), warming with food limitation, and warming with Carbaryl; missing values indicated by Na.
- Purpose/usage context:
  - Provides physiological and molecular responses to thermal stress and stressor combinations, enabling analyses of genotype-specific thermal tolerance, hematological responses, and heat-shock protein expression under varying environmental conditions.

## Dataset 3
- Files:
  - Cambronero_etal_Environmental_data.csv
  - Cambronero_etal_life_history_traits_eva.csv
- What they contain:
  - Environmental_data: paleolimnological and historical data from Lake Ring (1955–2010); Carbaryl insecticide usage from Danish national archives; LOI measurements; ephippia of D. magna hatched under standard laboratory conditions; Na indicates missing data.
  - Life_history_traits_eva: per-individual life history traits with population-level maternal effect control; full factorial design varying two algae concentrations (low 0.2 mg Carbon/L; high 2.4 mg Carbon/L) and two insecticide concentrations (low 4 μg/L; high 10 μg/L); treatments include single stressors and pairwise stressor combinations (HA, LA, HI, LI, and HAHI, HALI, LAHI, LALI); missing data indicated by Na.
- Purpose/usage context:
  - Supports examination of evolutionary and fitness responses to multiple stressors across environmental history, enabling comparisons of single vs. interacting stressors in naturalistic and laboratory conditions.

## Data Governance Considerations for Data Stewards
- Provenance and publication linkage:
  - Datasets are tied to three published studies (2018 Scientific Reports; 2018 Molecular Ecology; 2021 Evolutionary Applications), enabling traceable lineage and reuse with proper citation.
- Data formats and interoperability:
  - All data are stored as CSVs with explicit missing data markers (Na) or empty cells; consider providing a dataset-level and file-level metadata schema to harmonize variable names, units, and factor levels across datasets.
- Metadata and documentation:
  - Detailed descriptions of experimental designs (CGE1–CGE3, factorial treatments), units (e.g., µmol/L, mg C/L, °C, μg/L), and geographic context (Lake Ring coordinates) are present, but centralized metadata would improve discoverability and reuse.
- Data quality and updates:
  - Missing data are present in several files; establish clear data quality rules, imputation guidance, and any embargo or access restrictions if applicable.
- Stewardship actions recommended:
  - Create a unified metadata record (dataset-level) articulating scope, methods, variables, units, data collection periods, and data provenance.
  - Align variable naming and units across datasets to facilitate integration (e.g., CTmax, body size, Hb, HSP expression, LOI, Secchi depth).
  - Provide versioning and change logs for dataset updates; include links to associated publications and any related code or analytical pipelines.
  - Include data usage notes clarifying limitations due to missing values and experimental design nuances (single vs. multi-stressor contexts, genotype-specific responses).