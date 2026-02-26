# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

- A comprehensive dataset combining tracking data, gut microbiome profiles, and environmental metadata from wild rodents (wood mice, yellow-necked mice, bank voles) captured at Holly Hill, Wytham Woods, 2018–2019.
- Aimed at studying how social contacts influence gut microbiome transmission in a wild setting, with additional vegetation/microhabitat context and bacterial phenotype information.

## Study site and sampling design

- Location and scale: 4-hectare study grid (200 x 200 m) at Holly Hill, Wytham Woods, Oxford, UK; core area of 2.56 ha used for intensive logger deployment.
- Rodent trapping: approximately fortnightly trapping over 12 months (Nov 2018–Nov 2019) using Sherman live traps; processed animals recorded with species, sex, age, weight, reproductive status, and PIT-tag identification.
- Sample collection: faecal samples collected at trapping and preserved for microbiome analysis; traps sterilized between sessions.
- Captures: 187 captures with 167 tagged since early 2019; 88% of tagged individuals recorded on loggers; mean nights with data per individual ~23 (SD 25.3).

## Tracking and social association data

- Tracking devices: 115 custom PIT-tag loggers recording rodent presence within ~1 m2 detection fields.
- Logger deployment:
  - Above-ground loggers (AG): 100 loggers in a checkerboard across the grid; rotated every two weeks to sample fine-scale movement; no lure used to record random movement.
  - Burrow loggers (B): 50 loggers deployed on known burrows from July–November 2019 to capture spatially explicit behavior around burrows; distributed across the core area.
- Logging schemes:
  - February 2019–June 2019: AG loggers across the full 4 ha area.
  - July 2019–November 2019: core area (2.56 ha) with AG and burrow loggers in roughly equal spatial coverage.
- Data: logger records tied to individual PIT-tags, with timestamps; grid-cell and burrow metadata recorded to enable social network reconstruction.

## Vegetation and microhabitat data

- Habitat survey conducted in May 2019 for each 10 x 10 m grid cell.
- Variables collected:
  - Percentage cover for eight ground-cover types (e.g., open ground, bluebell, bramble, grass, sedge, Enchanter's nightshade, wild garlic, currant).
  - Presence/absence of additional herbs and trees, canopy openness, and dead wood amount.
- Tree and herb prevalence summarized for the study area (e.g., Beech, Sycamore, Ash, Oak, Hawthorn, etc.; notable frequent taxa listed with overall prevalence percentages).
- Resulting habitat context data to relate to rodent behavior and microbiome variation.

## Gut microbiota characterization

- Sample scope: 424 wood mouse faecal samples (from 196 individuals), 26 yellow-necked mouse faecal samples (from 17 individuals), 25 bank vole faecal samples (from 15 individuals); 93% of wood mice with logger data had microbiome samples.
- Sequencing approach: two sequencing batches of 16S rRNA gene (V4–V5) amplicons using Illumina MiSeq (2x250 bp).
- DNA extraction and library prep: standardized 96-well plate protocol with mock community controls; quality checked via Qubit and gel electrophoresis.
- Data processing: DADA2 (v1.14) pipeline for quality filtering, dereplication, ASV inference, and chimera removal; taxonomic assignment against SILVA v138; results compiled into a phyloseq object (raw form, without downstream filtering or normalization).
- Contamination issue: detected contamination in extraction plates leading to spatial autocorrelation of contaminant ASVs; contamination tends to be higher in extraction controls and can introduce technical noise.
- Recommendation: decontam package (threshold ~0.75) to identify and remove contaminants; apply separately to each sample type (e.g., wood mice vs. water controls) before downstream analysis.

## Data files and metadata

- 1) Wytham_HH_rodent_capture_data.csv
  - Per-capture records with fields for date, trap, grid cell, processing time, recapture status, PIT tags, sex, age, species, reproductive status, body measurements (mass, AGD, feet), ectoparasite screening, release status, and comments.
- 2) Wytham_HH_logger_tag_data.csv
  - Per-logger-records: datetime, PIT_tag, individual ID, logger ID, logger type (AG or Burrow), burrow ID, grid cell, coordinates, sex, species, date tagged, trap/handling indicators, and distraction flags.
- 3) Mouse_microbiome_genera_phenotypes.csv
  - Phenotypes for bacterial genera present in wood mouse gut microbiota: aerotolerance (OA/FA/MA/A), spore formation (SF/NSF/mixed/unknown), Gram-stain (Negative/Positive), with direct/indirect inferences and references.
- 4) Phyloseq object and associated microbiome tables (raw)
  - ASV table, taxonomy, sample metadata, and phylogenetic tree packaged for reproducible microbiome analysis (not pre-filtered).
- Additional contextual data: vegetation/microhabitat table and a table detailing genus-level microbiome phenotypes.

## Data quality, caveats, and analysis considerations

- Contamination and batch effects: plate-based DNA extraction introduced contamination; biases may appear as technical noise but can be mitigated with decontamination and careful subsetting by sample type.
- No a priori filtering: the provided phyloseq object is intentionally raw to allow researchers to apply their own quality control (e.g., filtering by read count, prevalence, or taxonomy).
- Data integration: combining social network data from loggers with gut microbiome data enables analyses of associations between social connectivity and microbial composition, while accounting for habitat context and host traits.
- Temporal and spatial design: multi-month logging with rotating AG loggers and burrow-focused sampling provides both random movement and burrow-centered data, enabling more nuanced network inferences.
- Documentation and reproducibility: detailed field methods, sequencing protocols, and bioinformatics steps are described, with references to standard pipelines (DADA2, decontam, phyloseq) to support reproducibility.

## Practical implications for analysis

- Potential analyses:
  - Relate social network metrics (e.g., centrality, contact rates) to microbiome diversity and ASV/phyla-level composition.
  - Examine habitat covariates (ground cover, canopy openness, dead wood) as moderators of social-microbiome associations.
  - Compare microbiome profiles across rodent species and across different logger types (AG vs. Burrow).
  - Use the genus-phenotype data to interpret ecological traits of the microbiome (aerotolerance and spore formation) in relation to host ecology.
- Quality control steps to perform:
  - Subset phyloseq object by sample type and apply decontam to identify potential contaminants.
  - Consider batch effects between the two sequencing runs and incorporate sequencing batch as a covariate.
  - Apply appropriate normalization or transformation for downstream diversity and differential abundance analyses.

## References and methodological notes

- Data and methods align with established microbiome analysis workflows (DADA2 for ASV inference; SILVA for taxonomy; phyloseq for data integration).
- Contamination considerations follow recommendations to use decontam and to handle plate-based extraction noise.
- Sequencing and primer choices correspond to V4–V5 region targeting 16S rRNA gene.