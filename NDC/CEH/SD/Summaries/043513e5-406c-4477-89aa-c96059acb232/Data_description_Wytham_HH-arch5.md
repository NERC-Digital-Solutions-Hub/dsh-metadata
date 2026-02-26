# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

## Overview
- Combined dataset of tracking data, gut microbiome data, and metadata from wild rodents (wood mice Apodemus sylvaticus, yellow-necked mice Apodemus flavicollis, bank voles Myodes glareolus) at Holly Hill, Wytham Woods, Oxford, UK, 2018–2019.
- Study goal: assess how social contacts influence gut microbe transmission in a wild setting.
- Data components: capture and individual metadata, RFID/PIT-tag tracking data, gut microbiome profiles (16S rRNA V4–V5), vegetation/microhabitat surveys, and related phenotypic data for microbiome genera.
- Processed by Aura Raulo; sequencing by Liverpool Centre for Genomics Research; provided as CSVs and a phyloseq object for microbiome data.
- Includes notes on data quality and contamination with guidance for re-use.

## Data collection and study design
- Trapping
  - 1-year period (Nov 2018–Nov 2019) on a 4 ha Holly Hill grid; 200 Sherman traps; traps checked fortnightly to monthly.
  - Individuals tagged with PIT-tags for permanent identification; faecal samples collected and stored at -80°C within 8 hours; sterile handling; measurements and reproductive status recorded; release back to capture location.
  - Data collected: species, sex, age, weight, body measurements, reproductive status, release outcomes, and capture details.
- Tracking
  - 115 custom PIT-tag loggers deployed to record spatial use and social associations.
  - Above-ground loggers across the grid Feb 2019–Jun 2019; rotation planned to improve spatial resolution.
  - Burrow loggers across the 2.56 ha core area Jul–Nov 2019; approximately 70% of mouse burrows covered.
  - Coverage: 88% of wood mice tagged since early 2019 were recorded on loggers; mean nights of active data per individual around 23.
  - Logger hardware details: ~1 m2 detection field; 124 kHz PIT-tags; periodic “I’m alive” signals to monitor battery life.
- Vegetation/microhabitat survey
  - May 2019 survey across grid cells; measured percent cover for eight main ground types, canopy openness, and amount of dead wood.
  - Documented plant and tree species presence/absence; Table 1 lists prevalence by species.
- Gut microbiota characterisation
  - DNA extraction, library preparation, and sequencing conducted in two batches using Illumina MiSeq (2x250 bp).
  - Included mock communities for QC; negative controls monitored.
  - Microbiome data available for 424 wood mice (196 individuals), 26 yellow-necked mice (17 individuals), 25 bank voles (15 individuals); 93% of wood mice with logger data had microbiome samples.
  - Sequencing and bioinformatics pipelines described (DADA2, SILVA v138); two sequencing batches with randomization to control batch effects.

## Data products and structure
- Wytham_HH_rodent_capture_data.csv
  - Capture-level data per event with fields such as Date, Trap_num, Site, Grid_square, PIT_tag, Sex_clean, Age_clean, Species_clean, Reproductive_status, Body_mass_g, Released, and Comments.
- Wytham_HH_logger_tag_data.csv
  - Logger records per rodent: datetime, PIT_tag, ID, LOGGER_ID, logger_type (AG or B), Burrow, Gridcell, X_coord, Y_coord, Sex, Species, Date_tagged, trap_set_day, trapping_day, other_distraction, Sample_name, Sample_type, Trap_date, PIT_tag, Individual_ID, Sex_clean, Age_clean, Extraction_plate, Extraction_plate_position, Pcr_plate, Pcr_plate_position, Sequencing_batch.
- Gut microbiota data (processing and outputs)
  - Raw sequencing data processed with DADA2; ASV table, taxonomy table (SILVA 138), sample metadata, and a phyloseq object provided for downstream analyses.
  - Note: the phyloseq object is provided in its raw form (no filtering beyond initial processing).
- Mouse_microbiome_genera_phenotypes.csv
  - Aerotolerance and spore-formation phenotypes for bacterial genera found in the wood mouse gut; includes direct and indirect inferences, Gram-stain and references.
- Vegetation/microhabitat data (grid-level survey)
  - Grid-cell level habitat variables (ground cover types, open canopy, dead wood, plant species presence) with prevalence data (Table 1).
- Related and supplementary notes
  - Related dataset: Wild rodent trapping data (Wytham Woods) linked for broader context.
  - Detailed methodology chapters (Raulo et al., 2022, Chapter 3) for lab and field protocols.

## Data processing, quality control, and limitations
- Microbiome processing
  - Two sequencing batches; DNA extraction with Zymo kit; inclusion of mock communities; two-step PCR targeting V4–V5 region; sequencing on MiSeq.
  - Data processing via DADA2: primer/adaptor trimming, ASV inference, chimera removal, and SILVA-based taxonomy assignment; outputs compiled into a phyloseq object.
  - Contamination issues identified: bacterial DNA detected in extraction controls; spatial autocorrelation of contaminants within extraction plates.
  - Recommendations for users: decontam R package to identify/filter contaminants, applied per sample type (e.g., wood mouse vs. water controls) to reduce technical noise.
  - Mock community results indicate the pipeline captures major diversity but with some variance in relative abundances.
- Data quality and reproducibility
  - The provided phyloseq object is intentionally raw; downstream filtering (e.g., low-abundance taxa, sample filtering) is left to the user.
  - Detailed cross-batch design information supports assessment of batch effects and reproducibility.

## Metadata, governance, and access
- Metadata and linking keys
  - Consistent use of PIT_tag and Unique IDs (ID, Sample_name, Extraction_plate, Pcr_plate) to enable cross-dataset linking.
  - Clear column definitions, units, and data types (dates, coordinates in meters, measurements in mm/g).
- Provenance and reproducibility
  - Documented data-processing steps and software versions (DADA2 v1.14; Cutadapt; SILVA v138; phyloseq) to aid reproducibility.
  - Field and lab protocols summarized, with full protocol context available in Raulo et al. (2022) Chapter 3.
- Access and reuse
  - Data released with accompanying metadata, sample identifiers, and a raw microbiome phyloseq object; guidance and references provided for proper use.

## Practical considerations for Data Stewards
- Maintain versioning and accessibility of the CSV files and the phyloseq object; clearly record any updates or corrections.
- Preserve cross-dataset linkage through robust keys (PIT_tag, ID, Sample_name, Extraction_plate, Pcr_plate).
- Document contamination notes and the recommended decontamination workflow to support correct data interpretation.
- Provide clear data-use citations, especially Raulo et al. (2022) Chapter 3 and the associated software references.