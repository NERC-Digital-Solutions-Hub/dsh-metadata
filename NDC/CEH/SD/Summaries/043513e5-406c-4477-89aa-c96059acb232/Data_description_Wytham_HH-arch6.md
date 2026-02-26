# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

## Overview
- A longitudinal study (2018–2019) combining tracking data and gut microbiome data from wild rodents in Holly Hill, Wytham Woods, Oxford, UK.
- Aims to understand how social contacts influence gut microbiome transmission across three rodent species (wood mice, yellow-necked mice, bank voles).
- Data types include capture and metadata, high-resolution tracking via PIT-tag loggers, vegetation/microhabitat context, and 16S rRNA gene microbiome data processed into a phyloseq object.

## Data components
- Rodent_capture_data.csv
  - Per-capture metadata: date, trap, site/grid, processing time, recapture status, ID, sex, age, species, reproductive status, PIT_tag, body measurements, ectoparasite screen results, release status, and comments.
- Logger_tag_data.csv
  - Per-logger presence records: datetime, PIT_tag/ID, logger ID, logger type (above-ground or burrow), grid location, coordinates, sex, species, date tagged, disturbance flags (trap setting, trapping day, other distractions), sample identifiers, extraction/PCR plate details.
- Vegetation/microhabitat survey data
  - Per grid cell: ground cover percentages for eight types, canopy openness, dead wood, presence/absence of other herbs and tree species, plus a table enumerating prevalent tree and herb species.
- Microbiome phenotype data
  - Mouse_microbiome_genera_phenotypes.csv detailing aerotolerance and spore-formation phenotypes for bacterial genera found in wood mouse guts, with direct and indirectly inferred annotations and references.

## Data collection and processing
- Field collection
  - Trapping over 1 year in a 4 ha Holly Hill grid (200 x 200 m); monthly to bimonthly trapping rounds with PIT-tagging for permanent identification.
  - Faecal samples collected from traps for gut microbiome analysis; strict sterilization and cold-chain handling.
- Tracking
  - 115 custom PIT-tag loggers deployed: 100 Above-ground (AG) loggers rotated biweekly across a 4 ha grid (and later within a 2.56 ha core area); 50 Burrow (B) loggers positioned at known mouse burrows in the core area (July–November 2019).
  - Logger data provide high-resolution records of space use and social associations; majority of tagged animals recorded on loggers.
- Vegetation and habitat context
  - May 2019 vegetation survey across grid cells to quantify ground cover types, canopy openness, and dead wood, enabling habitat-context analyses of social/microbial patterns.
- Microbiome data generation
  - 16S rRNA gene sequencing (V4-V5 region) from faecal samples; two-step PCR with Illumina Nextera indexing; MiSeq 2x250 bp runs.
  - DNA extraction with Zymo Quick-DNA kits; included mock community controls to assess accuracy.
- Bioinformatics and data products
  - DADA2 (version 1.14) pipeline for ASV inference; primer trimming (cutadapt), quality filtering, dereplication, merging, chimera removal; taxonomic assignment via SILVA v138.
  - Phyloseq object provided, containing ASV table, sample metadata, taxonomy table, and phylogeny.
  - Data are provided in as-raw-as-possible form; no post-processing filtering (e.g., no low-read-count filtering) has been applied.
  - Contamination issue identified: extraction plates showed bacterial DNA in controls and spatial autocorrelation of contaminants. Recommendation to decontam (threshold ~0.75) by subset (e.g., wood mouse samples + water controls) and apply to the phyloseq object prior to downstream analyses.

## Data structure and key variables
- Capture data (Wytham_HH_rodent_capture_data.csv)
  - Columns cover: Date, Trap_num, Site, Grid_square, Processing_time, New.Recapture, IDclean, Sex_clean, Age_clean, Species_clean, Reproductive_status, PIT_tag, Body_mass_g, AGD_1/2/3, Foot_1/2/3, Ectoparasite_screen and parasite counts, Released, Comments.
- Logger data (Wytham_HH_logger_tag_data.csv)
  - Columns cover: datetime, PIT_tag, ID, LOGGER_ID, logger_type (AG or B), Burrow, Gridcell, X_coord, Y_coord, Sex, Species, Date_tagged, trap_set_day, trapping_day, other_distraction, Sample_name, Sample_type, Trap_date, PIT_tag, Individual_ID, Sex_clean, Age_clean, Extraction_plate, Extraction_plate_position, Pcr_plate, Pcr_plate_position, Sequencing_batch.
- Habitat and other data
  - Vegetation/microhabitat survey provides per-grid-cell ground-cover percentages, canopy openness, dead wood, and presence/absence data for herbs and trees; Table 1 summarizes tree and herb species prevalence across the grid.
- Microbiome data
  - See processed ASV table, taxonomy, and phylogeny within the provided phyloseq object; two sequencing batches with randomization to control batch effects.
  - 424 wood mouse faecal samples from 196 individuals; 26 yellow-necked mice; 25 bank voles; 93% of wood mice in the logger dataset had microbiome samples (mean 3.1 samples/individual).
  - Mock community analysis confirms broad capture of microbial diversity; note that abundances may deviate from theoretical expectations.
- Genera phenotypes
  - Table summarizing aerotolerance and spore-formation for bacterial genera found in wood mouse guts, including direct and indirectly inferred classifications with references.

## Usage notes and caveats
- Data are provided in raw form; users should perform standard microbiome QC (e.g., decontamination, filtering) before analysis.
- Contamination risk is non-trivial due to plate-format DNA extraction; decontam-based cleaning is recommended, applied per sample type (e.g., wood mouse samples with water controls) to reduce false positives.
- Some logging coverage biases exist:
  - Burrow loggers targeted ~70% of burrows, potentially biasing detection of individual- or site-specific interactions.
  - AG-loggers rotated and repositioned; data offer high spatial resolution but require careful alignment to grid design when reconstructing networks.
- Two sequencing batches may introduce batch effects; randomization was used to mitigate, but users should account for batch in analyses.
- The phyloseq object is intentionally provided in a raw state to allow flexible preprocessing by researchers; downstream analysis can incorporate decontamination, normalization, and filtering steps as appropriate.

## Potential data products and analysis directions (Data Support perspective)
- Integrate social network data from logger records with microbiome profiles to study transmission pathways of gut microbes among individuals and species.
- Explore habitat context (vegetation, microhabitat) as moderators of social interactions and microbiome structure.
- Perform species-level or genus-level microbiome analyses, accounting for contamination, batch effects, and sample-type differences.
- Create dashboards or reusable analysis templates that link capture metadata, movement data, habitat context, and microbiome outcomes for end users.
- Use the provided phyloseq object as a starting point for reproducible microbiome analyses, with transparent documentation of preprocessing steps and contamination controls.