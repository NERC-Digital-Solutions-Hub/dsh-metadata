# This document is a supplement to the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf' Details of data structure to ' CINAg_soil_biology_data_2016_v2.csv' The dataset consists of 92 columns and 324 rows. Data from grassland fertiliser trial 2016.

## Overview
- Supplementary data description for CINAg_soil_biology_data_2016_v2.csv, detailing structure and content.
- Dataset originates from a grassland fertiliser trial conducted in 2016.
- Contains 92 columns and 324 rows of measurements.

## Dataset design and scope
- Experimental context: Inorganic fertilizer experiment.
- Sampling platforms/sites: NW (North Wyke), HF (Henfaes Farm), EB (Easter Bush).
- Temporal design: Sampling years with T0, T1, T2 timepoints across the study.
- Spatial design: Plot-level data with plots numbered 1–16; three soil depths (0–15 cm, 15–30 cm, 30–60 cm).
- Treatments: C (Control), Urea, Urea inhibitor, AN (Ammonium nitrate).
- Sample identification: Sample_ID uniquely identifies each sample (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).
- Repeats: Repeat column indicates repeated measures (0, 1, or 2).

## Measured biological and molecular variables
- DNA quality and quantity indicators: DNA_qubit_ng_per_µl, DNA_260_280_ratio, DNA_260_230_ratio.
- DNA concentration per soil mass: DNA_conc_ng_per_g_soil.
- Microbial gene copy numbers per gram of dry soil:
  - Bacteria: X16S_bact_copy_per_g_soil
  - Archaea and ammonia oxidisers: AOA_copy_per_g_soil, AOB_copy_per_g_soil
  - Functional genes: ureC_copy_per_g_soil, nirS_copy_per_g_soil, nirK_copy_per_g_soil, nosZI_copy_per_g_soil, nosZII_copy_per_g_soil, nifH_copy_per_g_soil
  - Fungi: Fungi_ITS_copy_per_g_soil
- Community structure metrics:
  - AOA_AOB_ratio (ammonia oxidisers)
  - nirK_nirS_ratio (nitrite reductase genes)
  - nosZI.nosZII (nosZ clades ratio)
  - nirS_K.nosZI_II (nirS/nirK to nosZI/nosZII ratio)
  - div16s.tot, div16s.shan (bacterial 16S richness and Shannon index)
  - divFun.tot, divFun.shan (fungal ITS richness and Shannon index)
- Taxonomic composition (amplicon-based estimates; per-sample frequencies for numerous phyla, using a 10,000 reads subset):
  - p__ (unassigned identities) and a long list of phyla such as Caldiserica, Chlamydiae, Chlorobi, Chloroflexi, Cyanobacteria, Acidobacteria, Actinobacteria, Bacteroidetes, Firmicutes, Proteobacteria, Spirochaetes, and many others (with partial line formatting issues in the source).
  - Each entry is the frequency (percentage) of the specified phylum within the sample’s 10,000 reads.
- Data-driven summaries:
  - Richness metrics for 16S and ITS from amplicon sequencing (div16s.tot, divFun.tot).

## Data structure and metadata details
- Data schema: 92 columns spanning sample metadata, DNA quality, microbial abundances (gene copies), diversity indices, functional/ratio metrics, and taxonomic composition.
- Sample metadata fields include Year, Site, platform, Sampling_date, Sampling_time, Plot, Treatment, Depth_cm, Repeat.
- Units and data types vary (e.g., ng/µl for DNA concentration, copies per g soil for gene abundances, percentages for phylum frequencies, index scores for diversity).

## Relevance to environmental health monitoring and policy
- Enables monitoring of soil microbial community structure and function under different inorganic fertilizer regimes.
- Combines molecular markers (16S/ITS, functional genes) with environmental context (depth, date, site, treatment) to support assessments of soil health and nutrient cycling under management practices.
- Provides multi-tier indicators suitable for evaluating fertilizer policies and their ecological consequences.

## Data quality, metadata, and governance considerations
- Metadata completeness and standardization are critical for comparability across studies and over time.
- The dataset description hints at formatting inconsistencies (e.g., misformatted phylum entries) that could impede automated data integration.
- Open data sharing and provenance considerations: underlying data and QA/QC processes should be clearly documented to meet governance expectations.
- Transformation and harmonization needs: phylum-level frequency data rely on a fixed read depth (10,000 reads) and require clear documentation of pipelines to ensure reproducibility.

## Practical use for monitoring frameworks
- Use as a case study for integrating microbial indicators into environmental health monitoring, policy evaluation, and decision-making about fertilizer use.
- Supports trend analysis of microbial diversity, functional potential, and community composition in response to management practices.
- Helps define data governance requirements (metadata standards, data sharing, and transparency) essential for robust monitoring frameworks.

## Limitations and cautions
- Temporal coverage is limited to the 2016 grassland fertiliser trial, which may constrain longitudinal inferences.
- Some formatting and labeling irregularities in phylum entries may require data cleaning before integration into dashboards or policy analyses.
- High-dimensional microbial data necessitate careful statistical handling and clear interpretation to inform policy without overfitting.