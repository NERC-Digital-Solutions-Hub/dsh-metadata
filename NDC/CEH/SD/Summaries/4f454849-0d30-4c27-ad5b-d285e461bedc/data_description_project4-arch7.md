# Details on data collection

- Scope and scope of datasets
  - Datasets describe wood mice (Apodemus sylvaticus) and other small mammals collected 2014-2018.
  - Main components include: longitudinal trapping in Wytham Woods, a dissection study, and a diet shift experiment in a captive colony.
  - Datasets underpin work described in Marsh (2020) and relate to additional data submissions (e.g., Silwood Park project).

- Spatial design and GIS relevance
  - Longitudinal study area: 100 m² grid within a 100 m × 100 m woodland plot at Wytham Woods.
  - Additional habitat grids: two 100 m × 50 m grids (conifer and meadow) sampled mid-2018.
  - Dissection study locations: 8 sites at least 300 m from the main grid.
  - Habitat contexts include mixed/Conifer/Meadow, with reference to an associated Figure 1 and related study areas (e.g., Holly Hill).

- Data collection protocols
  - Longitudinal trapping: Sherman live traps set in a checkerboard design; fortnightly to monthly captures; individuals processed, sampled, and released within their grid cell.
  - Individual animal data: species, sex, weight, age, PIT-tag, and unique identifiers; some captures resulting in deaths or humane euthanasia.
  - Sample handling: fecal samples collected at trapping, stored at -80°C within 8 hours; faecal samples for parasite analysis stored in 10% formalin; stringent sterilization between samples and traps.
  - Dissection study: ethical approvals obtained; juvenile/pregnant/lactating mice excluded; euthanasia performed for analysis; GI tract divided into five sections for microbiota and parasite analysis; samples stored appropriately for microbiome and helminth assessments.
  - Experimental (diet shift) data: outbred laboratory colony under controlled semi-barrier conditions; five diet treatments varying seed (peanut) and insect (mealworm) content; 25-day perturbation with staged diet changes; fresh fecal samples collected during handling; body mass and food intake measured; mice culled after the experiment.

- Data sets and structure (files available)
  - 1) Project_4_processed_microbiome_data.rds
    - A phyloseq object containing microbiome data for the three main datasets (Wytham longitudinal, dissection, and experiment), post-DADA2 processing and taxonomic assignment to Silva v138.
    - Four slots: otu_table (ASV counts), tax_table (taxonomy), sample_data (metadata), refseq (raw ASV sequences).
  - 2) Wytham_longitudinal_sample_metadata.csv
    - Per-sample metadata for longitudinal trapping: unique sample code, collection date, trap/grid identifiers, habitat type, PIT tag, Animal_ID, species, sex, age, measurements (e.g., AGD, limb lengths), ectoparasite data, bait left, and other observations.
  - 3) Full_Wytham_trapping_data.csv
    - Per-trap processing data: data enterer, dataEntry method, collection date, trap specifics, grid/habitat, species, sex, morphometrics, PIT and tag information, ectoparasite screen results, parasite counts (EPG), bait consumption indicators, release details, and misc. notes.
  - 6) Diet_shift_experiment_2017_metadata.csv
    - Per-animal per-day data for the 30-day diet shift experiment: Seq_ID, Mouse.ID, date, intervention type, shift period, diet type (seed/insect ratios), hours since intervention, sex, origin cage, processing time, body weight, body condition, jar weight, food intake, total food left, fresh poo, bedding poo, timing for storage, dietary and metabolite measurements (acetic, propionic, butyric, isobutyric, valeric, isocaproic, caproic, heptanoic acids, total SCFA), and notes.
  - Note: Several numeric fields show placeholders (e.g., XXX) where exact counts are not specified in the text.

- Molecular methods and data processing
  - DNA extraction: 96-well plate Zymo Quick-DNATM kits; bead-beating for homogenization; extraction batches include mock community and negative controls; DNA quantified with Qubit.
  - Library preparation and sequencing: two-step, dual-index Illumina approach targeting the V4 region of 16S rRNA; MiSeq runs with 2 × 250 bp reads; four runs in total (two runs for longitudinal/experimental, two for longitudinal/dissection).
  - Bioinformatics: sequence data demultiplexed and processed with DADA2; primer/adaptor trimming with cutadapt; quality trimming to produce forward/reverse read lengths; ASV inference, merging, chimera removal; taxonomy assigned against Silva v138; creation of a phyloseq object (raw, with no downstream filtering applied).
  - Diet characterization and metabolite profiling
    - Faecal metabolite profiling via GC-FID, with internal standard and targeted SCFAs (acetic, propionic, isobutyric, butyric, isovaleric, valeric, isocaproic, caproic, heptanoic acids) quantified per mg faecal material or bedding.
  - Gut helminth quantification
    - Faecal flotation with sodium nitrate solution to estimate parasite eggs/oocysts per gram (EPG); multiple parasite taxa enumerated where detectable; some limitations for certain taxa (e.g., trematodes, certain nematodes).

- Reuse and GIS-focused applications
  - Spatially explicit metadata supports mapping of sampling events, trap locations, grid cells, habitats, and movement between grids.
  - Integrated microbiome and dietary/metabolite data across wild and captive settings enables map-based exploration of spatial patterns in gut microbiota, diet effects, and parasite burden.
  - Data are suitable for creating map-based data products that illustrate spatial-temporal dynamics of microbiome features, host traits, and environmental contexts in Wytham Woods and related study sites.