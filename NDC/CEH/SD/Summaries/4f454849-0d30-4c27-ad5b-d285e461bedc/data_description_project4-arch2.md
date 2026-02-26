# Details on data collection

- A combined dataset from wood mice (Apodemus sylvaticus) and other small mammals collected 2014-2018, including wild and captive populations.
- Main components:
  - Longitudinal trapping study (Wytham Woods, Oct 2015-2018): fortnightly trapping in a 100 m² woodland grid; additional grid habitats in 2018; species include Apodemus sylvaticus, A. flavicollis, Myodes glareolus.
  - Dissection study (Wytham Woods, Oct 2017-18): euthanasia and dissection to quantify gut helminths and sample GI tract sections for microbiota analysis.
  - Diet shift experiment (captive colony, University of Edinburgh, May 2017): five dietary treatments varying seed (peanut) and insect (mealworm) proportions; gut microbiota and faecal metabolites measured.
  - Associated data from Silwood Park (Project 1: Wild rodents social networks and the microbiome) included in related submissions.
- Data collection details:
  - Longitudinal trapping: Sherman traps in a checkerboard 10x10 m grid; traps baited with peanuts, apple, bedding; PIT-tags for identification; faecal samples collected within 8 hours and stored at -80°C; parasite samples preserved in formalin; traps cleaned between sessions.
  - Dissection: ethical exclusions applied (PIT-tagged, juvenile, pregnant/lactating, non-target species); GI tract segmented into five sections for microbiota and helminth analyses; tissues frozen at -80°C and helminths stored in 70% ethanol.
  - Diet shift experiment: 17-18 week-old mice; six cages per group; 25-day diet perturbation with five daily shifts; faecal samples collected during handling; bedding samples collected for metabolite analysis; mice culled post-study under UK Home Office regulations.
- Studied habitats and locations:
  - Wytham Woods, Oxfordshire (51.77°N, -1.33°W): main 100 m² longitudinal grid plus additional habitat grids (conifer and meadow); dissection sites 300 m away from main grid.
- Ethical approvals and licenses:
  - RVC Clinical Research Ethical Review Board and University of Oxford Animal Welfare and Ethical Review Board for dissection work.
  - UK Home Office Regulations under Project license 70/8543 for the diet shift experiment.

# Data collection and processing workflow

- Sample types and handling:
  - Faecal samples for gut microbiota and parasite analysis; faecal pellets and bedding processed to maximize freshness; samples stored at -80°C or in formalin as appropriate.
  - GI tract tissues collected from five gut sections for microbiota and helminth analysis; samples snap-frozen or preserved in ethanol as required.
- DNA and sequencing:
  - DNA extraction from samples using 96-well plate Zymo kit with bead beating; inclusion of mock community and negative controls; DNA quantified with Qubit.
  - 16S rRNA gene amplicon sequencing targeting the V4 region via Illumina MiSeq (2x250 bp); two-step PCR with dual-indexing; eight sequencing runs across datasets.
  - Data processing with DADA2: primer trimming, quality filtering, ASV inference, merging of paired reads, chimera removal; taxonomic assignment against Silva Database v138; creation of a phyloseq object containing OTU/ASV table, taxonomy, and sample metadata.
  - The dataset provided as a raw phyloseq object (no far-reaching preprocessing beyond removal of non-gut taxa like chloroplasts/mitochondria).
- Diet metabolite profiling:
  - Faecal metabolite analysis by GC-FID using a modified David et al. (2014) protocol; internal standard added; metabolites identified against a standard mix of SCFAs (acetic, propionic, isobutyric, butyric, isovaleric, valeric, isocaproic, caproic, heptanoic acids).
- Parasitic load assessment:
  - Faecal flotation for parasite detection using sodium nitrate solution; eggs/oocysts counted to estimate eggs per gram (EPG) for multiple parasite taxa.
- Metadata and data structure:
  - Project_4_processed_microbiome_data.rds: phyloseq object with ASV counts, taxonomy, sample metadata, and reference sequences; includes four slots (otu_table, tax_table, sample_data, refseq).
  - Wytham_longitudinal_sample_metadata.csv: per-sample metadata for trapping events, including trap details, grid/habitat, PIT tag, species, sex, age, reproductive status, morphometrics, ectoparasites, bait consumption, and sample handling.
  - Full_Wytham_trapping_data.csv: detailed trapping events with processing times, trap outcomes, morphometrics, ectoparasite data, diet-related measurements, and sample handling notes.
  - Diet_shift_experiment_2017_metadata.csv: daily per-mouse data during the 30-day diet shift, including intervention type, diet composition, group, housing conditions, food intake, body measurements, fresh/fitted faecal samples, bedding samples, and metabolite measurements.
  - Diet characterisation and metabolite datasets described within the processing metadata (faecal SCFA concentrations and related measurements).

# Key outputs and formats

- Processed microbiome data
  - Phyloseq object (Project_4_processed_microbiome_data.rds) containing:
    - ASV count table (otu_table)
    - Taxonomic assignments (tax_table)
    - Sample metadata (sample_data) with extraction/sequencing details and cross-dataset fields
    - Reference sequences for ASVs (refseq)
  - Metadata keys in sample_data include dataset origin (Wytham_longitudinal, Wytham_dissection, Experiment), DNA extraction dates and batch, extraction format, sequencing batch/run, and sample identifiers.
- Datasets for analysis and monitoring
  - Longitudinal trapping metadata for population-level monitoring
  - Trapping data with processing and morphometric details for spatial-temporal analyses
  - Diet shift metadata for controlled experimental evaluation of diet-microbiome interactions
- Analytical scope
  - Gut microbiota composition via 16S rRNA (V4) sequencing
  - Diet-related microbiome shifts and metabolite production (SCFAs)
  - Gut helminth burden across GI tract sections
  - Links among microbiota, diet, host morphology, and parasite burden in wild and captive contexts

# Data quality, limitations, and accessibility

- Quality assurance:
  - Inclusion of mock communities and negative controls in DNA extraction
  - Standardized processing and storage protocols; consistent sample handling across datasets
  - Sequencing performed in multiple runs with batch-tracking to enable cross-batch comparisons
- Limitations:
  - Some numeric details omitted in the provided text (placeholders like XXX for sample counts and read counts)
  - Raw microbiome data are provided with minimal preprocessing, leaving downstream analysts responsible for filtering and normalization decisions
- Accessibility:
  - Datasets are organized with clear metadata files and a comprehensive phyloseq object to facilitate re-use and integration with external environmental datasets

# Relevance for environmental health and policy monitoring

- Standardized, time-stamped data across wild and captive populations support longitudinal assessments of environmental health indicators (microbiome diversity, diet effects, parasite pressure).
- Rich metadata enables cross-dataset analyses and benchmarking against other environmental monitoring programs.
- The inclusion of raw and processed microbiome data, metabolite profiles, and parasite metrics supports multi-factor analyses linking ecosystem changes to host health and ecosystem functioning.
- Data governance and ethical oversight documentation enhance trust and reproducibility for environmental policy evaluation and reporting.