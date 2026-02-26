# Dataset Descriptions for Cambronero et al. on Daphnia under Multiple Stressors

## Overview
- The document describes three datasets used in studies by Cambronero et al. addressing the impact of multiple stressors on Daphnia magna, with data spanning paleolimnological records, historical insecticide usage, and controlled laboratory experimentation.
- The datasets combine environmental, chemical, life-history, physiological, and gene expression data collected from Lake Ring, Denmark (geographic coordinates provided) and across multiple experimental treatments.
- Treatments focus on combinations of temperature, food availability, and insecticide Carbaryl, enabling analysis of single versus multiple stressor effects.
- Data include both historical/paleolimnological data and modern laboratory results, with frequent mention of missing data (Na or empty cells) and the need for consistent metadata.

## Dataset 1
- a) Cambronero_etal_Environmental_metadata.csv: Paleolimnological and historical data for Lake Ring sediment cores. For each radiometrically dated year, nine variables are included: Daphnia magna ephippia count, Cladocera assemblage, carbamate insecticides, Loss on Ignition (LOI), Secchi transparency, total nitrates (TN), total phosphates (TP). Missing data are marked as Na. Transparency, TN, and TP data are available for 1971–1999.
- b) Cambronero_etal_pesticides.csv: Insecticide sales data by Danish county from 1955–2010 (tons/year). Carbaryl highlighted as the relevant insecticide for this study.
- c) Cambronero_etal_life_history_traits_sr.csv: Life-history traits (Mortality, size at maturity, age at maturity, fecundity) per IndividualID and PopulationID across three common garden experiments (CGE1–CGE3). Experimental conditions include temperature (18°C, 24°C), two food levels (0.2 mg C/L and 2.4 mg C/L), and two Carbaryl concentrations (4 μg/L and 10 μg/L). Includes maternal-effect controls; notes on experimental exposure combinations (e.g., T18, T24, TFH18, TFL18, etc.). Missing data are indicated with Na.

## Dataset 2
- d) Cambronero_etal_CTmax_bodysize.csv: 22 columns detailing CTmax (temperature of maximum tolerance) and body size for 30 Daphnia magna genotypes. Data collected after exposure to temperature alone (CGE1) and in combination with food levels (CGE2) or Carbaryl (CGE3). Experimental temperatures: 18°C and 24°C; nutrient levels: 0.2 mg C/L and 2.4 mg C/L; Carbaryl concentrations: 4 μg/L and 10 μg/L. Empty cells represent missing data.
- e) Cambronero_etal_Hb.csv: Total haemoglobin content (µmol/L) for the 30 genotypes at control temperature (20°C) and after hyper-thermal stress (30°C). Columns include Genotype ID, Population ID, average Hb across three replicates, and log2 fold change between the two temperatures.
- f) Cambronero_etal_HSP_expression.csv: 27 columns describing log2 fold-change expression of four heat-shock proteins (HSP20, HSP60, HSP70, HSP90). Expression measured on genotypes after temperature ramping (TR) and on the same genotypes not exposed to TR, under single stress (warming), warming with food limitation, and warming with Carbaryl insecticide. Missing values are indicated by empty cells.

## Dataset 3
- g) Cambronero_etal_Environmental_data.csv: Paleolimnological and historical data from Lake Ring (same location as Dataset 1). Carbaryl usage (tons/year) drawn from Danish national archives for 1955–2010; LOI measured from sediment subsamples; ephippia of D. magna harvested from sediment and hatched under standardized laboratory conditions. Missing data are indicated as Na.
- h) Cambronero_etal_life_history_traits_eva.csv: Life-history traits by IndividualID and PopulationID across experiments, with columns for Experiment, Treatment, Mortality day, Mortality event, Age at maturity, Fecundity, and Size at maturity. Fully factorial design with two algae concentrations (low: 0.2 mg C/L; high: 2.4 mg C/L) and two insecticide concentrations (low: 4 μg/L; high: 10 μg/L). Includes both single-stressor and dual-stressor combinations (e.g., HA, LA, HI, LI, HAHI, HALI, LAHI, LALI). Missing data indicated as Na.

## Metadata and data governance
- Datasets integrate historical records, paleolimnological measures, and controlled experiments, with clear treatment definitions, sampling contexts, and genotype/population identifiers.
- Missing data are explicitly marked, underscoring the need for complete metadata to enable cross-study comparability.
- Data provenance includes publication links and standardized laboratory conditions, facilitating reproducibility and secondary analyses.

## Implications for monitoring frameworks
- Demonstrates how to construct comprehensive environmental monitoring datasets by combining historical/environmental context with controlled experimental results and genetic/physiological measures.
- Highlights the importance of rich metadata (treatment definitions, units, soil/ Sediment context, geographic coordinates) and the management of missing data.
- Illustrates a layered approach to monitoring multiple stressors across temporal scales (paleodata) and experimental scales (lab-based assays), informing policy decisions and future monitoring designs.
- Emphasizes data sharing, standardization of variables and units, and the need to address data governance barriers such as access, silos, and metadata completeness to maximize reuse in monitoring frameworks.