# Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

## Overview
- A multi-dataset study assessing how chronic radiation exposure affects development (fluctuating asymmetry), reproduction, and genetic diversity in Asellus aquaticus from Chernobyl-contaminated areas in Belarus and Ukraine.
- Timeframes covered: 2003–2005 and 2015 (with 2015/2016 follow-up sampling in some datasets).
- Key metrics across datasets:
  - Morphological development: fluctuating asymmetry (FA2) across multiple traits.
  - Reproduction: fecundity measures, including egg numbers, egg weights, gravid female proportion, and normalization by female weight.
  - Genetics: population-level diversity metrics from genotyping-by-sequencing (GBS), including heterozygosity and Tajima’s D.
- Sampling design includes six sites along a contamination gradient; environmental context (dose rate and water quality) collected alongside biological data.
- Data collection and analysis were conducted under the TREE project and related funding; methods include blinded measurements, image-based morphometrics, and standardized environmental measurements.

## Datasets

- FA_Data_Chernobyl_2015.csv
  - Purpose: Morphological data to calculate fluctuating asymmetry (FA2) in 2015 sampling.
  - Columns (10): Site of collection, Sex, Morphological trait analysed, Fluctuating Asymmetry (FA2), Dose rate (µGy/hr), Conductivity (µS/cm), Oxygen saturation (%), pH, Temperature (°C), Number of antennal segments.
  - Notes: Measurements are means of two independent measurements; samples from Belarus and Ukraine; figure S1 maps sampling sites.
  - Data context: Environmental dose rates and morphological stability along a radiation gradient; 3988 measurements on 394 individuals.

- Fecundity_Data_Chernobyl.csv
  - Purpose: Reproductive capacity data for Asellus aquaticus across six lakes in Belarus/Ukraine (2015/2016).
  - Columns (9): Number of eggs, weight of eggs (mg), female weight (mg), site of collection, year of collection, eggs per female weight, sampling date, dose rate (µGy/hr), proportion of gravid females.
  - Notes: Eggs photographed and counted from marsupium; gravid proportion calculated as egg-bearing females relative to total adult females (>3 mm).
  - Data context: Insight into how chronic radiation exposure influences fecundity and reproductive effort.

- FA_Data_Chernobyl_2003.CSV
  - Purpose: Morphological data to compare fluctuating asymmetry (FA2) during 2003–2005 with 2015 data.
  - Columns (11): Site of collection, Morphological trait analysed, Fluctuating Asymmetry (FA2), Dose rate (µGy/hr), Number of antennal segments, Sampling Date, Temperature (°C), pH, Conductivity (µS/cm), Oxygen saturation (%), Dissolved Oxygen (mg/L), Conductivity (µS/cm) and Total hardness (mmol/L) [note: list shows 11 columns with environmental and trait data; includes both site-level and condition measurements].
  - Data context: Enables temporal comparisons of developmental stability across time points; environmental context accompanies morphological data.

- Chernobyl_Genetic_Diversity.csv
  - Purpose: Genetic diversity metrics from Asellus aquaticus at Chernobyl-contaminated sites for 2003–2005 and 2015.
  - Columns (6): Sample ID, Inbreeding Coefficient, Expected Heterozygosity, Observed Heterozygosity, Tajima's D, Nucleotide Diversity.
  - Data context: Genotyping-by-sequencing (GBS) data generated at Cornell; 12 individuals across 6 sites analyzed for SNP diversity; provides population-genetic context to radiation effects on genetic health.

## Data collection and methods

- Sampling and bias reduction:
  - Samples collected in randomly coded boxes to prevent bias.
  - Six sites mapped in Figure S1 along a contamination gradient.
- Morphological measurements:
  - Four morphological traits dissected, mounted, flattened, photographed with Leica DFC310, and measured with ImageJ.
  - Two replicate blind measurements per individual; total of 3988 measurements on 394 organisms (2015 dataset).
- Fluctuating asymmetry:
  - FA2 calculated as FA2 = Mean[|R−L| / ((R+L)/2)], with R and L in micrometres.
- Dose rate and environmental data:
  - Dose rates estimated from radiocaesium/strontium deposition and lake-water activity (2003 data) using ERICA tool.
  - Environmental parameters measured with a HANNA 9828 multiparameter probe (conductivity, oxygen saturation, pH, temperature, etc.).
- Reproductive data collection:
  - Sexing by pleopod analysis; weights measured with precision scales; embryos removed, photographed, and eggs counted.
  - Egg numbers normalized by female weight to derive standardized reproductive metrics.
- Genetic data:
  - DNA extraction from 12 individuals across 6 sites (2003 samples) using DNeasy kits; GBS library construction with PstI digestion; sequencing on Illumina platform.
  - Bioinformatics: UNEAK pipeline and TASSEL for SNP discovery; heterozygosity statistics via VCFtools; diversity metrics with PopGenome in R.
- Provenance:
  - Data generated under the TREE project funded by NERC, Environment Agency, and Radioactive Waste Management; data interpretation led by Neil Fuller and collaborators.

## Data structure and accessibility

- Missing data:
  - Blank cells indicate unavailable data in respective fields or columns.
- Data organization:
  - Each dataset uses clearly labeled columns describing site, traits, environmental variables, and timepoint.
- Scale and units:
  - Dose rate: micrograys per hour (µGy/hr); environmental variables in standard SI-like units (temperature °C, pH, conductivity µS/cm, etc.).
- Spatial context:
  - Six sampling sites along a gradient of radiation exposure; site locations depicted in Figure S1.

## Purpose, provenance and intended use

- Primary aim: assess the impact of chronic radiation exposure on developmental stability, reproductive capacity, and genetic diversity in aquatic crustaceans at Chernobyl.
- Data provenance:
  - Grounded in the TREE project; multiple years enable temporal comparisons.
  - Data intended to support correlations between dose rate and morphological/reproductive/genetic responses, controlling for environmental covariates.

## Analytical opportunities for data-driven insights

- Developmental stability analyses:
  - Examine the relationship between dose rate and FA2 across sites and years; assess whether higher radiation correlates with increased developmental instability.
- Reproductive ecology:
  - Model how dose rate and site conditions influence fecundity measures (eggs per female weight, gravid proportion) and potential trade-offs with environmental factors.
- Temporal comparisons:
  - Compare 2003–2005 data with 2015/2016 data to infer long-term trends in developmental stability and reproduction under chronic exposure.
- Genetic diversity and population structure:
  - Use genetic diversity metrics to explore whether radiation exposure is associated with changes in heterozygosity, inbreeding, Tajima’s D, and nucleotide diversity over time and across sites.
- Integrated analyses:
  - Combine morphometric, reproductive, environmental, and genetic data to build predictive models of organismal responses to varying dose rates, incorporating site-specific covariates (temperature, pH, DO, conductivity, etc.).

## Key references and context

- Data generated under the TREE project; methodologies tied to Fuller et al. and related work.
- Related published methods include the 2017 Science of the Total Environment article detailing dose-rate calculations and developmental stability assessments.