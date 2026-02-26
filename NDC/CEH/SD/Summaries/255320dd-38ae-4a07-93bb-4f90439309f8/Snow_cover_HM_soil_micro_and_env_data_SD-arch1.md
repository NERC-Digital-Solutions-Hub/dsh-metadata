# Alpine grassland soil microbial and biogeochemical data from a snow manipulation experiment in Hohe Mut, Austria, 2017

- Study site and experimental design
  - Location: Hohe Mut summit, 2650 m, near Obergurgl, Austria (lat 46.84862, lon 11.02957)
  - Plots: 15 plots × 6 m2, randomly allocated to three snow manipulation treatments (n = 5 per treatment): snow removal, snow addition, untreated control
  - Plot protection: fenced to prevent trampling
  - Environmental monitoring: soil moisture and temperature tracked with HOBO data loggers
  - Snow manipulations: conducted three times between end of March and end of May 2017; removal plots reduced snow depth to <10 cm using a snow blower or shovels; addition plots received extra snow; control plots left undisturbed

- Soil sampling timeline and field procedures
  - Sampling points (six time points across late winter to early summer 2017): late winter (28/3), snowmelt (1/6 and 8/6), spring post-snowmelt (12/6 and 18/6), early summer (8/7)
  - Sampling method: five random locations per plot; soil cores (diameter 2 cm, depth ~7 cm; shallower where soil was frozen) pooled per plot; vegetation/litter removed
  - Molecular analyses: five subsamples (~200 mg each) combined per sample; preserved in DNA/RNA shield; field lysis performed; stored at -80°C
  - Biogeochemical and enzyme samples: sieved to 4 mm; stored at 4°C for up to 2 weeks; shipped to Manchester for analyses

- Biogeochemical cycling and soil properties measured
  - N forms: plant-available NH4+-N and NO3--N extracted with 1 M KCl; DON extracted with water; analyzed with a flow analyzer
  - Mineralisation: 14-day incubation at 25°C to determine NH4+-N and NO3--N release
  - Dissolved carbon: DOC measured from water extracts with a TOC analyzer
  - Basic soil properties: pH (1:2.5 soil:water), soil water content (gravimetric), total C and N (105°C dried soil via elemental analyser)

- Extracellular enzyme assays
  - Enzymes assayed (absolute potential activity): eight enzymes including GLC, CBH, XYL, NAG, PHO, URE, POX, PER
  - Substrates and readouts: specific substrates for each enzyme; colorimetric or spectrophotometric readouts after incubation; corrections for soil/substrate colour
  - Units: nmol product g-1 soil h-1 (except URE measured as ammonium production per g dry soil per hour; PER/POX measured via L-DOPA oxidation)
  - Normalisation: enzyme activities also presented relative to microbial biomass by dividing by total PLFA

- Microbial biomass and community analyses
  - PLFA (phospholipid fatty acid) profiling: used to estimate total microbial biomass and to differentiate fungal vs. bacterial groups (fungal marker 18:2w6,9; bacterial markers include various 16:1, 18:1, 18:0, etc.)
  - DNA extraction: using ZR soil microbe DNA kit with enhanced lysis; DNA stored at -20°C
  - Bacterial and fungal community profiling: 16S rRNA gene (bacteria) and ITS2 region (fungi) amplicon sequencing via Illumina MiSeq
  - Library preparation: two-step PCR with Illumina adapters and sample-specific barcodes; libraries normalised and sequenced; PhiX spike-in included
  - Data processing: quality filtering, dereplication, and ASV/OTU inference using DADA2 in R; taxonomic assignment with GreenGenes (bacteria) and UNITE (fungi)
  - Sequencing depth: 16S ~ 5.7 million reads; ITS ~ 3.08 million reads after processing; data rarefied to 10,083 (16S) and 5,349 (ITS) reads per sample
  - Sample naming: links between sequence data and soil data via sample16S and ITSsample identifiers

- Data structure and available files
  - Soil and enzyme/microbial data: Snow_cover_HM_soil_env_data.csv
    - Columns include: date, timepoint, season, plot, treat (1 snow removal, 2 control, 3 snow addition), snow status, onoff, days since melt, swc (soil water content), pH, TOCwat, NH4, NO3, TIN, TN, ON, NH4inc, NO3inc, urer, nagr, phor, cbhr, xylr, glcr, perr, poxr, C, Nit, CNrat, C14:0, i-C15:0, a-C15:0, etc. for PLFA markers and enzyme activities
  - Microbial sequence data: Snow_cover_HM_seq_tab_16S.csv (bacterial counts) and Snow_cover_HM_seq_tab_ITS.csv (fungal counts)
  - Taxonomy info: Snow_cover_HM_16S_taxa.csv (bacterial taxa) and Snow_cover_HM_ITS_taxa.csv (fungal taxa)
  - Raw data and metadata: raw sequence data deposition at the European Bioinformatics Institute; sample-to-data mapping provided by the Snow_cover_HM_soil_env_data.csv
  - Data provenance and documentation: detailed methods and parameter settings included in the accompanying documentation and references

- Processing details and methodological references
  - Enzyme assays: high-throughput microplate approaches with standard references for each enzyme; corrections for colour
  - PLFA methodology: Bligh and Dyer lipid extraction; fungal and bacterial biomarker interpretation
  - DNA and sequencing: two-step PCR with Illumina adapters; barcode encoding; DADA2 pipeline for ASVs; classical databases for taxonomy (GreenGenes, UNITE)
  - Data handling: sequence depth normalization via rarefaction; standard R packages (phyloseq, etc.) referenced

- Data accessibility and utility for analysis
  - Rich, multi-omics dataset enabling correlations across snow treatments, soil chemistry, microbial biomass, community composition, and enzyme functionality
  - Longitudinal sampling across winter-to-summer seasons supports temporal trend analyses and predictive modelling of snow manipulation impacts on alpine soil processes
  - Comprehensive metadata and explicit links between biogeochemical measurements and microbial data facilitate reproducible analyses and cross-study comparisons

- References for methods
  - Key methodological sources spanning enzyme assays, PLFA, DNA extraction, sequencing, and data processing, including foundational works and recent methodological papers (references 1–28)