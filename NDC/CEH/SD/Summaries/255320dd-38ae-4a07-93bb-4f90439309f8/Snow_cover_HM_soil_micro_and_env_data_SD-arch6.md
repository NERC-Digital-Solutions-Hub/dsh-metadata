# Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017

- Study design and scope
  - Field experiment on Hohe Mut summit (2650 m), Austria, with 15 plots (6 m2 each) randomly assigned to three snow treatments: snow removal, snow addition, and untreated control (5 replicates per treatment).
  - Snow manipulation occurred three times between late March and late May 2017; the manipulation altered soil temperature and moisture.
  - Aims to support robust data exploration of how snow cover affects soil biogeochemistry and microbial communities.

- Sampling scheme and field procedures
  - Soil sampling across six time points spanning late winter to early summer 2017: late winter (28/03), snowmelt (01/06; 08/06), spring (12/06; 18/06), and summer (08/07).
  - Five soil cores per plot (diameter 2 cm, depth ~7 cm; some shallower when frozen) were pooled per plot; vegetation/litter removed.
  - Molecular analyses: five subsamples per plot stored in DNA/RNA preservation buffer and kept at -80°C.
  - Soil for enzyme and biogeochemical analyses sieved and stored at 4°C for transport to Manchester, UK.

- Measurements and analyses
  - Biogeochemical properties
    - Plant-available nutrients: NH4+-N and NO3--N extracted with 1 M KCl; DON via water extraction; mineralisation rates after 14 days at 25°C.
    - Dissolved organic carbon (DOC) from water extracts; soil pH; soil water content; total C and total N in dried soil.
  - Extracellular enzyme activities (potential absolute activity)
    - GLC, CBH, XYL, NAG, PHO, and URE (high-throughput photometric assays) to probe carbon and nitrogen cycling.
    - POX and PER (L-DOPA-based) for lignin-type and phenolic degradation; URE via ammonia production assay.
    - Enzyme activities reported per soil sample and normalized relative to microbial biomass using PLFA.
  - Microbial biomass and community structure
    - PLFA analysis to estimate total microbial biomass and fungal/bacterial community structure (markers for fungi, Gram-positive/Gram-negative bacteria, and non-specific indicators).
    - DNA extraction and sequencing-based profiling
      - 16S rRNA (bacteria) and ITS2 (fungi) amplicon sequencing using a 2-step Illumina protocol; rarefaction and ASV/table construction with DADA2.
      - Taxonomic assignment: Greengenes for 16S; UNITE for ITS.
      - Raw sequence data deposited at the European Bioinformatics Institute (EBI); accompanying taxa tables provided.
  - Data processing and normalization
    - Enzyme activities optionally scaled relative to PLFA biomass to reflect investment in enzymes per microbial biomass.
    - Sequencing data processed to produce ASV tables; sample names linked to soil data via sample16S and ITSsample identifiers.

- Data files and structure
  - Snow_cover_HM_soil_env_data.csv
    - Contains soil abiotic, PLFA, and soil extracellular enzyme data with columns for date, timepoint, season, plot, treatment, snow status, sample identifiers (ITSsample, sample16S), snow presence indicator, days since/until snowmelt, soil water content (swc), pH, dissolved and total carbon/nitrogen metrics (TOCwat, NH4, NO3, TN, CN ratios, etc.), incubation-derived NH4inc/NO3inc, urease (urer), NAG (nagr), phosphatase (phor), CBH (cbhr), XYL (xylr), GLC (glcr), PER (perr), POX (poxr), total C and N contents, and PLFA-based C/N ratios.
    - Rows correspond to sampling events and plots; includes both measured and derived metrics.
  - Snow_cover_HM_seq_tab_16S.csv
    - Bacterial OTU/ASV abundance table; columns are samples; rows are bacterial taxa.
  - Snow_cover_HM_seq_tab_ITS.csv
    - Fungal ITS OTU/ASV abundance table; columns are samples; rows are fungal taxa.
  - Snow_cover_HM_16S_taxa.csv
    - Taxonomic information for 16S OTUs/ASVs.
  - Snow_cover_HM_ITS_taxa.csv
    - Taxonomic information for ITS taxa.
  - Data relationships
    - Sample names in sequencing tables correspond to sample16S (16S data) and ITSsample (ITS data) in Snow_cover_HM_soil_env_data.csv, enabling integrated analyses across microbial and soil measurements.
  - Availability
    - Raw sequencing data deposited at EBI; methodological details and data processing pipelines are described to support reproducibility and data reuse.

- Data processing and methodology notes
  - DNA and sequencing work followed standardized high-throughput pipelines:
    - 2-step Illumina PCR with sample-specific barcodes; libraries prepared and quantified; MiSeq sequencing with V3 chemistry.
    - DADA2 used for quality filtering, dereplication, denoising, ASV construction, and taxonomic assignment against Greengenes (16S) and UNITE (ITS).
  - PLFA profiling followed established lipid-based microbial biomass methods; fungal and bacterial markers used to derive community composition and biomass estimates; ratios computed (fungal:bacterial, Gram-positive:Gram-negative) to characterize community shifts.
  - Extracellular enzyme assays used high-throughput substrates; activities reported as nmol or µmol product g-1 dry soil h-1, with standard corrections for soil color and substrate interference; enzyme data optionally normalized to PLFA biomass.

- How to use the data (Data Support perspective)
  - Integrate soil chemistry and biogeochemical measures with microbial community data to study how snow manipulation impacts soil function and microbial ecology over time.
  - Track temporal dynamics of enzyme activities and mineralisation alongside microbial composition shifts (16S/ITS) and microbial biomass (PLFA).
  - Compare treatment effects (snow removal vs. snow addition vs. control) across time points to identify robust patterns in carbon and nitrogen cycling, microbial processes, and community structure.
  - Build data products such as:
    - Time-series dashboards of key soil nutrients, enzyme activities, and PLFA biomarkers by treatment.
    - Diversity and abundance plots for bacterial and fungal communities, with time and treatment facets.
    - Correlation networks linking enzyme activities, mineralisation rates, and microbial community metrics.
  - Data provenance and harmonization considerations
    - Use sample16S/ITSsample identifiers to join soil data with microbial abundance tables and taxa metadata.
    - Pay attention to units and normalization (e.g., enzyme activities relative to PLFA biomass vs. absolute activities) when performing comparative analyses.

- Access and reproducibility
  - Data are organized for reuse by data consumers and analysts, with explicit data structure mappings and cross-referenced sample identifiers.
  - Raw sequencing data are deposited and available through EBI; processing steps and reference databases are documented to enable replication or re-analysis with alternative pipelines.