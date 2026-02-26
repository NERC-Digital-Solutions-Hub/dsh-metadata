# Details on data collection

- This document describes integrated datasets on wood mice (Apodemus sylvaticus) and other small mammals collected between 2014-2018 from wild and captive populations. It centers on gut microbiome profiling, diet, parasites, and host traits, collected across multiple linked studies in Wytham Woods, Oxfordshire, and a parallel diet-shift experiment in Edinburgh.

## Datasets and study designs

- Longitudinal Trapping (Wytham Woods, 2015-2018)
  - Wild rodent population in a 100 m2 grid; additional habitat grids (conifer and meadow) sampled in 2018.
  - Species include Apodemus sylvaticus, Apodemus flavicollis, and Myodes glareolus.
  - Methods: capture-mark-recapture with Sherman traps, PIT-tags for identity, fortnightly to 2–4 week intervals.
  - Samples: fecal material for gut microbiota; fecal samples for parasite quantification; processing data includes demographic and morphological measurements; ethical and husbandry details described.

- Dissection Study (Wytham Woods, 2017-2018)
  - Fortnightly trapping nights aligned with the longitudinal study.
  - Euthanasia performed for GI tract dissection to quantify gut helminths and microbiota across five GI sections; tissue and contents collected and stored for microbiota and parasite analyses.
  - Ethical approvals noted; includes detailed processing of morphometrics, fecal collection, and organ sampling.

- Experimental Diet Shift (Laboratory, Edinburgh, May 2017)
  - Outbred wood mice in specific pathogen-free conditions; five diet groups manipulating seed (peanut) and insect (mealworm) content in a 25-day perturbation, followed by a return to chow.
  - Data collected: microbiome and fecal metabolites, body mass, food intake, bedding samples for metabolite analysis; post-experiment euthanasia.
  - Ethical approvals under UK Home Office Regulations (Project license 70/8543).

## Data products and formats

- 1) Project_4_processed_microbiome_data.rds
  - A phyloseq object containing microbiome data for the three main datasets (longitudinal, dissection, and experiment) after DADA2 processing and SILVA taxonomy assignment.
  - Includes four slots: otu_table (ASV counts), tax_table (taxonomy), sample_data (metadata), refseq (raw ASV sequences).
  - Two extraction/sequencing batches; non-gut taxa filtered out; minimal preprocessing beyond removal of chloroplasts/mitochondria.

- 2) Wytham_longitudinal_sample_metadata.csv
  - Sample-level metadata for the longitudinal study, tied to each trapping event.
  - Columns cover: sample identifiers, collection date, trap/grid details, species, sex, age, body metrics, reproductive status, PIT/ear IDs, ectoparasite screening results, parasite burdens (EPG) for multiple taxa, and bait_leftover counts.

- 3) Full_Wytham_trapping_data.csv
  - Comprehensive trapping and processing data per trap event.
  - Includes: data enterer, data entry method, collection date, trap outcomes, trap number, grid/habitat details, processing time, anatomical/biometric measurements, PIT information, species/sex/age, ectoparasite screen results, parasite counts (EPG), and miscellaneous notes.

- 6) Diet_shift_experiment_2017_metadata.csv
  - Daily data per mouse during the 30-day diet shift experiment.
  - Columns cover: Seq_ID, Mouse.ID, day of experiment, date, intervention type (single housing or diet change), shift period, diet type (e.g., 100s, 75s, 50s, 25s, 100i, chow), hours since intervention, group, sex, origin cage, processing time, body weight, body condition, jar weight, food intake, food left, top-up, fresh/fecal bedding weights, times for storage, notes.
  - Metabolite and intake measurements: acetic, propionic, isobutyric, butyric, isovaleric, valeric, isocaproic, caproic acids, total SCFA, all in micrograms per mg or related units.

## Data processing and microbiome analysis details

- DNA extraction and sequencing
  - Extraction with Zymo Quick-DNATM kits on a 96-well plate; bead-beating for homogenization; QC with Qubit.
  - Library preparation: two-step PCR with dual-indexing; targeting the V4 region of 16S rRNA; Illumina MiSeq 2x250 bp reads; four sequencing runs in two batches.
  - Negative controls included; mock community standards incorporated.

- Bioinformatics
  - DADA2 pipeline for ASV inference; primer/adaptor trimming with cutadapt; quality filtering and merging of paired-end reads; chimera removal.
  - Taxonomy assigned against SILVA database v138.
  - Output packaged as a phyloseq object; raw (as-raw-as-possible) data, with no aggressive filtering performed beyond standard gut-microbial removal of non-gut taxa.

- Diet/metabolite and parasite data
  - Faecal metabolite profiling by GC-FID with internal standard and a targeted panel of SCFAs; standard curves used to calibrate abundance.
  - Gut helminth quantification via fecal flotation (sodium nitrate) to estimate eggs per gram; acknowledges detection limits for certain taxa.

## Ethics and governance

- Approvals from:
  - RVC Clinical Research Ethical Review Board.
  - University of Oxford Department of Zoology Animal Welfare and Ethical Review Board.
  - UK Home Office Regulations (Project license 70/8543) for laboratory work.
- Animal welfare considerations described for trapping, handling, sampling, and euthanasia.

## Data access, reuse, and interoperability

- Data are organized to enable cross-dataset analyses, linking microbiome profiles with host traits, diet exposure, parasite burdens, and ecological context.
- Key data objects (phyloseq for microbiome, rich per-sample metadata, and detailed trap/processing data) are provided to support reproducible analyses and potential creation of self-serve data products or dashboards.
- Clear documentation of data provenance, batch information, and extraction/sequencing details to support reproducibility.

## Notes and considerations

- Certain counts and sequence-length specifics are indicated with placeholders (e.g., XXX) where exact values are not present in the text.
- The data encompass both wild populations and a controlled diet-shift experiment, enabling comparative analyses across natural and experimental conditions.

## Relevance for Data Support

- Illustrates end-to-end data lifecycle: collection in the field, controlled experiments, multi-omics analyses (microbiome, metabolites, parasites), and rich metadata.
- Demonstrates integration of heterogeneous data sources into cohesive data products (phyloseq object and comprehensive CSV metadata) to enable self-serve exploration and broader policy or research inquiries.