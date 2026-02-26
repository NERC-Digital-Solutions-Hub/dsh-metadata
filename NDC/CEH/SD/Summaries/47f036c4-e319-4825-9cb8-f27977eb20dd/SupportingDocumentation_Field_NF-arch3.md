# Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

## Overview
- Examines how chronic radiation exposure affects development, reproduction, and genetic diversity in Asellus aquaticus from Chernobyl-affected areas (Belarus and Ukraine).
- Integrates morphological, reproductive, environmental, dose-rate, and genetic data across multiple time points to assess long-term impacts along a contamination gradient.
- Data generated under the TREE project; intended to inform environmental monitoring and policy decisions.

## Key environmental health measures and indicators
- Developmental stability: fluctuating asymmetry (FA2) across five morphological traits, calculated as [|R−L|/(R+L)/2] using micrometre measurements.
- Reproductive capacity: fecundity metrics including number of eggs, egg weight, female weight, eggs per weight, and proportion of gravid females.
- Contaminant exposure: dose rate (µGy/hr) at sampling sites, with environmental factors (conductivity, oxygen saturation, pH, temperature) recorded.
- Environmental context: site-level measurements of conductivity (µS/cm), oxygen saturation (%), pH, temperature (°C), and dissolved oxygen where applicable.
- Temporal and spatial comparison: data from 2003–2005 and 2015–2016 across six sites along a contamination gradient.
- Genetic diversity: genotyping-by-sequencing (GBS) derived metrics including inbreeding coefficient, expected and observed heterozygosity, Tajima’s D, and nucleotide diversity.

## Datasets and what they contain
- FA_Data_Chernobyl_2015.csv
  - Morphological data for A. aquaticus from Belarus and Ukraine (2015).
  - Five morphological traits; FA2 computed; includes dose rate, environmental variables, and antennal segment data.
  - 10 data columns; 394 individuals with 3988 measurements; blanks indicate missing data.
  - Methods: blinded replication, Leica imaging, ImageJ analysis; dose rates via deposition data and ERICA-based calculations.
- Fecundity_Data_Chernobyl.csv
  - Reproductive data for six lakes (Belarus/Ukraine) across 2015/2016.
  - Metrics: eggs, egg weight, female weight, eggs per female weight, sampling date, dose rate, gravid proportion.
  - 9 data columns; provides a reproductive profile across contamination gradients.
  - Methods: sexing by pleopods, weighing, imaging eggs, calculating brood metrics.
- FA_Data_Chernobyl_2003.CSV
  - Morphological data for 2003–2005 collections (Belarus/Ukraine) with FA2 and related site metadata.
  - 11 data columns; includes dose rate, number of antennal segments, and multiple environment parameters (temperature, pH, conductivity, oxygen saturation, etc.).
  - Enables temporal comparison of developmental stability across time points.
- Chernobyl_Genetic_Diversity.csv
  - Genetic diversity data for A. aquaticus from 2003–2005 and 2015.
  - Genotyping-by-sequencing (GBS) data analyzed with UNEAK/TASSEL; diversity statistics (inbreeding, heterozygosity, Tajima’s D, nucleotide diversity).
  - 6 data columns: Sample ID, Inbreeding Coefficient, Expected Heterozygosity, Observed Heterozygosity, Tajima’s D, Nucleotide Diversity.
- Sampling and sites
  - Six sampling sites across Belarus and Ukraine; site locations illustrated (Figure S1).
  - Environmental context and dose-rate data linked to each site to characterize exposure gradients.

## Methods and data collection approaches
- Sampling design
  - A. aquaticus collected from Chernobyl-affected areas along a contamination gradient.
  - Samples distributed in randomly coded boxes to minimize bias.
- Morphological measurements
  - Five traits dissected, mounted, and measured; two replicate measurements per individual (blind).
  - FA2 calculated for developmental stability; measurements captured via Leica camera and ImageJ.
- Reproductive assessments
  - Sexing by pleopod analysis; eggs removed, photographed, and weighed; brood metrics calculated; gravid rate computed.
- Environmental and dose-rate characterization
  - Environmental parameters measured with a HANNA multiparameter probe.
  - Dose rates calculated from radiocaesium/strontium deposition data (2003) and lake-water activity concentrations; ERICA tool used for dose estimation.
- Genetic analyses
  - DNA extraction from samples; GBS workflow with PstI digestion, barcoding, and Illumina sequencing.
  - Bioinformatics via UNEAK and TASSEL; diversity statistics computed with VCFtools and PopGenome.

## Temporal and geographic scope
- Timeframes: 2003–2005 and 2015–2016 (where data exist).
- Geography: six sites across Belarus and Ukraine within Chernobyl-affected zones.
- Purposefully structured to enable temporal (2003–2005 vs 2015–2016) and spatial gradient analyses of radiation effects.

## Data structure and metadata considerations
- Datasets vary in column count and types (morphology, reproduction, environment, dose, genetics).
- Some fields are blanks where data were unavailable, reflecting real-world data gaps.
- Supporting figure (Figure S1) maps site locations, reinforcing spatial context for monitoring.
- Documentation references established methods and prior studies (e.g., Fuller et al. 2017) for dose-rate calculations.

## Implications for monitoring frameworks
- Demonstrates integration of multiple, complementary indicators (morphology, reproduction, genetics, environment, dose rates) to monitor chronic radiation impacts.
- Supports temporal tracking and gradient analysis to inform policy on environmental health and radiation risk assessment.
- Highlights data governance and metadata needs for monitoring:
  - Importance of standardized data collection and clear data provenance.
  - Need for accessible, well-documented metadata to enable data sharing and reuse.
  - Challenges related to data gaps, missing values, and cross-dataset comparability.
- Provides a model for combining field measurements with advanced genetic analyses to assess ecosystem resilience and developmental stability under contaminant stress.