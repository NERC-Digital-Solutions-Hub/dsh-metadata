# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

- A multi-component data set combining tracking data, microbiome data, and related metadata from wild rodents at Holly Hill, Wytham Woods, Oxford UK (2018-2019). Objects include rodent movement/social data, gut microbiota profiles, environmental context, and sequencing/processing details. Also provides raw phyloseq object and guidance for decontamination.

## Study design and data collection

- Study area and period
  - 4 ha study grid (200 x 200 m) in Holly Hill, Wytham Woods; tracking Nov 2018–Nov 2019.
- Species
  - Wood mice (Apodemus sylvaticus), yellow-necked mice (Apodemus flavicollis), bank voles (Myodes glaerololus).
- Trapping protocol
  - Trapping every 2–4 weeks using 200 Sherman traps; PIT-tags for permanent ID; faecal samples collected at trapping and stored at -80°C within 8 hours.
  - Data include capture time, morphology, reproductive status, body measurements, and release outcomes.
- Tracking and social interaction data
  - 115 custom PIT-tag loggers deployed; logged rodent presence within ~1 m2 detection field.
  - Two logging schemes:
    - Above-ground loggers (AG): 100 units, even checkerboard distribution, rotated to improve spatial resolution.
    - Burrow loggers (B): 50 units placed at known burrows (core area only), recording around burrows with uneven spatial coverage.
  - Coverage: 88% of tagged wood mice recorded on loggers; mean around 23 nights per individual (SD ~25).
- Vegetation/microhabitat survey
  - Per 10 x 10 m grid cell: percent cover of eight ground cover types, open canopy, dead wood; presence/absence of other herbs and trees; prevalence data for many species (trees and herbs) mapped to grid cells.

## Data types and contents

- Trapping data
  - Wytham_HH_rodent_capture_data.csv: per-capture records including date, trap, site/grid cell, processing time, recapture status, ID, sex/age/species, reproductive status, PIT tag, body measurements, ectoparasite screening, release status, and comments.
- Logger data
  - Wytham_HH_logger_tag_data.csv: per-logger per-rodent presence events with timestamp, PIT tag, logger ID, logger type (AG or Burrow), burrow ID, grid cell, coordinates, sex/species, tagging date, trap/distraction flags, sample identifiers, and sequencing batch references.
- Vegetation/microhabitat data
  - Per-grid summaries of ground cover types, canopy openness, dead wood, and presence/absence of additional flora; includes a table of tree and herb species prevalence across the Holly Hill site.
- Gut microbiota data
  - Gut microbiota was characterized from:
    - 424 wood mouse faecal samples (196 individuals)
    - 26 yellow-necked mouse samples (17 individuals)
    - 25 bank vole samples (15 individuals)
  - 93% of wood mice in logger data had microbiome samples (153/164 with an average of 3.1 samples per mouse; range 2–10).
- Sequencing and microbial phenotype data
  - 1) Mouse_microbiome_genera_phenotypes.csv: aerotolerance and spore-formation phenotypes for bacterial genera present in wood mouse gut; includes direct and indirectly inferred annotations, Gram stain, and literature references.
  - 2–4) Metadata and phenotypic tables describing sequencing batches, plate layouts, and taxonomic associations (as described in text).

## Data processing and sequencing

- DNA extraction, library prep, and sequencing
  - DNA extraction using Zymo Quick-DNATM Fecal/Soil Microbe kits on 96-well plates; included mock community controls.
  - Two-step PCR targeting V4-V5 region of 16S rRNA (primers 515F/926R); dual-indexing with Illumina Nextera primers; 2 x 250 bp MiSeq sequencing.
  - Randomization across plates to detect technical effects; two sequencing batches (HH1 and HH2) spanning different study periods.
- Bioinformatics and preprocessing
  - Data processed with DADA2 (v1.14): primer trimming with cutadapt, quality filtering, dereplication, ASV inference, merging, chimera removal.
  - Taxonomy assigned against SILVA (v138); creation of a phyloseq object combining ASV table, metadata, taxonomy, and phylogeny.
  - The phyloseq object is provided with the dataset and is intentionally kept as raw as possible (no filtering or normalization applied yet).
- Contamination and data quality notes
  - Evidence of contamination in extraction plates (bacterial DNA detected in controls; spatial autocorrelation of contaminants within plates).
  - Contamination likely via lysis step; could add random technical noise and obscure real differences.
  - Recommendation: decontam package (threshold p = 0.75) to filter contaminants, applied per sample type (e.g., wood mice only with water controls). Subset data accordingly before decontamination.
  - Mock community visualization indicates overall capture of diversity, with some discrepancies in relative abundances.

## Usage notes, limitations, and data governance

- Linking and integration
  - Datasets are interconnected: captures link to logger records and to microbiome samples; environmental data provides context for habitat.
- Design limitations and potential biases
  - Burrow logger coverage excludes ~30% of burrows, potentially biasing capture of some individuals.
  - Logging effort and rotation may introduce temporal/spatial biases in movement inferences.
- Data availability and formats
  - Includes both raw/structured CSV data and the raw phyloseq object for microbiome analysis.
  - Clear documentation of field methods, sequencing methods, and data processing steps to support reproducibility and re-use.

## End-to-end summary

- This data package provides an integrated, multi-modal data set describing wild rodent social networks and gut microbiomes, with detailed field protocols, sequencing methods, and metadata. It enables analyses of how social contact and space use relate to gut microbiota composition, while offering guidance on data processing and contamination handling for robust reuse in data-led analytics and cross-institutional collaborations.