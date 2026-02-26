# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017' deposited in the Environmental Information Data Centre repository

- Location and field setup
  - Summit of Hohe Mut (2650 m) near Obergurgl, Austria (lat. 46.84862, lon. 11.02957)
  - 15 plots of 6 m2 each, randomly assigned to snow removal, snow addition, or untreated control (n = 5 per treatment)
  - Plots fenced to prevent trampling; soil moisture and temperature monitored with HOBO data loggers

- Snow manipulation
  - Three manipulation events between late March and late May 2017
  - Snow removal: depth reduced to <10 cm using snow blower or hand tools
  - Snow addition: snow evenly added to designated plots
  - Control plots left undisturbed
  - Aim: assess impacts on soil temperature and moisture

- Soil sampling design
  - Six sampling timepoints spanning late winter to early summer 2017
    - Late winter (28 March)
    - Snowmelt (1 June and 8 June)
    - Spring post-snowmelt (12 June and 18 June)
    - Summer (8 July)
  - Sampling within plots: five random locations per plot, at least 1 m from edges
  - Core size: Ø 2 cm, depth ~7 cm (shallower if soil frozen)
  - Field handling: vegetation/litter removed; cores pooled per plot, five subsamples prepared for molecular analyses
  - Preservation: DNA/RNA protection buffer; storage at -80°C; separate soil for enzyme/biogeochemical analyses stored at 4°C for up to 2 weeks and shipped to Manchester for analysis

- Biogeochemical measurements
  - Plant-available nitrogen and DON
    - NH4+-N and NO3--N extracted with 1 M KCl (5 g soil; 25 mL extract)
    - DON extracted with ultrapure water (35 mL)
    - Analysis by segmented flow multi-chemistry analyser
  - Mineralisation
    - Net NH4+-N and NO3--N mineralisation after 14 days at 25°C
  - Dissolved and total carbon/nitrogen
    - DOC from water extracts measured with TOC analyser
    - pH in 1:2.5 soil:water suspension
    - Soil water content gravimetrically
    - Total soil C and N by elemental analysis (105°C drying)

- Extracellular enzyme assays
  - Eight enzymes tested to probe microbial function
    - GLC (β-glucosidase), CBH (cellobiohydrolase), XYL (β-xylosidase)
    - NAG (N-acetylglucosaminidase), PHO (phosphatase), URE (urease)
    - POX (phenol oxidase), PER (peroxidase)
  - Substrate-specific colorimetric assays in microplates; absorbance measured and converted to activity
  - Enzyme activity also expressed relative to microbial biomass using PLFA

- Phospholipid fatty acid analysis (PLFA)
  - Assess total microbial biomass and broad community structure
  - Biomarkers for fungi and major bacterial groups (Gram-positive, Gram-negative, non-specific)
  - Abundances expressed as nmol g soil-1 and used to derive fungal:bacterial and Gram-positive:Gram-negative ratios

- DNA extraction and sequencing
  - DNA extraction using ZR soil microbe kit with additional lysis step
  - Amplicon sequencing for bacterial (16S rRNA) and fungal (ITS2) communities
  - Two-step Illumina PCR protocol with tagged primers and barcodes
  - Library preparation, purification, and sequencing on Illumina MiSeq (V3 chemistry)

- Bioinformatics and data processing
  - Sequence processing with DADA2 in R (quality filtering, denoising, ASV inference)
  - Taxonomic assignment with Greengenes (16S) and UNITE (ITS)
  - Rarefaction to even depth for downstream analyses
  - OTU/ASV tables for bacteria (16S) and fungi (ITS2)
  - Taxa metadata files accompanying sequence tables

- Data products and structure
  - Soil abiotic, PLFA, and enzyme activity data: Snow_cover_HM_soil_env_data.csv
    - Columns include: date, timepoint, season, plot, treat (snow removal, control, snow addition), snow status, sampling day, soil water content, pH, TOCwat, NH4, NO3, TIN, TN, ON, incubation-derived N metrics, urease, nagr, phor, cbhr, xylr, glcr, perr, poxr, C, Nit, CNrat, several PLFA markers (C14:0, i-C15:0, a-C15:0, etc.)
  - Microbial community abundance data
    - Snow_cover_HM_seq_tab_16S.csv: 16S sequence variant counts per sample
    - Snow_cover_HM_seq_tab_ITS.csv: ITS sequence variant counts per sample
  - Taxonomic assignments
    - Snow_cover_HM_16S_taxa.csv: taxonomic information for 16S ASVs/OTUs
    - Snow_cover_HM_ITS_taxa.csv: taxonomic information for ITS ASVs/OTUs
  - Metadata linkage
    - Sample names in sequence tables match the sample16S and ITSsample columns in Snow_cover_HM_soil_env_data.csv
  - Data access
    - Raw sequence data being deposited at the European Bioinformatics Institute (EBI)

- Practical notes for GIS-oriented use
  - Data are organized by plot and timepoint, enabling spatial-temporal analyses across snow treatments
  - Plot-level data support mapping of soil properties, enzyme activities, and microbial community shifts
  - Clear coding for treatments and snow status facilitates integration with environmental layers (e.g., elevation, aspect, snow cover, microclimate)
  - Documented methods and units support reproducibility and cross-study comparisons
  - Access to links between soil chemistry, enzyme activities, PLFA biomarkers, and microbial community composition enables multi-layer map visualisations and trend analyses

- References and methodological provenance
  - Methods and standards for soil enzyme assays, PLFA, DNA extraction, sequencing, and DADA2 processing as cited in the accompanying references (1–28)