# Introduction

- This document outlines three datasets (Dataset 1–3) and the CSV files they comprise, each linked to published studies on Daphnia magna and environmental stressors. It details data types, variables, measurement contexts, time ranges, and site information to support data discovery, combination, and analysis.

## Dataset 1
- a) Cambronero_etal_Environmental_metadata.csv
  - Source: sedimentary archive of Lake Ring, Denmark (coordinates provided).
  - For each radiometrically dated year: 9 columns including Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi depth (transparency), total nitrates (TN), total phosphates (TP).
  - Missing data indicated as Na.
  - Data for transparency, TN, and TP cover 1971–1999.

- b) Cambronero_etal_pesticides.csv
  - List of insecticides sold in Denmark (1955–2010) by the Danish county authority.
  - Value in tons per year; highlighted cells indicate carbamate insecticides, specifically Carbaryl used in the study.

- c) Cambronero_etal_life_history_traits_sr.csv
  - Life history traits for individuals across eight columns: IndividualID, populationID, experimental exposure, and traits (mortality, size at maturity, age at maturity, fecundity) after maternal effects were controlled.
  - Three common garden experiments (CGE1–CGE3) with varying temperature (18°C, 24°C), food levels (0.2 mg C/L, 2.4 mg C/L), and Carbaryl concentrations (4 μg/L, 10 μg/L).
  - Detailed exposure codes (e.g., T18, T24, TFH18, TFL24, TIH18, TIL24, etc.).

## Dataset 2
- d) Cambronero_etal_CTmax_bodysize.csv
  - 22 columns summarizing 3 experimental data on temperature of maximum tolerance (CTmax) and body size for 30 Daphnia magna genotypes.
  - Exposures: temperature alone (CGE1) and with either food levels (CGE2) or Carbaryl (CGE3).
  - Experimental temperatures: 18°C and 24°C; nutrient levels: 0.2 mg C/L and 2.4 mg C/L; Carbaryl concentrations: 4 μg/L and 10 μg/L.
  - Missing data represented by empty cells.

- e) Cambronero_etal_Hb.csv
  - Total haemoglobin content (µmol/L) in the 30 genotypes at control (20°C) and after hyper-thermal stress (30°C).
  - Columns: Genotype ID, Population ID, mean Hb across three replicates, and log2 fold change between temperatures.

- f) Cambronero_etal_HSP_expression.csv
  - 27 columns detailing log2-fold changes of four heat shock proteins (HSP20, HSP60, HSP70, HSP90).
  - Measured on genotypes exposed to temperature ramping (TR) immediately after common garden experiments, including single-stress (warming) and combinations with food limitation or Carbaryl.
  - Conditions include warming with/without additional stresses; missing values indicated as empty.

## Dataset 3
- g) Cambronero_etal_Environmental_data.csv
  - Paleolimnological and historical data from Lake Ring, Denmark.
  - Carbaryl usage (tons/year) from Danish national archives (1955–2010).
  - LOI measurements from sediment subsamples and standard hatch conditions for ephippia (N. ephippia/m2) after hatching experiments.
  - Missing data indicated as Na.

- h) Cambronero_etal_life_history_traits_eva.csv
  - Individual-level data: IndividualID, PopulationID, Experiment, Treatment, and life history traits (mortality day, mortality event, age at maturity, fecundity, size at maturity).
  - Full factorial design with two algae concentrations (low 0.2 mg C/L; high 2.4 mg C/L) and two insecticide concentrations (low 4 μg/L; high 10 μg/L), evaluating single vs. paired stressors (HA, LA, HI, LI, and combinations such as HAHI, HALI, LAHI, LALI).
  - Missing data indicated as Na.

- Context and purpose for data support
  - Data support for exploring multi-stressor effects on Daphnia magna, enabling cross-dataset integration (environmental history, life history traits, physiological responses) across three related studies (2018 Scientific Reports; 2018 Molecular Ecology; 2021 Evolutionary Applications).
  - Geographic focus: Lake Ring, Denmark; temporal range spans mid-20th to early 21st century data.
  - Data types include environmental measurements, chemical usage, life history metrics, physiological markers, and gene expression, with several variables having missing values to be considered during analysis.
  - Potential use cases: building self-serve analyses, dashboards, or reports that combine environmental history with organism responses to multiple stressors; cross-referencing pesticide usage with ecological and physiological outcomes.