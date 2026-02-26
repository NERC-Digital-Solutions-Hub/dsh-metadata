# Introduction

- This document describes three datasets linked to studies on Daphnia magna from Lake Ring, Denmark, focusing on historical environmental context and responses to multiple stressors (temperature, food, and chemical insecticides).
- All datasets are provided as CSV files and include a mix of paleolimnological, environmental, life-history, physiological, and gene-expression data. Several fields have missing values marked as Na or blank.
- Geographic focus is centered on Lake Ring (55°57′51.83″N, 9°35′46.87″E) with supplementary Danish pesticide usage data by year and location.

## Datasets at a glance

- Dataset 1: three CSV files linked to the 2018 Scientific Reports paper
  - Environmental metadata: sedimentary records for Lake Ring including ephippia counts, Cladocera, carbamate insecticides, LOI, Secchi depth, total nitrates (TN), total phosphates (TP); years 1971–1999 for transparency, TN, TP.
  - Pesticides: list of insecticides sold in Denmark (1955–2010) with total amounts by year; carbaryl highlighted.
  - Life-history traits (SR): measurements across eight columns for individuals, populations, and experimental exposures (mortality, size at maturity, age at maturity, fecundity) under different CGEs and conditions (temperatures 18°C/24°C; food 0.2 vs 2.4 mg C/L; Carbaryl 4 vs 10 μg/L).
- Dataset 2: three CSV files linked to the 2018 Molecular Ecology paper
  - CTmax and body size (CTmax_bodysize): 22 columns for 30 genotypes under temperature alone (CGE1) and with food (CGE2) or Carbaryl (CGE3); temperatures 18°C/24°C; nutrients 0.2/2.4 mg C/L; Carbaryl 4/10 μg/L; missing data indicated.
  - Haemoglobin (Hb): total Hb content (µmol/L) in 30 genotypes at control (20°C) and after hyper-thermal stress (30°C); includes genotype ID, population ID, mean Hb, and log2 fold-change between temperatures.
  - HSP expression: 27 columns detailing log2 fold changes in four heat shock proteins (HSP20, HSP60, HSP70, HSP90) under warming alone, warming with food limitation, and warming with insecticide exposure; data from genotypes with and without temperature ramping (TR); includes empty cells for missing values.
- Dataset 3: two CSV files linked to the 2021 Evolutionary Applications paper
  - Environmental data: paleolimnological and historical Lake Ring data including Carbaryl usage (tons/year, 1955–2010), LOI, ephippia density, and hatching conditions; Na for missing values.
  - Life-history traits – eva: per IndividualID and PopulationID, Experiment and Treatment, life-history metrics (Mortality day, Mortality event, Age at maturity, Fecundity, Size at maturity); factorial design with two algae levels (low 0.2 mg C/L and high 2.4 mg C/L) and two insecticide levels (low 4 μg/L and high 10 μg/L), evaluating single vs. combined stressors (HA/LA/HI/LI and HAHI/HALI/LAHI/LALI); Na for missing data.

## Key variables and measures

- Paleolimnological and water quality indicators: ephippia counts, Cladocera assemblage, LOI, Secchi depth, TN, TP; LOI and Secchi depth as proxies for past water quality.
- Pesticide exposure: Carbaryl presence and amounts by year; geographic/temporal distribution in Denmark.
- Life-history and fitness traits: mortality, age at maturity, size at maturity, fecundity; measured across single and multiple stressor conditions.
- Thermal biology and physiology: CTmax, body size, haemoglobin content, and HSP gene expression under varying temperature, nutrient, and insecticide contexts.
- Experimental design: full-factorial combinations of temperature, food availability, and insecticide exposure; multiple CGEs (CGE1/2/3) and treatment regimes.

## Spatial and temporal context for GIS use

- Lake Ring, Denmark as a fixed spatial reference point for environmental and paleolimnological data.
- Spatially aggregated pesticide usage data for Denmark (county-level, 1955–2010) enabling regional visualization of chemical exposure over time.
- Temporal depth includes sedimentary records (past decades to 1999), laboratory experiments across defined temperatures and chemical/nutrient treatments, and historical insecticide usage spanning 1955–2010.
- Potential GIS visualizations:
  - Map of Lake Ring with sediment-layer derived variables (ephippia density, LOI, Secchi depth proxies) over time.
  - Time-series maps or dashboards showing regional Carbaryl usage by year across Denmark.
  - Linking genotype-level experimental results to spatial proxies when available (e.g., origin populations) and overlaying environmental context.

## Data quality and notes

- Several fields contain missing data (Na or blank cells), particularly in biological measurements and expression data.
- The datasets are linked to three major publications (Scientific Reports 2018, Molecular Ecology 2018, Evolutionary Applications 2021), providing methodological context and validation for the measurements.

## GIS-ready insights and potential visualizations

- Temporal-spatial trends of past water quality indicators and pesticide exposure around Lake Ring.
- Comparative maps of environmental drivers (pesticide usage) and biological responses (ephippia density, life-history traits) across different experimental conditions.
- Visualization of genotype-specific responses (CTmax, Hb, HSP expression) in relation to temperature and toxin exposure, with notes on data gaps due to missing values.
- Integration of paleolimnological data with modern experimental results to explore historical-backdrop effects on current fitness responses to multiple stressors.