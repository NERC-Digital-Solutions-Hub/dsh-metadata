# Wild rodents social networks and the microbiome

- A study combining trapping, tracking, and microbiome profiling of wild rodents to understand gut microbe transmission through social contacts in a natural setting (Silwood Park, 2014–2015).
- Field site: 2.47 ha Nash's Copse woodland at Imperial College Silwood Park; multiple rodent species captured in a 100 m2 grid with point-in-time sampling and continuous spatial monitoring.

- Field data collection and sampling
  - Trapping: fortnightly sessions using 122 Sherman traps; each rodent identified to species, sexed, weighed, aged; PIT-tags implanted for permanent identification; ear punches collected for genotyping; faecal samples collected within 8 hours of capture and stored appropriately.
  - Live-trapping logistics: traps set dusk, retrieved at dawn; sterilization and fresh bedding routines; alternating checkerboard trap layout to ensure even coverage.
  - Spatial recording: grid-based positioning with trap/location metadata and trap-night conditions (rain, temperature, soil moisture).

- Social and spatial tracking (loggers)
  - Nine custom PIT-tag loggers distributed across the grid to record presence of tagged rodents at 0.3-second intervals.
  - Loggers rotated with predefined territories (27 grid cells per logger; 9 loggers cover 243 cells total) to achieve even spatial coverage; precise logger position within a cell randomized at each rotation.
  - Rotation schedule: approximately 3.54 times per week; rotations occur during daytime to minimize nocturnal disturbance; data from nights with multiple consecutive nights in one location treated conservatively to maintain coverage.
  - Data cleaning: removal of corrupt reads and filtering of non-logged nights to align with trapping data; final dataset included 83 of 93 tagged mice.

- Kinship and genetic relatedness
  - Genotyping: ear tissue from wood mice analyzed at 11 microsatellite loci; COLONY used for pedigree reconstruction accounting for polygamy and genotyping error.
  - Kinship results: after resolving conflicts with trapping data, pedigree comprised 17 mother–pup, 14 father–pup, 13 full-sibling, and 26 half-sibling relationships.
  - Kinship matrix: dyadic relatedness converted to numeric distances (e.g., 0.5 for parent-offspring/full-siblings; 0.125 for half-siblings/cousins).

- Microbiome profiling
  - Sampling: 239 faecal samples from 75 individuals (≈90% of monitored mice); mean 3.2 samples per mouse (range 1–9).
  - Library preparation and sequencing: extraction, two-step 16S rRNA V4 region amplification ( primers N515F/N806R ); inclusion of multiple controls (extraction, PCR, mock communities); 2x250 bp Illumina MiSeq sequencing with dual indices.
  - Bioinformatics: DADA2 pipeline with trimming, dereplication, ASV inference; taxonomic assignment via GreenGenes; removal of low-count sample and non-gut taxa; normalization to proportional abundances; diversity analyses (iNEXT) confirmed adequate sampling depth.
  - Data outputs: ASV table with taxonomic assignments, read depths, alpha diversity estimates, and sample metadata.

- Datasets and data structure
  - silwood_rodent_trapping_data.csv: trap-night level data including site, trap details, species, sex, age, PIT-tag, body metrics, reproductive status, ectoparasite data, trap timings, and environmental context.
  - silwood_rodent_capture_data.csv: capture-event level data including grid location (X/Y), ID, PIT-tag(s), species, sex, age, trapdate, and coordinates.
  - silwood_logger_data.csv: per-record logger data with timestamp, rodent ID and PIT-tag, logger ID, grid location and coordinates, logger territory, and sample date/time metadata.
  - Kinship and microbiome data (implied): pedigree-derived kinship distances; microbiome ASV counts, taxonomic classifications, sample metadata, and diversity metrics.
  - Data quality notes: discusses filtering steps, read-depth thresholds, and exclusion criteria to ensure robust downstream analyses.

- GIS and spatial-analysis relevance for GIS specialists
  - Spatial framework: 2.47 ha plot partitioned into 100 m2 grid cells; logging territories map to nine logger areas with explicit X/Y coordinates for traps, loggers, and grid cells.
  - Data fusion potential: link trapping events, logger co-occurrence data, spatial positions, and kinship/relatedness to analyze spatial-social networks and potential microbe transmission paths.
  - Temporal dynamics: timestamped records enable time-resolved network analyses and movement patterns; rotation schedules provide systematic sampling design for spatial coverage assessment.
  - Data outputs suitable for map-based visuals: spatial networks (social proximity, logger co-presence), kinship-informed dyadic networks, and microbiome composition maps across space and time.
  - Data-quality and preprocessing transparently documented: stepwise filtering, binning by nights, and QC checks support reproducible GIS-centric analyses.

- Considerations and limitations
  - Logger breakage (April–May 2015) reduced spatial coverage temporarily.
  - Some nights/trapping nights filtered to maintain even coverage and reduce bias.
  - Genotyping success limited to 70 of 83 monitored individuals; pedigree reconstruction accounts for uncertainty and potential inbreeding.
  - Microbiome data derived from 239 samples may have uneven sampling across individuals, but the dataset provides substantial depth for network-microbiome associations.

- Overall utility
  - The integrated dataset enables analyses of how social structure, spatial proximity, and kinship shape gut microbiome transmission in wild rodent populations.
  - Provides rich GIS-ready metadata (locations, territories, movement patterns) alongside genetic and microbiome data for comprehensive spatial-network investigations.