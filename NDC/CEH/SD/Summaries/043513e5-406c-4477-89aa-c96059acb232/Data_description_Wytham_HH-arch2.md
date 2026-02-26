# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

- Study combine tracking data and gut microbiome data from wild rodents at Holly Hill, Wytham Woods (Oxford, UK) during 2018-2019 to investigate how social contacts influence gut microbe transmission across species.

## Aim and scope

- Aim to understand social contact-driven transmission of gut microbiota in wild rodent communities and how social structure relates to microbiome composition.
- Data are interlinked across catching, tagging/tracking, and microbiome profiling, plus habitat context, enabling examination of environmental and social factors shaping microbiomes.
- Outputs include comprehensive datasets, standardized metadata, and a raw microbiome analysis object for reproducible analysis.

## Study area, species, and time frame

- Location: Holly Hill trapping grid (4 ha; 200 x 200 m) within Wytham Woods, Oxford, UK.
- Species involved: wood mice (Apodemus sylvaticus), yellow-necked mice (Apodemus flavicollis), bank voles (Myodes glareolus).
- Sampling period: November 2018 – November 2019 (fortnightly trapping; 10 months of logger data in two phases).
- Vegetation/microhabitat context captured via ground-cover surveys across grid cells.

## Data collected

- Trapping data: capture histories, individual metadata, morphometrics, reproductive status, PIT-tag identifiers, release outcomes, and other capture-related notes (Wytham_HH_rodent_capture_data.csv).
- Tracking data: time-stamped logger records linking PIT-tagged individuals to logger locations (Wytham_HH_logger_tag_data.csv).
- Metadata: individual-level and sampling-site metadata describing individuals, traps, loggers, grid cells, and temporal context (including fields like Species_clean, Sex_clean, Age_clean, PIT_tag, Logger_ID, Gridcell, etc.).
- Environment/habitat: vegetation/microhabitat survey data per grid cell, including ground cover types, canopy openness, dead wood presence, and presence/absence of plant species; Table 1 summarizes prevalence of tree and herb species across Holly Hill.
- Gut microbiota data: microbiome profiles from fecal samples across three rodent species, with 424 wood mouse samples (from 196 individuals), 26 yellow-necked mouse samples (from 17 individuals), and 25 bank vole samples (from 15 individuals); 93% of wood mice with logger data had microbiome samples.

## Microbiome sampling and sequencing

- Sample collection: fecal samples collected from traps, stored at -80°C within 8 hours of collection; strict sterilization between samples.
- DNA sequencing: 16S rRNA V4-V5 region amplified and sequenced (Illumina MiSeq) using two sequencing runs; primers 515F/926R.
- Mock controls: included positive DNA mocks to assess extraction/PCR/sequencing accuracy; negative controls included in each plate.

## Tracking and trapping methodologies

- Trapping protocol: 200 Sherman live traps arranged in an alternating checkerboard across the 4 ha grid; traps checked at dawn, contents processed, and animals released into their capture cell; occasional mortality in traps.
- PIT tagging: all captured individuals tagged with subcutaneous PIT-tags for permanent identification.
- Tracking equipment:
  - Above-ground loggers (AG-loggers): 100 units, randomly distributed across grid; rotated every two weeks to sample movement across cells.
  - Burrow loggers (B-loggers): 50 units, placed at known mouse burrow entrances in the core area; used July–November, loggers not rotated.
- Data coverage: 88% of tagged wood mice were recorded on loggers over the study period, with a mean of 23 nights of active data per individual (sd 25.3).

## Vegetation and microhabitat data

- Ground cover types recorded per 10 x 10 m grid cell (eight main types) plus open canopy and dead wood scores.
- Additional presence/absence data for other herbs and trees (tree species prevalence listed; e.g., Beech 54%, Sycamore 71%, Ash 57%, Oak 15%, etc.).
- Provides environmental context to microbiome data and potential habitat-mediated exposure differences.

## Microbiota sequencing data and preprocessing

- Data processing: two sequencing batches; DADA2 pipeline (using Cutadapt for primer trimming) to generate amplicon sequence variants (ASVs); reads trimmed to 290 bp forward, 230 bp reverse; ASVs dereplicated, merged, and chimeras removed.
- Taxonomy: assigned against the Silva v138 database; outputs compiled into a phyloseq object (raw, no downstream filtering or normalization applied yet).
- Contamination considerations: detected contamination in DNA extraction plates; evidence of spatial autocorrelation of contaminants within plates; contamination higher in extraction controls than in PCR controls.
- Recommendations: decontamination with the decontam R package is advised before analysis (subset by sample type, e.g., wood mice vs water controls, and apply decontam with threshold ~0.75); contamination likely random across biological groups but can add noise.
- Mock community visualization: sequencing captured expected diversity with some variance in relative abundances, indicating overall pipeline reliability for diversity detection.

## Datasets and data structure

- 1) Wytham_HH_rodent_capture_data.csv: cleaned capture-level dataset; rows correspond to unique capture-date events with fields like Date, Trap_num, Site, Grid_square, Processing_time, New.Recapture, IDclean, Sex_clean, Age_clean, Species_clean, PIT_tag, Body_mass_g, and various morphometrics and condition indicators.
- 2) Wytham_HH_logger_tag_data.csv: cleaned logger records; rows correspond to logger-rodent presence events with fields such as datetime, PIT_tag, ID, LOGGER_ID, logger_type (AG or Burrow), Burrow, Gridcell, X_coord, Y_coord, Sex, Species, Date_tagged, trap_set_day, trapping_day, other_distraction, Sample_name, Sample_type, Trap_date, Extraction_plate, Pcr_plate, Sequencing_batch, etc.
- 3) (Not explicitly specified in provided text; referenced as part of dataset collection)
- 4) Mouse_microbiome_genera_phenotypes.csv: phenotypic table describing aerotolerance and spore-forming traits for bacterial genera present in wood mouse gut microbiomes; includes columns for Bacterial_genus, Aerotolerance_detailed, Aerotolerance_strict, Spore_formation, Gram_stain, Reference, and notes on indirect inferences and comments.

## Outputs and usage notes

- Core output: a raw phyloseq object containing ASV table, sample metadata, taxonomy table, and phylogenetic tree for downstream microbiome analyses.
- Data utility: enables analyses linking social network data (via tracking and trap data) to gut microbiome composition across multiple small mammal species, in a well-characterized habitat context.
- Data accessibility: materials include full methodological details, data fields, and example data files to support reproducibility and re-use in environmental monitoring and ecological health assessments.

## Relevance to environmental monitoring analysts

- Demonstrates a comprehensive, standardized approach to environmental data integration: capture/labeling, movement tracking, habitat context, and microbiome profiling.
- Emphasizes data quality assurance, transparent preprocessing, and explicit caveats about technical noise (contamination) and batch effects, aligning with standard monitoring practices.
- Highlights the importance of metadata management and sharing raw data objects (phyloseq) to enable scrutiny, cross-study comparisons, and policy-relevant analyses of ecosystem health and host-microbiome dynamics.
- Addresses challenges relevant to monitoring data value: combining diverse data streams (trapping, movement, microbiome, habitat) and enabling access to underlying data for secondary use.