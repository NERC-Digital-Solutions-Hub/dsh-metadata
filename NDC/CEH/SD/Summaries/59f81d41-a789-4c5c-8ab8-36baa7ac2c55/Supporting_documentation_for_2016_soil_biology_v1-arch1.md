# Details of data structure to CINAg_soil_biology_data_2016_v2.csv

## Overview
- Supplemental documentation describing the data structure for CINAg_soil_biology_data_2016_v2.csv
- Grassland fertiliser trial data from 2016
- Dataset: 92 columns and 324 rows

## Experimental design and metadata
- Site/platform: NW (North Wyke), HF (Henfaes Farm), EB (Easter Bush)
- Sampling year: Year column indicates when samples were taken
- Sampling date and time: Sampling_date (dd/mm/yyyy) and Sampling_time (T0, T1, T2)
- Plot and treatment: Plot numbers 1–16; Treatments include C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate)
- Depths: 0–15 cm, 15–30 cm, 30–60 cm
- Replicates: Repeat values 0, 1 or 2
- Structure supports longitudinal comparisons across time, depth, treatment, and site

## Measurements and data types
- DNA metrics: 
  - DNA_qubit_ng_per_µl (concentration), DNA_260_280_ratio, DNA_260_230_ratio, DNA_conc_ng_per_g_soil
- Microbial gene copies per g soil:
  - X16S_bact_copy_per_g_soil, AOA_copy_per_g_soil, AOB_copy_per_g_soil, ureC_copy_per_g_soil
  - X16S_arch_copy_per_g_soil, nirS_copy_per_g_.soil, nirK_copy_per_g_soil
  - nosZI_copy_per_g_soil, nosZII_copy_per_g_soil, nifH_copy_per_g_soil
  - Fungi_ITS_copy_per_g_soil
- Community structure metrics:
  - AOA_AOB_ratio, nirK_nirS_ratio, nosZI.nosZII, nirS_K.nosZI_II
  - div16s.tot (bacterial 16S richness), div16s.shan (Shannon index for 16S)
  - divFun.tot (fungal ITS richness), divFun.shan (Shannon index for fungi)
- Taxonomic composition (relative abundances per sample; 10,000 reads):
  - p__<phylum> entries (e.g., p__Firmicutes, p__Proteobacteria, p__Cyanobacteria, etc.)
  - Each entry represents frequency/percentage of reads assigned to that phylum
  - Includes numerous phyla listed with “Frequency … within sample's 10,000 reads: percentage”
- Notes: The phylum list includes many standard bacterial phyla; formatting shows occasional line breaks/duplications but represents relative abundance data

## Data formatting and units
- Dates formatted as day/month/year
- Depths expressed in centimeters; depth categories correspond to 0–15, 15–30, and 30–60 cm
- Gene copy data in copies per gram of dry soil
- DNA metrics in ng/µl or nanometer-based quality ratios
- Diversity indices dimensionless (indices/score)
- Relative abundances (p__ phyla) expressed as percentages per 10,000 reads

## Potential analyses and use cases
- Assess effects of fertilizer treatments (C, U, IU, AN) on microbial community structure and function
- Examine depth- and time-dependent patterns for gene copies (AOA, AOB, nifH, etc.)
- Explore relationships between DNA quality/quantity and sequencing results
- Model outcomes with fixed effects (Year, Site, Platform, Depth, Treatment, Sampling_time) and random effects (Plot)
- Analyze relationships between diversity indices and taxonomic/functional gene abundances
- Multivariate analyses of phylum-level relative abundances to detect treatment- and depth-driven shifts

## Data quality, limitations, and challenges
- Large, multi-source dataset with 92 columns; potential formatting inconsistencies in phylum list
- Local-scale data (grassland plots) may limit generalisability beyond study sites
- Relative abundance data depend on sequencing depth and read normalization to 10,000 reads per sample
- Depth categorization may limit continuous-depth analyses unless recoded

## Metadata, provenance, and accessibility
- Supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Data series context provided by the CINAg project; enables traceability of samples via Sample_ID and associated metadata
- Designed to be discoverable and usable with metadata, supporting data integration and reproducible analyses