# Details on data collection:

- Scope and datasets
  - Data collected 2014-2018 on wood mice (Apodemus sylvaticus) and other small mammals in Wytham Woods, Oxfordshire (with additional habitat grids in 2018) and related data from Silwood Park.
  - Main components: 3 linked studies
    - Longitudinal trapping study (2015-2018): fortnightly captures in a 100 m² grid; faecal samples for gut microbiota, diet, and parasite infections.
    - Dissection study (2017-2018): euthanized individuals; regional GI tract sampling for microbiota and helminths across five gut sections.
    - Diet shift experiment (2017): captive wood mice in a lab; five diet treatments varying seed (peanut) vs insect (mealworm) content; microbiota and metabolite analyses.
  - Associated data from Silwood Park (Project 1: Wild rodents social networks and microbiome).

- Field and laboratory methods
  - Longitudinal trapping
    - Sherman live traps set in a checkerboard design; biweekly to monthly checks; PIT-tags for identification; processing included species/sex/weight/age, and release in the original grid cell.
    - Faecal samples collected at trapping, stored at -80°C within 8 hours.
  - Dissection study
    - Ethical, PIT-tagged juveniles/pregnant/lactating mice excluded; euthanasia via pentobarbital and cervical dislocation.
    - GI tract divided into five sections (duodenum to colon) with tissue for microbiota and gut contents stored at -80°C; helminth burden stored in 70% ethanol.
  - Diet shift experiment (lab)
    - Outbred mice in semi-barrier housing; five diets with varying seed (peanut) and insect (mealworm) content; 25-day perturbation followed by a 5-day recovery.
    - Daily sampling: faecal microbiota and bedding for metabolites; body mass and food intake recorded; humane euthanasia at end.
  - Ethics
    - Dissection and diet experiments approved by relevant ethics boards and Home Office licenses as stated.

- Data types and measurements
  - Microbiome
    - 16S rRNA gene (V4 region) amplicon sequencing; two-step library prep; dual-indexing; Illumina MiSeq runs (2x250 bp).
    - Four MiSeq runs total; samples processed in two batches (experimental + early year samples; later year + dissection samples).
    - DNA extraction using Zymo Quick-DNATM kits with bead beating; controls included (mock community and negative control).
    - Bioinformatics via DADA2: primer trimming, quality filtering, ASV inference, chimera removal; taxonomy assigned against SILVA 138; produced a phyloseq object with raw-like data (no aggressive preprocessing like zero-removal or rarefaction).
  - Diet characterisation and metabolites
    - Faecal metabolite profiling via GC-FID with internal standard; targeting short-chain fatty acids (acetic, propionic, isobutyric, butyric, etc.).
    - Faecal and bedding samples used for metabolite concentrations; internal standard and extraction efficiencies applied.
  - Gut helminths
    - Faecal flotation in sodium nitrate solution to detect nematodes, cestodes, Eimeria spp.; eggs/oocysts counted per gram (EPG) where possible.
  - Host and environmental metadata
    - Detailed trapping metadata: date, trap ID, grid, habitat type, PIT tag, animal ID, species, sex, age, body mass, reproductive status, ectoparasite screen results, and trap/bait metrics.
    - For dissection and longitudinal data: same core morphometrics and parasite measures; detailed GI tract sampling data.
  - Diet shift dataset
    - 30-day protocol with daily data per mouse: diet type, day, date, housing changes, time of processing, body weight, body condition, jar weight, food intake, food left, top-up, fresh faecal matter and bedding faecal matter masses, sampling times, and notes.
    - Metabolite data (faecal acetic, propionic, isobutyric, butyric, isovaleric, valeric, isocaproic, caproic acids) and total SCFA; parasite-related measurements included as applicable.

- Data organization and access
  - Project_4_processed_microbiome_data.rds
    - A phyloseq object containing ASV counts, taxonomy (SILVA-based), sample metadata, and reference sequences.
    - Minimal preprocessing beyond removal of non-gut taxa (chloroplast/mitochondria); raw-like dataset ready for further filtering/normalization.
  - Wytham_longitudinal_sample_metadata.csv
    - Per-trapping-event metadata including Sequence_sample_code, collection_date, trap, grid, habitat_type, PIT_tag, Animal_ID, Species, Sex, Age, Reprod, Body_mass_g, AGD measurements, ectoparasite counts, and sampling particulars.
  - Full_Wytham_trapping_data.csv
    - Comprehensive trap-by-trap records including data entry details, trap outcomes, morphometrics, ecto-parasite screens, diet/bait measures, parasite data, tissue/bedding samples, release information, and processing times.
  - Diet_shift_experiment_2017_metadata.csv
    - 30-day diet-shift experiment per-animal data: Seq_ID, Mouse.ID, Day_of_experiment, Date, Intervention, Shift_period, Diet.type, Hours_since_intervention, Group, Sex, Cage_of.origin, Time.mouse.processed, Body.weight, Body.condition, Jar.weight, Weight.of.food, Food intake, Food left, Top up, Fresh poo and Bedding poo metrics, and multiple metabolite measurements (acetic, propionic, isobutyric, butyric, isovaleric, valeric, isocaproic, caproic acids, Total SCFA).

- Data considerations and limitations
  - Data counts and sample sizes are partially unspecified in the methodology text (placeholders such as XXX indicate that exact numbers are not disclosed here).
  - Sequencing and extraction occurred in two batches, which may introduce batch effects; the provided phyloseq object is intentionally near raw to allow custom preprocessing.
  - Variation in gut sampling (longitudinal vs dissection) and diet experiments introduces heterogeneity that analysts should account for in comparative analyses.
  - Ethical approvals and licenses are noted for dissection and diet experiments.

- Analytical opportunities
  - Correlations between gut microbiota composition (ASVs) and diet history, habitat type, and parasite burden across five gut regions.
  - Longitudinal assessment of microbiome dynamics in wild vs. lab conditions, including diet-induced shifts and metabolite associations.
  - Integration of microbiome data with host traits (weight, body condition, reproductive status) and ectoparasite load.
  - Exploration of gut metabolite profiles (SCFA) in relation to microbiome structure and diet treatment.
  - Cross-dataset analyses leveraging the metadata richness to control for batch effects and sampling frame.

- Usage notes for analysts
  - Leverage the phyloseq object for flexible microbiome analyses; apply standard preprocessing (e.g., filtering low-prevalence ASVs) as needed for robust statistics.
  - Use the detailed sample metadata to align samples across datasets; note batch information (Miseq_batch, Miseq_run, DNA_extraction_date, Extraction_format) to mitigate confounding.
  - Consider hierarchical modeling to accommodate repeated measures (longitudinal data) and multiple gut sites (dissection) within the same individuals.