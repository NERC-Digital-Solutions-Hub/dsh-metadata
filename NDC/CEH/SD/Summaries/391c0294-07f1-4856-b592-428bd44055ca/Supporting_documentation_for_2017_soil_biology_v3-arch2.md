# Details of data structure to CINAg_Digestate_experiment_2017_soil_biology.csv

## Overview and purpose
- Supplement to the supporting documentation for data series in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Contains data from the winter wheat digestate trial 2017, within the inorganic fertilizer experiment
- Designed for monitoring environmental health by recording soil biological indicators under different treatments and depths

## Dataset scope
- 87 columns, 180 rows
- Measures collected across plots with three treatments: C (control), D (digestate), ADNI (acidified digestate with nitrification inhibitor DMPP)
- Sampling at two time points (T1 and T2)
- Sites: NW (North Wyke) and HF (Henfaes Farm)
- Depths: 0–15 cm, 15–30 cm, 30–60 cm
- Includes both physical/chemical metadata and molecular biology metrics

## Key data categories and variables
- Experiment metadata
  - Experiment: Inorganic fertilizer experiment
  - Sample_ID: unique ID encoded as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths
  - Year, Site, Sampling_date (dd/mm/yyyy), Sampling_time (T1/T2), Plot, Treatment, Depth_cm, Repeat (0, 1 or 2)
- DNA quality and concentration
  - DNA_qubit_ng_per_µl
  - DNA_260_280_ratio (quality; protein contamination indicator)
  - DNA_260_230_ratio (quality; salt contamination indicator)
  - DNA_conc_ng_per_g_soil
- Microbial gene copy numbers per gram dry soil
  - X16S_bact_copy_per_g_soil (bacteria 16S)
  - X16S_arch_copy_per_g_soil (archaea 16S)
  - fungi_ITS_copy_per_g_soil
  - AOA_copy_per_g_soil (ammonia-oxidising bacteria)
  - AOB_copy_per_g_soil (ammonia-oxidising archaea)
  - nirS_copy_per_g_soil, nirK_copy_per_g_soil (nitrite reductase genes)
  - nifH_copy_per_g_soil (nitrogen fixation)
  - nosZI_copy_per_g_soil, nosZII_copy_per_g_soil (nitrous oxide reductase)
- Microbial diversity and richness
  - div16s.tot (bacterial 16S richness)
  - div16s.shan (Shannon index for bacterial 16S)
  - divFun.tot (fungal ITS richness)
  - divFun.shan (Shannon index for fungal ITS)
- Taxonomic composition (amplicon sequencing results; 10,000 reads per sample)
  - p__ prefixes indicate bacterial phyla; numerous phyla listed (e.g., Caldiserica, Chlamydiae, Chlorobi, Chloroflexi, Cyanobacteria, Acidobacteria, Actinobacteria, Firmicutes, Proteobacteria, Spirochaetes, Verrucomicrobia, etc.)
  - p__Unassigned and numerous specific phylum percentages
  - Some groups (e.g., OP11) and related named taxa represented with percentage frequencies
  - Note: frequencies are given as percentages of 10,000 reads (with special case for fungi/other groups described separately)

## Data format and units
- Date fields use dd/mm/yyyy format
- Depths represented in cm
- Gene copy numbers and DNA concentrations in copies per gram soil or ng per µl
- Ratios in standard quality-control units (nanodrop metrics)
- Diversity metrics as counts or index scores; percentages for phylum-level compositions

## Data provenance and quality considerations
- Derived from the winter wheat digestate trial 2017
- Sample_ID encodes traceable metadata (Year, Experiment, Site, Sampling_time, Treatment, Plot, Depths)
- Quality indicators from Qubit (DNA concentration) and Nanodrop (purity ratios)
- Amplicon sequencing outputs used for 16S (bacteria/archaea) and ITS (fungi) analyses
- Depth- and treatment-related structure enables cross-comparison over time and space

## How this supports environmental monitoring
- Provides a standardized, multi-metric view of soil microbial community structure and function under different fertilization regimens
- Facilitates temporal and spatial monitoring of soil health indicators
- Enables integration with other environmental datasets to assess policy performance and environmental health trends

## Practical considerations for analysts (Analysts Monitoring the Environment)
- Large, wide dataset (87 columns) requires careful data wrangling and cleaning
- Ensure consistent interpretation of time points (T1 vs T2) and depth categories
- Be aware of sequencing depth assumptions (10,000 reads for most taxa; 5,000 reads for fungi) when interpreting abundance percentages
- Maintain traceability via the encoded Sample_ID for audits and longitudinal analyses

## Alignment with the Analysts Monitoring the Environment archetype
- Supports data verification, quality assurance, cleaning, and standardization of environmental monitoring data
- Enables clear outputs (reports, maps, charts) illustrating microbial indicators across treatments, depths, and time
- Encourages data sharing and reuse by storing and enabling access through appropriate data portals