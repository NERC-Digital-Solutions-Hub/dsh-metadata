# Details of data structure to CINAg_Digestate_experiment_2017_soil_biology.csv

## Overview
- Supplement to the CINAg supporting documentation.
- Dataset: CINAg_Digestate_experiment_2017_soil_biology.csv.
- Size: 87 columns and 180 rows.
- Source: Winter wheat digestate trial conducted in 2017.
- Purpose: Comprehensive data structure for soil biology measurements under different digestate treatments.

## Dataset structure and key variables
- Experiment: Inorganic fertilizer experiment.
- Sample_ID: Unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).
- Year, Site: Year of sampling; Site codes NW (North Wyke), HF (Henfaes Farm).
- Sampling_date, Sampling_time: Dates and timepoints (T1 and T2).
- Plot, Treatment: Plot numbers; Treatments are C (control), D (digestate), ADNI (acidified digestate with DMPP).
- Depth_cm: Soil depths (0-15, 15-30, 30-60 cm).
- Repeat: Replication indicator (0, 1, or 2).
- DNA_quality_and_quantity: DNA_qubit_ng_per_µl; DNA_260_280_ratio; DNA_260_230_ratio; DNA_conc_ng_per_g_soil.
- Microbial gene copies per g soil: X16S_bact_copy_per_g_soil; X16S_arch_copy_per_g_soil; fungi_ITS_copy_per_g_soil; AOA_copy_per_g_soil; AOB_copy_per_g_soil; nirS_copy_per_g_soil; nirK_copy_per_g_soil; nifH_copy_per_g_soil; nosZI_copy_per_g_soil; nosZII_copy_per_g_soil.
- Diversity metrics: div16s.tot; div16s.shan; divFun.tot; divFun.shan.
- Taxonomic composition (phylum-level): p__ followed by numerous phyla (e.g., Caldiserica, Chlorobi, Firmicutes, Proteobacteria, etc.) with percentages representing frequencies per sample (within 10,000 reads).
- Note: Includes multiple p__ entries for diverse bacterial phyla; some line breaks in the listing reflect formatting but all pertain to phylum-level abundances.

## Experimental design details
- Treatments evaluated: Control, Digestate, and Acidified Digestate with nitrification inhibitor (DMPP).
- Spatial and temporal resolution: Data across multiple plots, depths (0–15, 15–30, 30–60 cm), and two sampling times (T1, T2) at two sites.
- Multi-omics scope: Chemical/physiochemical context, DNA quality/quantity metrics, functional gene abundances (e.g., nifH, nirS, nosZ), and microbial community structure/diversity metrics from amplicon data.

## Measurements and units (highlights)
- DNA metrics: ng/µl (DNA_qubit_ng_per_µl); DNA_260/280 and DNA_260/230 ratios; DNA_conc_ng_per_g_soil.
- Gene copy numbers: copies per g soil (e.g., X16S_bact_copy_per_g_soil, nirS_copy_per_g_soil, nosZ_copy_per_g_soil, etc.).
- Diversity metrics: div16s.tot, div16s.shan, divFun.tot, divFun.shan (diversity indices and richness).
- Taxonomic frequencies: percentages (per 10,000 reads) for numerous bacterial phyla (p__ names).
- Dataset scope implies integration of molecular biology results with agronomic treatments and soil depth.

## Data quality and metadata considerations
- Data are tied to a specific experiment (digestate treatment) and include both quantitative measurements and sequencing-derived metrics.
- Metadata captures site, year, sampling times, depths, and replication status to support stratified analyses.
- Users should verify consistency of column naming (some phylum entries appear with formatting quirks) and ensure proper interpretation of read-depth normalization (per 10,000 reads).

## Practical considerations for data management and use
- Data discoverability: File referenced as CINAg_Digestate_experiment_2017_soil_biology.csv within the CINAg supporting documentation.
- Integration potential: Rich, multi-omics dataset enabling analyses of how digestate treatments affect microbial abundance, diversity, and functional potential across depths and time.
- Granularity: Highly granular by site, plot, depth, timepoint, and treatment, suitable for depth- and time-resolved microbiome analyses.
- Quality checks: Include DNA quality metrics and sequencing-based abundance measures to assess data reliability before downstream analyses.

## Potential uses for Data Leaders
- Develop and refine data governance around multi-omics soil biology datasets linked to agronomic treatments.
- Plan data discovery and metadata standards to improve discoverability of complex, multi-source data (chemical, molecular, sequencing) in soil studies.
- Enable cross-site, cross-treatment comparisons by leveraging depth- and time-resolved microbial metrics and diversity indices.
- Inform data product design for soil microbiome dashboards by aligning variables (gene abundances, diversity, phylum-level abundances) with user needs.