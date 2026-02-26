# Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

## Overview
- Assess the effects of chronic radiation exposure on developmental stability, reproduction, and genetic diversity of Asellus aquaticus from Chernobyl-affected sites in Belarus and Ukraine.
- Data span two timeframes (2003–2005 and 2015–2016) and include morphological, reproductive, environmental, and genetic information.
- Generated under the TREE project to monitor environmental health and policy-relevant outcomes.

## Datasets
- FA_Data_Chernobyl_2015.csv
  - Morphological data for five traits; fluctuating asymmetry FA2 calculated as |R−L|/(R+L)/2; includes dose rate and environmental factors; 10 columns.
- Fecundity_Data_Chernobyl.csv
  - Reproductive metrics (eggs, egg weight, female weight, gravid proportion) across sites/years; 9 columns.
- FA_Data_Chernobyl_2003.CSV
  - Morphological data (same concept as 2015 FA data) from 2003–2005; includes additional columns (11 total).
- Chernobyl_Genetic_Diversity.csv
  - Genetic diversity metrics from Genotyping-by-Sequencing (SNP-based); inbreeding coefficient, expected/observed heterozygosity, Tajima's D, nucleotide diversity; 6 columns.

## Methods
- Field and sample handling
  - Samples collected from six sites along a radiation contamination gradient; boxes coded to prevent bias.
  - Sex determined via pleopods; individuals measured and analyzed in the lab.
- Morphology and developmental stability
  - Four morphological characters measured per individual; slides prepared and imaged; two replicate blind measurements per individual (total of 3988 measurements on 394 organisms).
  - FA2 calculated as described above; environmental dose rates derived from deposition data and lake water activity using the ERICA tool.
- Reproduction
  - Embryos removed from marsupium, photographed, and eggs counted; gravid proportion calculated as eggs-bearing females per total adult females.
- Environment and dose rates
  - Measurements include temperature, pH, conductivity, oxygen saturation, and other factors; dose rates reported in µGy/hr.
- Genetics (GBS)
  - DNA extracted, digested with PstI, barcoded adapters added, PCR amplified, and Illumina sequencing performed.
  - Bioinformatics (UNEAK, TASSEL) used to call SNPs; diversity statistics computed with VCFtools and PopGenome.
- Quality and completeness
  - Blank cells indicate missing data; methods and QA steps are described for reproducibility.

## Data Structure (key columns)
- FA_Data_Chernobyl_2015.csv: site, sex, morphological trait, FA2, dose rate, conductivity, oxygen saturation, pH, temperature, number of antennal segments.
- FA_Data_Chernobyl_2003.CSV: site, morphological trait, FA2, dose rate, number of antennal segments, sampling date, temperature, pH, conductivity, oxygen saturation, total hardness.
- Fecundity_Data_Chernobyl.csv: eggs, eggs weight, female weight, site, year, eggs per female weight, sampling date, dose rate, proportion gravid.
- Chernobyl_Genetic_Diversity.csv: sample ID, inbreeding coefficient, expected heterozygosity, observed heterozygosity, Tajima's D, nucleotide diversity.

## Sampling Sites and Temporal Coverage
- Six sites across Belarus and Ukraine along a contamination gradient.
- Time periods:
  - 2003–2005: FA data (morphology) and site information.
  - 2015–2016: FA data, fecundity data, with site information shown in Figure S1 (top row for 2015/2016; bottom row for 2003–2005).

## Purpose and Implications for Monitoring
- Provides standardized, comparable data to monitor environmental health indicators across time and sites.
- Enables analysis of relationships between radiation exposure (dose rates) and developmental stability, reproductive output, and genetic diversity.
- Supports long-term environmental monitoring, data integration, and evidence-based policy assessment through the TREE project framework.

## Data Provenance and Access
- Primary collection by Neil Fuller (2015) and Liubov L. Nagorskaya (2016 for Belarus) with analyses at the University of Portsmouth.
- Data generated under the TREE project funded by NERC, the Environment Agency, and Radioactive Waste Management.
- Data summarized in CSV datasets; figures (including S1) illustrate sampling locations.