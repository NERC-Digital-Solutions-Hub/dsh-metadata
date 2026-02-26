# Supporting documentation for 'Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017' deposited in the Environmental Information Data Centre repository

- Purpose: Document the Alpine grassland snow-manipulation experiment and the associated soil abiotic, biogeochemical, microbial biomass, enzyme activity, and microbial community data to support monitoring of environmental health and policy performance over time.
- Context: Field experiment on Hohe Mut summit (2650 m) near Obergurgl, Austria to assess how different snow conditions influence soil processes and microbial communities.

## Field experimental design

- Plots and treatments:
  - 15 plots of 6 m x 2 m, randomly allocated to three treatments (n = 5 per treatment): snow removal, snow addition, and untreated control.
  - Plots fenced to prevent trampling by humans/animals.
- Environment and manipulation:
  - Snow manipulated three times from late March to late May 2017.
  - Snow depth reduced on removal plots to <10 cm; snow added evenly to addition plots; control plots left undisturbed.
  - Soil moisture and temperature monitored with HOBO data loggers.
- Location data:
  - Coordinates provided; high-elevation alpine grassland context.

## Sampling regime and sample processing

- Soil sampling timeline:
  - Six time points spanning late winter to early summer 2017: late winter (28/03), snowmelt (01/06 and 08/06), spring post-snowmelt (12/06 and 18/06), and summer (08/07).
- Field sampling procedure:
  - Soil cores (diameter 2 cm, depth ~7 cm; shallower where soil was frozen) taken from five random locations per plot.
  - Cores pooled per plot, vegetation/litter removed, homogenised.
  - Subsamples collected for molecular analyses (approx. 200 mg per subsample; preserved in DNA/RNA shield; field lysing performed; stored at -80°C).
  - Additional soil for enzyme and biogeochemical analyses stored at 4°C for up to 2 weeks and shipped to Manchester for analysis.
- Edge effects:
  - Sampling performed ≥1 m from plot edges.

## Biogeochemical cycling and soil properties (abiotic and chemical)

- Measurements and methods:
  - Plant-available NH4+-N and NO3--N, and dissolved organic nitrogen (DON) extraction with 1 M KCl or water for DON; analysis via automated multi-chemistry analyzer.
  - Net mineralisation rates: incubation of 5 g soil for 14 days at 25°C.
  - Dissolved organic carbon (DOC) via water extraction and TOC analyzer.
  - pH (1:2.5 soil:water) and gravimetric soil water content.
  - Total C and N content via elemental analyzer on dried soil.
- Output types:
  - Concentrations of inorganic N, DON, DOC, pH, soil moisture, and total C/N.

## Extracellular enzyme assays (microbial functioning indicators)

- Target enzymes (absolute potential activity):
  - GLC (β-glucosidase), CBH (cellobiohydrolase), XYL (β-xylosidase), NAG (N-acetylglucosaminidase), PHO (phosphatase), URE (urease), POX (phenol oxidase), PER (peroxidase).
- Roles:
  - GLC, CBH, XYL: cellulose and hemicellulose decomposition.
  - NAG: chitin and related polymers; PHO: phosphomonoesters; POX/PER: lignin/polyphenol degradation; URE: urea hydrolysis.
- Assay details (high-level):
  - 96-well plate microplate assays with specific substrates; colorimetric detection (pNP or L-DOPA-based) and absorbance readings; corrections for soil/substrate coloration.
  - Time points and substrate-specific incubation times; enzyme activities calculated relative to substrate conversion.
- Normalisation:
  - Enzyme activities also expressed relative to microbial biomass via division by total PLFA.

## Phospholipid fatty acid (PLFA) analyses (microbial biomass and community structure)

- Purpose:
  - Quantify total microbial biomass and characterize fungal vs. bacterial, and Gram-positive vs. Gram-negative markers.
- Methods:
  - PLFA extraction and analysis via gas chromatography.
  - Biomarker markers used to assign fungal and bacterial groups (e.g., 18:2w6,9 for fungi; various chain markers for Gram +/- bacteria).
- Outputs:
  - Total PLFA abundance (nmol/g soil) and community composition ratios (fungal:bacterial, Gram-positive:Gram-negative).

## DNA extraction and microbial community profiling

- DNA extraction:
  - Zymo soil microbe DNA kit with enhanced lysis step; extraction performed with field-adapted steps and subsequent storage at -20°C.
- Sequencing targets:
  - Bacteria: 16S rRNA gene; Fungi: ITS2 region.
- Library preparation and sequencing:
  - Two-step Illumina PCR protocol using tagged primers; unique sample barcodes; library normalization and MiSeq sequencing (V3 chemistry).
- Data processing:
  - Quality control, merging, denoising to generate ASV tables using DADA2 in R.
  - Taxonomic assignment with Greengenes (16S) and UNITE (ITS).
  - Rarefaction to even sequencing depth (16S: ~10,083 reads; ITS: ~5,349 reads) to reduce biases.
- Outputs:
  - OTU/ASV tables for bacteria and fungi; associated taxonomic information in separate taxa files.

## Data structure and accessibility

- Primary data file:
  - Snow_cover_HM_soil_env_data.csv containing:
    - date, timepoint, season, plot, treatment (1 snow removal, 2 control, 3 snow addition), snow status, sample identifiers, snow cover status, days relative to snowmelt, soil water content (swc), pH, TOC in water extracts, NH4 and NO3 (KCl extracts), TIN, TN, ON, incubation-derived NH4inc and NO3inc, urease (urer), N-acetylglucosaminidase (nagr), phosphatase (phor), cellobiohydrolase (cbhr), xylosidase (xylr), glucosidase (glcr), peroxidase (perr), and total C/N indicators; plus PLFA, enzyme, and soil chemistry columns.
  - Column naming notes indicate copies of measurements (e.g., 1 = immediate extract; 2 = incubation/derived metrics).
- Microbial sequence data:
  - Snow_cover_HM_seq_tab_16S.csv and Snow_cover_HM_seq_tab_ITS.csv: ASV/OTU counts per sample.
  - Snow_cover_HM_16S_taxa.csv and Snow_cover_HM_ITS_taxa.csv: taxonomic information for 16S/ITS taxa.
- Metadata and data structure notes:
  - Sample names in sequence tables align with sample16S and ITSsample columns in the main data file.
  - Raw sequence data to be deposited at the European Bioinformatics Institute (EBI).
- Data portals:
  - Supporting documentation deposited in Environmental Information Data Centre repository.
  - Raw sequencing data intended for deposition at EBI.

## Data processing and methodological references

- High-level methodological basis:
  - Standardised, high-throughput enzyme assays; PLFA biomarker approaches; DNA extraction adaptations; 16S/ITS amplicon sequencing; DADA2 for sequence variant inference; taxonomic assignment with Greengenes and UNITE.
- Key references (representative examples of methods used):
  - Enzyme activity assays and substrate calibrations; PLFA protocols; DADA2 workflow; Illumina amplicon library preparation and indexing strategies; fungal ITS primer development; Greengenes and UNITE taxonomic databases.
- Data integrity and reproducibility:
  - Detailed procedural steps, replication (n=5 per treatment for field plots; multiple analytical replicates per sample), and normalization approaches (e.g., enzyme activity relative to PLFA).

## Practical implications for environmental monitoring and analysis

- Integrated dataset enables:
  - Linking snow manipulation to changes in soil chemistry, microbial biomass, enzyme activities, and microbial community composition over seasonal time points.
  - Assessing how abiotic changes drive microbial-mediated nutrient cycling and organic matter turnover in alpine grasslands.
- Data integration opportunities:
  - Combining abiotic, biogeochemical, enzyme, PLFA, and sequencing data to model ecosystem processes and monitor environmental health over time.
  - Potential to enhance data value by cross-referencing with other environmental datasets and enabling broader accessibility to researchers and policy analysts.