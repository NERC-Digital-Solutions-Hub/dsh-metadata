# Supporting Documentation Impacts of chronic radiation exposure on reproduction, development and genetic diversity of the freshwater crustacean Asellus aquaticus at Chernobyl

- This document describes a set of datasets collected around Chernobyl to assess developmental stability, reproduction, and genetic diversity in Asellus aquaticus under chronic radiation exposure.
- Key projects and data sources are tied to the TREE project and involve collaboration with Belarusian and Ukrainian scientists, with data generated and analysed primarily by Neil Fuller and colleagues.

## Datasets and their purpose

- FA_Data_Chernobyl_2015.csv
  - Morphological data from Asellus aquaticus collected in 2015 from six sampling sites in Belarus and Ukraine with varying radiation contamination.
  - Purpose: compute fluctuating asymmetry (FA2) as a metric of developmental stability across contamination gradients.
  - Data features: 10 columns including site, sex, morphological trait, FA2, environmental/dose measures (dose rate in µGy/hr, conductivity, oxygen saturation, pH, temperature), and count of antennal segments.
  - Measurements: 2 replicate blind measurements per individual; total of 3988 measurements from 394 organisms.
  - Dose rates calculated from radiocaesium/strontium deposition and lake-water activity (ERICA-based).
  - Method reference: Fuller et al. 2017; full methods described in supporting documentation.

- Fecundity_Data_Chernobyl.csv
  - Reproductive data for Asellus aquaticus from six Belgian/Ukraine lakes across 2015 and 2016.
  - Purpose: assess reproductive capacity under chronic radiation exposure.
  - Data features: 9 columns including eggs per female, egg weight, female weight, site, year, eggs normalized to female weight, sampling date, dose rate, and proportion of gravid females.
  - Procedures: sexing by pleopod analysis; eggs removed, photographed, and weighed; brood size estimated from images.
  - Notes: Blank cells indicate missing data.

- FA_Data_Chernobyl_2003.CSV
  - Morphological data analogous to the 2015 FA dataset but from 2003–2005 collections (Belarus/Ukraine).
  - Purpose: trace changes in fluctuating asymmetry over time in relation to chronic radiation exposure.
  - Data features: 11 columns including site, morphological trait, FA2, dose rate, antennal segment count, sampling date, temperature, pH, conductivity, oxygen saturation, and additional parameters (e.g., dissolved oxygen, total hardness).
  - Collection/processing: similar approach to 2015 dataset; field collection by Belarusian scientists; environmental data via multiparameter probe.

- Chernobyl_Genetic_Diversity.csv
  - Genetic diversity data for Asellus aquaticus from Chernobyl-affected areas across 2003–2005 and 2015.
  - Purpose: first assessment of genetic diversity following chronic radiation exposure.
  - Data features: 6 columns including Sample ID, Inbreeding Coefficient, Expected Heterozygosity, Observed Heterozygosity, Tajima's D, Nucleotide Diversity.
  - Methods: Genotyping-by-sequencing (GBS) performed at Cornell University; DNA extraction, restriction enzyme digestion, barcoding, sequencing; analyses with UNEAK/TASSEL and PopGenome in R.
  - Collaborations: samples collected by Neil Fuller and Liubov Nagorskaya; data interpretation by Fuller; data generated under the TREE project.

## Data collection context and methods

- Sampling design: Asellus aquaticus collected from multiple sites along a contamination gradient at Chernobyl in Belarus and Ukraine (sites mapped in Figure S1).
- Measurements and analyses:
  - Morphology: dissection, slide mounting, microscopy, and ImageJ-based measurements; replicate blind measurements.
  - Environmental metrics: dose rates estimated from deposition data and water measurements; environmental variables recorded (conductivity, oxygen saturation, pH, temperature, etc.).
  - Reproduction: adult sexing, brood assessment, egg metrics, and gravid female proportion calculations.
  - Genetics: DNA extraction, GBS library preparation, sequencing, and diversity statistics (heterozygosity, Tajima’s D, etc.).

## Data structure and variables (high-level)

- FA data (2015 and 2003–2005): site, sex, morphological trait, fluctuating asymmetry (FA2), dose rate, conductivity, oxygen saturation, pH, temperature, number of antennal segments, and related measurements.
- Fecundity data: eggs, egg weight, female weight, site, year, eggs per weight, sampling date, dose rate, proportion gravid.
- Genetic diversity data: sample ID, inbreeding coefficient, expected heterozygosity, observed heterozygosity, Tajima’s D, nucleotide diversity.

## Data governance, access, and quality considerations for Data Leaders

- Data provenance and lineage: data generated under the TREE project; multiple authors and institutions; clear assignment of data collection and analysis responsibilities.
- Metadata completeness: detailed descriptions of methods, sampling sites, and environmental measures provided; but some data fields are blank where data was unavailable (noted in FA and related datasets).
- Standardization and compatibility: analogous measurement approaches across years (2003–2005 vs 2015) with similar variables; differences in available environmental variables between datasets (e.g., 11-column vs 10-column structures).
- Discoverability and discoverable metadata: datasets are named and described with key variables and methods; location and site information referenced with figure panels (Figure S1) for context.
- Access implications: data reach across two countries and includes environmental and genetic data; potential access considerations due to cross-institution data sharing and older data formats.
- Data quality and gaps: missing values indicated; older datasets (2003–2005) may have different metadata depth; measurement replicates and quality control described for morphological data.

## Relevance, reuse potential, and recommendations for data strategy

- Cross-study analyses: the combination of morphological, reproductive, environmental, and genetic data across time (2003–2005 and 2015) enables temporal trends in developmental stability, reproduction, and genetic diversity under radiation exposure.
- Useful for policy and scientific communities interested in ecological impact of chronic radiation, developmental biology, and population genetics.
- Data stewardship recommendations:
  - Maintain alignment of variable definitions across years to support longitudinal analyses (e.g., FA2 calculation formula and units).
  - Improve metadata completeness for any blanks, and document any data processing steps beyond those described.
  - Ensure clear data access pathways and licensing to facilitate reuse while respecting institutional restrictions.
  - Consider creating a data dictionary and a unified schema to enable easier cross-dataset joins (e.g., linking sites, dose rates, and environmental metrics with genetic samples).

## Stakeholders and provenance

- Principal investigators and data collectors: Neil Fuller, Liubov L. Nagorskaya, Dmitri I. Gudkov, Alex T. Ford, and Jim T. Smith; TREE project coordinators.
- Data processing and analysis: ImageJ measurements, ERICA dose-rate calculations, GBS sequencing and population-genetics analyses.
- Institutions involved: University of Portsmouth, Belarusian Academy of Sciences, Ukrainian collaborators, Cornell University's Genomic Diversity Facility, and associated researchers.