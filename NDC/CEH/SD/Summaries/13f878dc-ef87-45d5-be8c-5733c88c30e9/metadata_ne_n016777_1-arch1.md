# Introduction

- Overview: The document describes three datasets, each containing multiple CSV files, linked to studies on Daphnia magna and environmental stressors in Lake Ring, Denmark.
- Scope: Datasets cover paleolimnological/historical data, experimental life-history traits, thermal tolerance, haemoglobin, heat-shock protein expression, and fitness under single and multiple stressors.

## Dataset 1 (three CSV files linked to Cambronero et al. 2018, Scientific Reports)

- Cambronero_etal_Environmental_metadata.csv
  - Data type: Paleolimnological and historical records from Lake Ring sedimentary archive.
  - Contents: Radiometrically dated years with 9 columns: Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi depth (transparency), total nitrates (TN), total phosphates (TP), with Na indicating missing data.
  - Temporal coverage: transparency, TN, TP data available 1971–1999.

- Cambronero_etal_pesticides.csv
  - Data type: Insecticide usage data in Denmark.
  - Contents: List of insecticides sold 1955–2010 (tons/year); Carbaryl highlighted as the insecticide of interest in the study.

- Cambronero_etal_life_history_traits_sr.csv
  - Data type: Experimental life-history traits.
  - Contents: Eight columns including IndividualID, populationID, experimental exposure, and life-history traits (mortality, size at maturity, age at maturity, fecundity).
  - Experimental design: Three common garden experiments (CGE1: temperature; CGE2: temperature and food; CGE3: temperature and carbaryl) with settings: temperatures 18°C and 24°C; food levels 0.2 and 2.4 mg C/L; Carbaryl 4 μg/L and 10 μg/L.

## Dataset 2 (three CSV files linked to Cambronero et al. 2018, Molecular Ecology)

- Cambronero_etal_CTmax_bodysize.csv
  - Data type: CTmax and body size data.
  - Contents: 22 columns for 30 Daphnia magna genotypes; data collected after exposure to temperature alone (CGE1) and in combination with either food (CGE2) or insecticide Carbaryl loads (CGE3).
  - Experimental conditions: Temperatures 18°C and 24°C; nutrient levels 0.2 mg C/L and 2.4 mg C/L; Carbaryl concentrations 4 μg/L and 10 μg/L; empty cells indicate missing data.

- Cambronero_etal_Hb.csv
  - Data type: Haemoglobin content.
  - Contents: Hb content (µmol/L) for 30 genotypes at control temperature (20°C) and after hyper-thermal stress (30°C); includes Genotype ID, population ID, average Hb across three replicates, and log2 fold change between the two temperatures.

- Cambronero_etal_HSP_expression.csv
  - Data type: Heat-shock protein expression.
  - Contents: 27 columns describing log2 fold change of four HSPs (HSP20, HSP60, HSP70, HSP90).
  - Conditions: Measured after temperature ramping (TR) following common garden experiments; treatments include Warming alone, Warming with food limitation, and Warming with insecticideCarbaryl; missing values indicated by empty cells.

## Dataset 3 (two CSV files linked to Cambronero et al. 2021, Evolutionary Applications)

- Cambronero_etal_Environmental_data.csv
  - Data type: Paleolimnological/history for Lake Ring.
  - Contents: Carbaryl insecticide usage (tons/year) from Danish archives (1955–2010); LOI; ephippia counts (N. ephippia/m²) following hatching under standard lab conditions; coordinates and Na for missing data.

- Cambronero_etal_life_history_traits_eva.csv
  - Data type: Life-history traits under multi-stressor conditions.
  - Contents: IndividualID, PopulationID, Experiment, Treatment, and traits (mortality day, mortality event, age at maturity, fecundity, size at maturity).
  - Experimental design: Full factorial with two algae concentrations (low/high: 0.2 mg C/L and 2.4 mg C/L) and two insecticide concentrations (low/high: 4 μg/L and 10 μg/L); assesses single stress vs. pair of stressors.
  - Notes: Na indicates missing data.