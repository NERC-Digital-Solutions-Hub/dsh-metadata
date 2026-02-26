# Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

## Overview
- Studies the effects of chronic radiation exposure on development, reproduction, and genetic diversity of Asellus aquaticus in Chernobyl-affected areas (Belarus and Ukraine).
- Combines morphological, reproductive, environmental, and genetic data across multiple years to assess developmental stability and population robustness under radiation gradients.
- Data generated under the TREE project; outputs intended for integration and longitudinal analyses.

## Datasets and Descriptions
- FA_Data_Chernobyl_2015.csv
  - Morphological data for A. aquaticus from Chernobyl-affected sites (2015/2016 sampling).
  - 10 columns including Site, Sex, Morphological trait, Fluctuating Asymmetry (FA2), Dose rate (µGy/hr), Conductivity (µS/cm), Oxygen saturation (%), pH, Temperature (°C), and number of antennal segments.
  - Measurements: 3988 measurements on 394 individuals; FA2 calculated as |R−L|/(R+L)/2; two replicate blind measurements per individual; blank cells indicate missing data.
- Fecundity_Data_Chernobyl.csv
  - Reproductive data (fecundity) for A. aquaticus from six lakes across Belarus/Ukraine (2015/2016).
  - 9 columns including eggs produced, egg weight (mg), female weight (mg), site, year, eggs per female weight, sampling date, dose rate (µGy/hr), and proportion gravid females.
  - Methods: embryos counted from marsupium images; gravid status calculated from counts of egg-bearing females.
- FA_Data_Chernobyl_2003.CSV
  - Morphological data for A. aquaticus from 2003–2005 sampling at similar Chernobyl-affected sites.
  - 11 columns including Site, Morphological trait, FA2, Dose rate, Number of antennal segments, Sampling Date, Temperature (°C), pH, Conductivity (µS/cm), Oxygen saturation (%), and additional environmental parameters (e.g., Dissolved Oxygen, Total hardness).
  - Purpose: to assess changes in fluctuating asymmetry over time.
- Chernobyl_Genetic_Diversity.csv
  - Genetic diversity data from A. aquaticus at Chernobyl-affected sites (2003–2005 and 2015).
  - 6 columns: Sample ID, Inbreeding Coefficient, Expected Heterozygosity, Observed Heterozygosity, Tajima's D, Nucleotide Diversity.
  - Derived from Genotyping-by-Sequencing (GBS) with SNP-focused analyses; data processed with UNEAK/TASSEL; diversity metrics calculated with VCFtools and PopGenome.

## Methods and Data Collection
- Field sampling
  - Six sampling sites across Belarus and Ukraine; site locations illustrated in Figure S1.
  - 2003–2005 and 2015 time points to compare developmental and genetic parameters across years.
- Morphology and development
  - A. aquaticus individuals dissected; four morphological characters measured.
  - Measurements taken from slides photographed with Leica DFC310; measured in ImageJ.
  - Two replicate blind measurements per individual; total of 3988 measurements from 394 individuals (2015 dataset).
  - Fluctuating asymmetry (FA2) calculated as FA2 = Mean[|R−L|/(R+L)/2] using right/left trait measurements in µm.
- Environmental and dose-rate data
  - Environmental factors measured with HANNA 9828 multiparameter probe.
  - Dose rates estimated from radiocaesium/strontium deposition data and lake water activity concentrations (2003 data) using ERICA tool.
  - Dose rate and environmental variables aligned with each specimen/site.
- Reproduction
  - Females sexed via pleopod analysis; eggs/embryos removed, weighed; offspring metrics normalized to female weight.
  - Egg numbers and gravid status calculated from imaging; reproductive metrics include egg counts, egg weight, total brood weight, and proportion gravid.
- Genetics
  - DNA extracted from samples; GBS performed with PstI restriction, barcoded libraries sequenced (Illumina).
  - SNP data processed with UNEAK and TASSEL; heterozygosity statistics computed; additional diversity statistics in PopGenome.

## Data Structure and Key Fields
- FA_Data_Chernobyl_2015.csv: Site, Sex, Morphological trait, FA2, Dose rate, Conductivity, Oxygen saturation, pH, Temperature, Number of antennal segments.
- Fecundity_Data_Chernobyl.csv: Eggs, Egg weight (mg), Female weight (mg), Site, Year, Eggs per female weight, Sampling date, Dose rate, Proportion gravid.
- FA_Data_Chernobyl_2003.CSV: Site, Morphological trait, FA2, Dose rate, Number of antennal segments, Sampling Date, Temperature, pH, Conductivity, Oxygen saturation, (and additional environmental parameters such as Dissolved Oxygen, Total hardness).
- Chernobyl_Genetic_Diversity.csv: Sample ID, Inbreeding Coefficient, Expected Heterozygosity, Observed Heterozygosity, Tajima's D, Nucleotide Diversity.

## Provenance, Funding, and Access
- Principal data collection and authorship: Neil Fuller; co-authors include J.T. Smith, A.T. Ford, L.L. Nagorskaya, D.I. Gudkov.
- Funding: TREE project (NERC, Environment Agency, Radioactive Waste Management).
- Methods cross-referenced in Fuller et al. (2017) Science of the Total Environment for dose-rate calculations.
- Data availability supports cross-year comparisons and integrative analyses of developmental stability, reproduction, and genetic diversity in relation to radiation exposure.

## Opportunities for Data Support and Exploration
- Cross-dataset integration
  - Link FA2 measures with dose rates and environmental variables to map developmental stability gradients.
  - Combine fecundity metrics with site-dose data to assess radiation effects on reproductive capacity.
  - Integrate genetic diversity metrics with chronological data (2003–2005 vs 2015) to explore temporal genetic changes under radiation pressure.
- Temporal analyses
  - Compare 2003–2005 and 2015 datasets to evaluate changes in FA2, reproduction, and genetic diversity over time.
- Geographic and environmental visualization
  - Site-based dashboards showing FA2, fecundity, and genetic diversity by location and year.
  - Dose-rate vs. FA2 and reproduction metrics visualizations to identify dose-response relationships.
- Data quality and gaps
  - Acknowledge missing values (blank cells) and ensure appropriate handling in analyses.
  - Leverage two-pass measurement approach for FA to assess measurement reliability.
- Reporting and reproducibility
  - Document measurement methods (ImageJ measurements, sampling dates, environmental probes) for replicability.
  - Reference the ERICA-based dose-rate calculations when reproducing environmental exposure assessments.

## Context and Purpose
- Overall aim: provide a multi-faceted data package to assess the impacts of chronic radiation exposure on development, reproduction, and genetic diversity in a freshwater crustacean, enabling comparative and temporal analyses across sites and years.