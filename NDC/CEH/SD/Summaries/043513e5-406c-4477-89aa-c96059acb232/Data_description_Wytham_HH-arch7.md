# Wild rodents social networks and the microbiome (Wytham Woods, Holly Hill)

## Overview
- A multi-faceted data package from 2018-2019 in Holly Hill, Wytham Woods, combining rodent movement/social tracking with gut microbiome data and habitat context.
- Key objectives: study how social contacts influence gut microbiota transmission across three rodent species (wood mice, yellow-necked mice, bank voles) in a wild setting.
- Data tiers include trapping and individual metadata, high-resolution tracking with PIT-tag loggers, vegetation/microhabitat surveys, and microbiome profiles (16S rRNA gene) from faecal samples.
- Additional phenotypic data for bacterial genera (aerotolerance and spore-formation) provided for contextual interpretation of microbiome results.
- Lab and bioinformatics pipelines documented; data provided with notes on contamination and data preparation.

## Spatial extent and data layers
- Study area: 4-hectare Holly Hill grid (200 m x 200 m) within Wytham Woods; core area of 2.56 hectares used for intensive logging.
- Spatial framework:
  - 10 m x 10 m grid cells (grid squares) as fundamental spatial units.
  - Logger locations with X, Y coordinates in meters from grid origin; gridcell identifiers (10x10 m cells).
  - Burrow logger placements at known mouse burrows across the core area.
  - Trap grid locations and grid-square codes for capture data.
- Habitat and vegetation layers per grid cell:
  - Ground cover types (open ground, dog’s mercury, bluebell, bramble, grasses, sedge, Enchanter’s nightshade, wild garlic, currant).
  - Canopy openness, dead wood presence, and presence/absence of other flora with frequency across grid cells.
  - Table of specific tree and herb species prevalence by grid cell.

## Data structure and key variables
- Datasets described:
  - Wytham_HH_rodent_capture_data.csv: per-capture records with date, trap, site, grid cell, processing times, unique animal IDs, PIT-tag history, sex, age, species, reproductive status, body measurements, Ectoparasite data, release status, and qualitative comments.
  - Wytham_HH_logger_tag_data.csv: per-logger record linking individual rodent (PIT_tag/ID) to a logger (LOGGER_ID), logger type (AG = above-ground, B = burrow), position within grid, coordinates (X/Y), demographic attributes, and trap/tracking context flags.
  - Data files describing microbiome results and sample metadata (see below).
  - Mouse_microbiome_genera_phenotypes.csv: phenotypic traits (aerotolerance and spore-formation) for bacterial genera detected in the wood mouse gut, including direct/indirect inferences and literature references.
- Microbiome output:
  - Gut microbiota characterized for 424 wood mice (196 individuals), 26 yellow-necked mice (17 individuals), and 25 bank voles (15 individuals).
  - Most wood mice with microbiome data had multiple samples (mean ~3.1 per individual; 93% of logger-recorded wood mice had microbiome samples).
  - Data processing yields a phyloseq object (raw form) containing ASV tables, sample metadata, taxonomy, and phylogeny (no downstream normalization or filtering applied in the provided object).

## Data collection and processing workflows
- Field collection:
  - Trapping conducted Nov 2018–Nov 2019 in a checkerboard 200 m x 200 m grid with Sherman traps; marked animals with PIT-tags for permanent identification.
  - Faecal samples collected at each trapping event, preserved and stored for microbiome analysis.
  - 115 PIT-tag loggers deployed to monitor spatial movement and social associations; loggers rotated biweekly to vary spatial coverage; burrow loggers added in mid-term to capture burrow-associated activity.
  - Vegetation/microhabitat surveyed in May 2019 for each 10x10 m cell.
- Tracking:
  - Logger system captured time-stamped detections of tagged rodents within ~1 m2 read field.
  - 88% of wood mice tagged since early 2019 were recorded on loggers; logging yielded nights of activity per individual.
- Microbiome lab workflow:
  - DNA extraction from faecal samples using 96-well plate kits with mock community controls.
  - Two-step PCR targeting 16S rRNA V4-V5 region (primers 515F/926R); duplicates pooled; indexing with Illumina Nextera primers.
  - Sequencing on Illumina MiSeq (2x250 bp reads) across two batches.
- Bioinformatics and preprocessing:
  - DADA2 pipeline used for ASV inference; primer trimming and quality filtering; chimeric sequence removal.
  - Taxonomy assigned against SILVA database; outputs consolidated into a phyloseq object.
  - Contamination noted: extraction plates showed contaminant ASVs; strong evidence of plate-level spatial autocorrelation for contaminants; recommendation to decontaminate phyloseq object before downstream analysis (e.g., using the decontam package) and to subset by sample type when applying decontamination.
- Mock and data quality checks:
  - Visualization of mock community profiles indicated capture of microbial diversity, with some deviations from theoretical abundances.

## Microbiome data specifics and caveats
- Contamination and noise:
  - Contamination more pronounced in extraction controls; spillage during lysis likely source.
  - Technical noise could obscure some biological differences; decontamination advised prior to analysis.
- Data objects and access:
  - Phyloseq object provided in raw form; users may apply their own filtering and normalization steps as needed.
- Phenotype mapping:
  - Genera-level aerotolerance and spore-formation data linked to microbiome genus observations via the provided phenotype table, with indirect inferences clearly annotated.

## Data integration and GIS relevance
- Spatially explicit data enable map-based visualization and analyses:
  - Map rodent movements and social associations using logger data integrated with capture metadata.
  - Overlay microbiome sampling locations (faecal sample sites) with habitat layers (ground cover, canopy openness, dead wood) and grid-cell attributes.
  - Visualize burrow-associated versus random movement patterns and their relation to microbiome composition.
  - Examine spatial biases: burrow logger deployment covered ~70% of burrows; logging effort and sample collection timing can influence spatial exposure and sampling density.
- Potential GIS products:
  - Layered maps of logger detections, trap locations, burrows, and grid-cell habitat features.
  - Network graphs of social contacts derived from co-occurrence in loggers, linked to individual microbiome profiles.
  - Heatmaps of microbiome metrics (e.g., alpha diversity, taxa abundances) across grid cells or around burrows.
  - Temporal animation of movement, social interactions, and sampling windows.

## Data quality, limitations, and cautions
- Spatial coverage:
  - Intensive data restricted to 2.56 ha core area for part of the study; initial 4 ha grid provides broader context.
- Logging design:
  - Burrow loggers offer biased coverage toward known burrows, which may influence perceived contact patterns.
- Sampling cadence:
  - Fortnightly trapping with variable sampling windows; temporal mismatches between movement data and microbiome sampling may affect interpretation.
- Lab and sequencing limitations:
  - Two sequencing batches with potential batch effects; randomization across plates implemented to mitigate; contamination highlights the need for careful preprocessing.

## Summary of data products
- High-resolution spatial dataset enabling mapping of rodent space use, social networks, and habitat context.
- Rich microbiome data aligned with individual identity, capture history, and spatial coordinates, with explicit caveats and decontamination guidance.
- Phenotypic metadata for bacterial genera to inform functional interpretation of microbiome results.
- Data are provided as CSV files for captures and logger records, with a raw phyloseq object for microbiome data and associated lab/process notes.

## Practical notes for GIS-focused users
- Prepare spatial layers:
  - Grid cells (10x10 m) with habitat attributes.
  - Logger point features with timestamps and species IDs.
  - Burrow locations and burrow-logger assignments.
  - Trap locations with capture events and individual IDs.
- Integrate with microbiome data:
  - Link sample IDs to individual IDs and spatial coordinates.
  - Use capture history and logger data to derive social networks or space-use metrics for overlay with microbiome profiles.
- Data cleaning:
  - Consider decontaminating microbiome data before analysis; subset data by sample type when applying decontam in practice.
  - Account for potential sampling bias due to burrow logger coverage and varying sampling windows.