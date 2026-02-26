# Details of data structure to CINAg_Digestate_experiment_2017_soil_biology.csv

## Overview
- Supplement to the supporting documentation for CINAg data series.
- Dataset: winter wheat digestate trial 2017.
- Structure: 87 columns and 180 rows.

## Dataset design and structure
- Experiment context: Inorganic fertilizer experiment.
- Sites: NW = North Wyke, HF = Henfaes Farm.
- Sampling scheme: Sampling_date (dates), Sampling_time with two time points (T1 and T2).
- Plot and depth: Plot numbers; Depth_cm categories 0-15, 15-30, 30-60 cm.
- Replication: Repeat values (0, 1, or 2).
- Treatments: C = control, D = digestate, ADNI = acidified digestate with nitrification inhibitor (DMPP).

## Sample metadata fields
- Sample_ID: unique identifier constructed as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths.
- Year: year of sample collection.
- Site: farm site code (NW or HF).
- Depth_cm: soil depth interval.
- Repeat: replication number.

## Molecular and chemical measurements
- DNA quality and quantity:
  - DNA_qubit_ng_per_µl
  - DNA_260_280_ratio
  - DNA_260_230_ratio
  - DNA_conc_ng_per_g_soil
- Microbial gene copy numbers per gram soil:
  - X16S_bact_copy_per_g_soil
  - X16S_arch_copy_per_g_soil
  - fungi_ITS_copy_per_g_soil
  - AOA_copy_per_g_soil
  - AOB_copy_per_g_soil
  - nirS_copy_per_g_.soil
  - nirK_copy_per_g_soil
  - nifH_copy_per_g_soil
  - nosZI_copy_per_g_soil
  - nosZII_copy_per_g_soil

## Diversity metrics
- Bacterial diversity:
  - div16s.tot (richness)
  - div16s.shan (Shannon index)
- Fungal diversity:
  - divFun.tot (richness)
  - divFun.shan (Shannon index)

## Taxonomic composition data
- Phylum-level relative abundances (p__ prefixes) derived from amplicon reads.
- Coverage reference: sample’s 10,000 reads (percentages); some fields note 5,000 reads for fungal data.
- Example phyla included (among many):
  - Caldithrix, Acidobacteria, Actinobacteria, AD3, Armatimonadetes, Bacteroidetes, Chlorobi, Chloroflexi, Cyanobacteria, Elusimicrobia, Firmicutes, Fusobacteria, Gemmatimonadetes, Proteobacteria, Spirochaetes, Verrucomicrobia, and others listed with p__ prefixes.
- Includes unassigned identities (p__. field) and numerous phylum-level profiles across samples.

## Data quality, preprocessing and usability considerations
- Data are normalized to per gram of dry soil for gene copy numbers.
- Sequencing depth indicated by read counts per sample (10,000 reads; 5,000 reads for fungi in some fields).
- Metadata-rich structure supports traceability and reproducibility, with explicit identifiers and consistent naming conventions.
- The breadth of features (87 columns) underscores the need for clear documentation and data management to enable reuse.

## Relevance for monitoring frameworks and policy evaluation
- Enables assessment of agricultural management effects (digestate vs control; with nitrification inhibitor) on:
  - Microbial community composition (bacteria and fungi) across soil depths and timepoints.
  - Functional potential related to nitrogen cycling (nitrification, denitrification, nitrogen fixation).
- Integrates chemical/biological indicators (DNA metrics, gene copies, diversity indices) with taxonomic profiles to support soil health monitoring and policy-relevant decision-making.

## Governance, accessibility, and reuse considerations
- Metadata-dense dataset supports transparency and potential data sharing.
- Clear structure facilitates integration with other datasets but may require harmonization if incorporated into broader monitoring frameworks.
- Documentation of data provenance and metadata is essential to enable reuse in policy evaluation and monitoring reports.