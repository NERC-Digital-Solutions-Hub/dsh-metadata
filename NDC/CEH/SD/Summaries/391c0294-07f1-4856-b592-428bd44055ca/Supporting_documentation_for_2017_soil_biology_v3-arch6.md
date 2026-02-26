# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'

## Overview
- Describes the data structure of CINAg_Digestate_experiment_2017_soil_biology.csv.
- Winter wheat digestate trial 2017, inorganic fertilizer experiment.
- Dataset contains 87 columns and 180 rows.
- Focuses on soil biology measurements derived from the trial across two farms/sites.

## Dataset contents and structure
- Experiment metadata
  - Experiment: Inorganic fertilizer experiment
  - Sample_ID: unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
  - Year: year samples were taken
  - Site: farm site
  - Sampling_date: date of sampling (dd/mm/yyyy)
  - Sampling_time: time point(s) (e.g., T1, T2)
  - Plot: plot number
  - Treatment: fertilizer treatments (C = control, D = digestate, ADNI = acidified digestate with nitrification inhibitor DMPP)
  - Depth_cm: sampling depth (0-15, 15-30, 30-60 cm)
  - Repeat: replication (0, 1, or 2)

- Molecular and chemical measurements
  - DNA_qubit_ng_per_µl: DNA concentration (Qubit)
  - DNA_260_280_ratio: DNA quality (Nanodrop 260/280)
  - DNA_260_230_ratio: DNA quality (Nanodrop 260/230)
  - DNA_conc_ng_per_g_soil: DNA concentration per gram of dry soil

- Microbial gene copy numbers (per g soil)
  - X16S_bact_copy_per_g_soil; X16S_arch_copy_per_g_soil
  - fungi_ITS_copy_per_g_soil
  - AOA_copy_per_g_soil; AOB_copy_per_g_soil
  - nirS_copy_per_g_soil; nirK_copy_per_g_soil
  - nifH_copy_per_g_soil
  - nosZI_copy_per_g_soil; nosZII_copy_per_g_soil

- Diversity metrics
  - div16s.tot; div16s.shan (bacterial 16S richness and Shannon index)
  - divFun.tot; divFun.shan (fungal ITS richness and Shannon index)

- Taxonomic composition (phylum-level relative abundances)
  - p__… entries representing a broad set of bacterial phyla (e.g., Caldiserica, Chlorobi, Chloroflexi, Cyanobacteria, Firmicutes, Proteobacteria, etc.)
  - Additional aggregated or unassigned categories (e.g., p__.Caldithrix., p__SR1, OP11-related groups)
  - Values are percentages derived from sample reads (e.g., per 10,000 reads)

- Notes on data shape
  - 87 columns total; 180 rows (samples)
  - Measurements span DNA quality/quantity, microbial gene abundances, diversity indices, and community composition

## Key data types and units
- Dates and times: Sampling_date (dd/mm/yyyy)
- Depth: cm (0-15, 15-30, 30-60)
- Gene copy numbers: copies per gram dry soil
- DNA measurements: ng/µl or ng/g soil
- Diversity indices: unitless scores (Shannon index)
- Phylum abundances: percentages (per 10,000 reads)

## Context for data use
- Provides a rich, multi-dimensional view of soil biology under different inorganic fertilizer treatments in a digestate trial.
- Enables integrated analyses across:
  - Treatment effects (C vs D vs ADNI)
  - Spatial variation (Site, Depth)
  - Temporal aspects (Year, Sampling_time)
  - Molecular biology metrics (DNA quality/quantity, microbial gene abundances)
  - Community structure (diversity metrics and phylum-level composition)

## Practical considerations for data support
- Use as a data product input: combine with other datasets to build dashboards or self-serve analyses of fertilizer impacts on soil microbial communities.
- Data quality and consistency: ensure careful handling of units, date formats, and consistent interpretation of phylum labels.
- Documentation alignment: this file serves as a data-structure supplement to the broader CINAg experiment documentation; refer to the related Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf for additional context.