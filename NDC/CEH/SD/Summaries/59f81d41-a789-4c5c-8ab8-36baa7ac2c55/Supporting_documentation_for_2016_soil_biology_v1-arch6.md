# Details of data structure to ' CINAg_soil_biology_data_2016_v2.csv '

## Overview
- Dataset: 92 columns, 324 rows
- Source: Grassland fertiliser trial 2016
- Purpose: Structure of soil biology data for analysis and data products

## Dataset structure and key variables
- Experiment: Inorganic fertilizer experiment
- Sample_ID: unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
- Year: year samples were taken
- Site: farm platform/site
- platform: NW (North Wyke), HF (Henfaes Farm), EB (Easter Bush)
- Sampling_date: date of sampling (dd/mm/yyyy)
- Sampling_time: T0, T1, T2 (time points)
- Plot: 1–16
- Treatment: C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate)
- Depth_cm: 0–15 cm, 15–30 cm, 30–60 cm
- Repeat: 0, 1, or 2

## Molecular and sequencing metrics
- DNA_qubit_ng_per_ul: DNA concentration by Qubit (ng/µl)
- DNA_260_280_ratio: DNA purity (A260/280)
- DNA_260_230_ratio: DNA purity (A260/230)
- DNA_conc_ng_per_g_soil: DNA concentration per gram of dry soil

## Microbial gene copies per gram soil
- X16S_bact_copy_per_g_soil: bacterial 16S gene copies
- X16S_arch_copy_per_g_soil: archaeal 16S gene copies
- AOA_copy_per_g_soil: ammonia-oxidising archaea gene copies
- AOB_copy_per_g_soil: ammonia-oxidising bacteria gene copies
- ureC_copy_per_g_soil: ureC gene copies
- nirS_copy_per_g_.soil: nirS nitrite reductase gene copies
- nirK_copy_per_g_soil: nirK nitrite reductase gene copies
- nosZI_copy_per_g_soil: nosZI nitrous oxide reductase gene copies
- nosZII_copy_per_g_soil: nosZII nitrous oxide reductase gene copies
- nifH_copy_per_g_soil: nifH nitrogen fixation gene copies
- Fungi_ITS_copy_per_g_soil: fungal ITS gene copies

## Ratios
- AOA_AOB_ratio: ammonia-oxidising archaea to bacteria ratio
- nirK_nirS_ratio: nirK to nirS nitrite genes ratio
- nosZI.nosZII: ratio of nosZI to nosZII nitrite genes
- nirS_K.nosZI_II: ratio of nirS:nirK to nosZI:nosZII nitrite genes

## Diversity metrics
- div16s.tot: richness of bacterial 16S genes (amplicon sequencing)
- div16s.shan: Shannon diversity (16S)
- divFun.tot: richness of fungal ITS (amplicon sequencing)
- divFun.shan: Shannon diversity (fungal ITS)

## Taxonomic abundance (phylum-level)
- p__ entries: percentage frequency of bacterial phyla within sample reads (up to 10,000 reads per sample)
- Includes many phyla (e.g., Caldithrix, Thermi, Acidobacteria, Actinobacteria, Bacteroidetes, Firmicutes, Proteobacteria, Cyanobacteria, Chloroflexi, and numerous others)
- Note: formatting irregularities visible in the source (some lines broken or showing “OP11” placeholders, e.g., p__SR1, p__Synergistetes, p__Tenericutes, etc.), indicating potential data import or naming caveats

## Provenance and usage
- Supplement to: Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Describes data structure for CINAg_soil_biology_data_2016_v2.csv
- Facilitates data exploration, self-service analysis, and integration with other datasets

## Practical notes for data support
- Useful for analyzing fertilizer treatment effects on microbial gene abundances, diversity indices, and phylum-level community composition across sites, plots, depths, and time points
- Be mindful of potential header/name formatting issues and phylum naming irregularities during data cleaning
- Acts as a foundation for creating data products (dashboards, reports) and for informing data creation and sharing practices