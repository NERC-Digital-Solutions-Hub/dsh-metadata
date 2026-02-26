# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Overview
- Describes metadata, site descriptions, and laboratory methods for analyzing fungal communities in a girdling experiment conducted in subarctic Sweden.
- Focuses on two data files: Abisko_Relative_Abundance.csv (relative abundance of fungal species hypotheses) and Abisko_Fungi_Taxonomy.csv (taxonomy and representative sequence for SHs).
- Data derive from a long-term, controlled field experiment (girdled vs. control) across birch forest and willow shrub habitats, with multi-year sampling and DNA-based community profiling.

## Experimental design and site description
- Location: subarctic forest-tundra ecotone near Abisko Scientific Research Station, Sweden.
- Experimental setup: girdling applied to canopy stems to disrupt photosynthate transport; plots include birch (Betula pubescens) and willow (Salix lapponum) with paired girdled and non-girdled treatments.
- Plot layout:
  - Birch plots: circular area radius 10 m.
  - Willow plots: circular area radius 2 m with trenched perimeter to prevent root ingrowth.
- Replication: six pairs of birch plots and five pairs of willow plots (total 22 plots).
- Timeline: girdling performed in June 2017; leaf production dynamics observed through 2019.
- Pre-treatment characteristics: average soil and canopy properties similar between treatments before girdling.

## Data generated and primary variables
- Abisko_Relative_Abundance.csv
  - Plot-level metadata: Plot, Description (Pair ID for adjacent plots), Vegetation (birch or willow), Treatment (girdled or control), Year.
  - Fungal data: ITS_copy_numbers (fungal ITS copy numbers per mg organic matter), scata4589_XXXX (relative abundance of distinct fungal species hypotheses, SHs, identified by SCATA with SH IDs).
- Abisko_Fungi_Taxonomy.csv
  - Taxonomic levels: Phylum, Subphylum, Class, Order, Family, Genus, Species, plus SCATA_ID linking to relative abundance data.
  - Representative_sequence: most common genotype for each SH.

## Sample collection and laboratory workflow
- Soil sampling
  - Time points: August 2017, August 2018, August 2019.
  - Plots: 22 total; nine 3.8 cm cores per plot, collected from central areas (birch) or across trenched Willow plots.
  - Sample processing: litter and mineral horizons removed, cores homogenized and pooled within 6 hours, coarse roots removed, samples frozen at -20°C.
  - Note: some birch samples from 2019 were lost, reducing replicates; 59 samples advanced to analysis (out of 66 plots).
- DNA extraction and amplification
  - DNA from ~50 mg sub-sample using NucleoSpin Soil Kit.
  - ITS2 region amplified with fungal gITS7 forward primer and a mix of ITS4 and ITS4arc reverse primers to cover fungi and Archaeorhizomycetes, with minimized cycle numbers to reduce biases.
  - Reactions run in duplicates; products pooled and purified; DNA quantified; equal amounts mixed for sequencing.
  - Sequencing by Pacific Biosciences SMRT Sequel technology after adaptor ligation.
- PCR and sequencing details
  - Primer concentrations: gITS7 (0.5 µM), ITS4 (0.3 µM), ITS4arc (0.1 µM).
  - Cycling: initial denaturation, 21–30 cycles (adjusted by sample), followed by final extension.
  - Quality control: duplicate PCRs pooled; cleanup with AMPure beads; concentration measured; library cleanup with CyclePure kit.
- qPCR (ITS region)
  - Quantification of ITS copy numbers using qPCR with ITS4/ITS4arc and gITS7 primers.
  - Reaction mix includes BSA, and standard curves generated from plasmids containing ITS2.
  - Inhibition checks performed; data used to scale SH abundances to copy numbers.

## Bioinformatics and data processing
- Sequence processing
  - Platform: Pacific Biosciences SMRT sequencing data; initial reads quality-filtered.
  - Clustering: sequences grouped into species hypotheses (SHs) using SCATA with 98.5% similarity threshold.
  - Filtering: plant sequences removed; only SHs with >1% contribution in at least one sample retained.
  - Final dataset: 52?SHs across 59 samples (final matrix described as 521 SHs in 59 samples after broader filtering and clustering steps; exact counts per file excerpt: 38,659 reads used in final analysis across 521 SHs in 59 samples).
- Taxonomic and functional classification
  - Taxonomy assigned by cross-referencing with reference datasets (Swedish Soil Inventory, Swedish Boreal forest, Abisko database) and UNITE at 98% similarity for species-level identifications.
  - Functional guilds assigned via FungalTraits: ectomycorrhizal fungi (ECM), moulds, litter saprotrophs, and root-associated ascomycetes (the latter treated as a broad category due to ecological diversity).
  - Ectomycorrhizal SHs further categorized into exploration types (ET) based on established datasets.
- Data integration and normalization
  - SH relative abundances multiplied by total fungal ITS copy numbers (after accounting for nonfungal sequence contributions) to obtain copy-number estimates per SH and per functional guild in each sample.
  - Outputs link SHs to taxonomy (Abisko_Fungi_Taxonomy.csv) and to abundance data (Abisko_Relative_Abundance.csv).

## Data quality, limitations, and considerations
- Sample completeness: some birch 2019 samples lost, reducing replication and affecting temporal comparability.
- PCR and sequencing biases: cycle number variation and primer efficiency can influence SH detection and relative abundances; steps taken to minimize biases (limited cycles, duplicates, pooling, and careful cleanup).
- Taxonomic resolution: reliance on 98% similarity with reference databases; some SHs may be unresolved at finer taxonomic levels; functional guild assignments depend on database accuracy (FungalTraits) and may carry uncertainty for poorly characterized taxa.
- Data interpretation: semi-quantitative estimates derived by scaling SH abundances with ITS copy numbers; assumes proportionality between ITS copies and organism abundance, which can be affected by ribosomal copy-number variation among taxa.

## How this data can be used
- Investigate how girdling and vegetation type (birch vs. willow) influence soil fungal community composition and abundance over three years.
- Compare SH-level responses and functional guild dynamics (e.g., ECM vs. saprotrophs) to girdling treatment.
- Explore the relationship between root/soil processes and fungal community structure in subarctic forest-tundra ecotones.
- Support meta-analyses or comparative studies using Abisko_Relative_Abundance.csv and Abisko_Fungi_Taxonomy.csv alongside the associated metadata.

## Notes on data provenance and references
- Data generation and processing steps are documented in the provided methods, with citations to Parker et al. (2020), Castaño et al. (2020), Ihrmark et al. (2012), Lindahl et al. (various), and related methodological sources.
- Taxonomic and functional annotations rely on UNITE, FungalTraits, and established ectomycorrhizal exploration type frameworks (Agerer, Tedersoo & Smith).