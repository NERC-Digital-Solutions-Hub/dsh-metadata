# Details of data structure to CINAg_soil_biology_data_2016_v2.csv

- Overview
  - Supplement to supporting documentation for data series referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Dataset: CINAg_soil_biology_data_2016_v2.csv
  - Structure: 92 columns, 324 rows
  - Source: Grassland fertiliser trial data from 2016

- Dataset scope and design
  - Field trial context: grassland fertiliser experiment conducted in 2016
  - Sites and platforms: NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush
  - Sampling framework:
    - Sampling_date: dates samples were taken (dd/mm/yyyy)
    - Sampling_time: T0, T1, T2 (timepoints; T2 at last harvest)
    - Depths: 0–15 cm, 15–30 cm, 30–60 cm
  - Experimental metadata:
    - Experiment: Inorganic fertilizer experiment
    - Sample_ID: unique identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
    - Year: sampling year
    - Site, platform, Plot (1–16)
    - Treatment: C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate)
    - Repeat: 0, 1, or 2 (repeat measurements)

- Molecular and quality metrics
  - DNA concentration and quality indicators:
    - DNA_qubit_ng_per_µl
    - DNA_260_280_ratio
    - DNA_260_230_ratio
    - DNA_conc_ng_per_g_soil
  - Target gene copies per gram dry soil (amplicon/qPCR type measurements):
    - X16S_bact_copy_per_g_soil
    - AOA_copy_per_g_soil
    - AOB_copy_per_g_soil
    - ureC_copy_per_g_soil
    - X16S_arch_copy_per_g_soil
    - nirS_copy_per_g_soil
    - nirK_copy_per_g_soil
    - nosZI_copy_per_g_soil
    - nosZII_copy_per_g_soil
    - nifH_copy_per_g_soil
    - Fungi_ITS_copy_per_g_soil
  - Community structure and relationships:
    - AOA_AOB_ratio
    - nirK_nirS_ratio
    - nosZI.nosZII (nosZI to nosZII ratio)
    - nirS_K.nosZI_II (nirS:nirK to nosZI:nosZII ratio)
  - Diversity and richness metrics:
    - div16s.tot (bacterial 16S richness from amplicon sequencing)
    - div16s.shan (Shannon index for bacterial 16S)
    - divFun.tot (fungal ITS richness from amplicon sequencing)
    - divFun.shan (Shannon index for fungal ITS)

- Taxonomic and relative abundance data
  - Amplicon sequencing-derived relative abundances (p__ prefix indicates bacterial phylum)
  - Broad panel of phyla covered (e.g., Firmicutes, Proteobacteria, Bacteroidetes, Actinobacteria, Chloroflexi, Cyanobacteria, Acidobacteria, Spirochaetes, etc.)
  - Many additional and less abundant phyla listed (e.g., p__Chlamydiae, p__Chlorobi, p__Elusimicrobia, p__OD1, p__OP11, p__WPS.2, p__WS2, p__WS3, p__WS4, p__WS6, p__WWE1, p__ZB3) with frequency values expressed as percentages per sample
  - Abundance data are reported per sample using 10,000 reads as a normalization reference in the header notes
  - Overall composition captures extensive microbial community structure alongside standard soil biology markers

- Outputs and data handling
  - Outputs are designed for standardised presentation (reports, maps, charts)
  - Dataset storage and upload to appropriate data portals are part of the workflow
  - Emphasis on ensuring datasets are accessible and reusable, supporting broader data integration

- Relevance to environmental monitoring aims
  - Enables assessment of soil microbial health and function across fertilizer treatments and depths
  - Provides standardized data to monitor environmental health and policy performance over time
  - Facilitates comparison across sites and sampling times, as well as integration with other environmental datasets

- Considerations for analysts
  - Data quality indicators included (DNA quality ratios, concentration)
  - Rich feature set supports multi-factor analyses of agricultural impact on soil microbiomes
  - Large taxonomic matrix allows exploration of community shifts in response to treatments and depth
  - Accessibility note: underlying data are intended to be accessible to support transparency and scrutiny