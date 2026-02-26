# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Objective and scope
- Document a girdling experiment to understand how disruption of carbon transport from canopy to roots affects soil fungal communities in subarctic forest-tundra transitions.
- Compare birch (Betula pubescens) and willow (Salix lapponum) vegetation under girdled versus control conditions.
- Provide standardized metadata, DNA-based community data (fungal), and qPCR-based abundance estimates to support environmental monitoring and long-term Trend analyses.

## Study design and site
- Location: subarctic landscape 4–5 km south of the Abisko Scientific Research Station, Sweden.
- Design: six pairs of birch plots and five pairs of willow plots across a 0.88 km² area.
- Treatments: girdled (g) vs. control (c) within each pair; girdling performed in June 2017.
- Plot geometry: birch plots are circular with a 10 m radius; willow plots have a 2 m radius with a trenched perimeter to prevent root ingrowth.
- Pre-treatment characteristics: average soil and canopy characteristics were similar between treatments.
- Girdling effect: disrupts photosynthate transport from canopy to roots; re-sprouting was controlled; leaf production showed girdling-induced suppression in subsequent years.

## Field sampling and processing
- Soil horizon: organic O horizon sampled on 3 Aug 2017, 1 Aug 2018, and 5 Aug 2019.
- Sampling per plot: nine 3.8 cm diameter cores collected and homogenised; birch cores grid-based in a central 3 x 3 m area; willow cores distributed within trenched perimeter.
- Sample handling: litter and mineral horizons removed; cores pooled within 6 hours, coarse roots removed, samples frozen at -20°C.
- Replicates: some year-specific losses (birch 2019) reduced replicates; 59 samples advanced to analysis.
- Laboratory processing: homogenised pooled soil samples were finely ground under frozen conditions prior to DNA extraction.

## DNA extraction, amplification, and sequencing
- Target: fungal communities via ITS2 region.
- Extraction: 50 mg sub-sample using NucleoSpin Soil Kit.
- Amplification: gITS7 forward primer with mixed ITS4/ITS4arc reverse primers, designed to capture general fungi and Archaeorhizomycetes; low-cycle PCR to reduce bias (53–55 cycles total across samples with cycle-variance).
- PCR setup: duplicates per sample; 50 µL reactions with standard reagents; specific cycling protocol with adjusted cycle numbers per sample.
- Library prep: duplicates pooled, purified with AMPure beads, quantified (Qubit), equal DNA amounts combined; cleaned with CyclePure kit.
- Sequencing: Pacific Biosciences SMRT Sequel technology (long-read metabarcoding) conducted by SciLifeLab NGI (Uppsala, Sweden).

## Bioinformatics and taxonomic identification
- Approach: metabarcoding to identify distinct fungal groups at the species-hypothesis (SH) level.
- Quality control: reads quality-filtered (mean quality ≥ 20), primer sequences and tags removed (90% similarity threshold for primer matching).
- Clustering: USEARCH-based pairwise comparison; SHs formed with a 98.5% similarity cutoff using single-linkage.
- Filtering: plant sequences removed; only SHs contributing >1% of fungal sequences in any sample retained.
- Dataset: 181,560 raw reads; 100,282 passed QC; final matrix: 59 samples × 52 SHs? (final text notes 521 SHs across 59 samples; 38,659 reads used in final analysis).
- Taxonomy: three reference datasets used to aid classification (Swedish Soil Inventory, Swedish Boreal Forest, Abisko database) and UNITE for species-level verification at 98% similarity.
- Functional assignment: SHs categorized into functional guilds (ectomycorrhizal fungi, moulds, litter saprotrophs, root-associated ascomycetes) via FungalTraits database.
- Ecological grouping: ectomycorrhizal SHs further assigned to one of five exploration types (ET) per established datasets.

## ITS region quantitative PCR (qPCR)
- Purpose: estimate copy numbers of the fungal ITS2 region to obtain semi-quantitative abundance estimates.
- Assay: IQ SYBR Green on iQ5 instrument; 20 µL reactions with ITS primers (ITS4/ITS4arc and gITS7) as above.
- Standards and controls: serial dilutions of linearized plasmids with ITS2; inhibition tests using known plasmid copies showed no significant inhibition.
- Data processing: multiply SH- and guild-level relative abundances by total fungal ITS copy numbers (adjusted for non-fungal amplification) to estimate absolute copy numbers per sample and per SH/guild.

## Metadata and data products
- Metadata files:
  - Abisko_Relative_Abundance.csv: per-plot metadata including pair ID, vegetation type (birch or willow), treatment (girdled or control), sampling year, ITS copy numbers, SH abundances (scata4589_XXXX), and taxonomy linkage to Abisko_Fungi_Taxonomy.csv.
  - Abisko_Fungi_Taxonomy.csv: taxonomy down to species with SCATA_ID, and representative sequence for each SH.
- Data structure: SHs linked to taxonomy and functional guilds; samples linked to plot descriptors and year; relative abundances integrated with ITS copy numbers to yield more quantitative outputs.

## Relevance to environmental monitoring and data stewardship
- Demonstrates a standardised, traceable workflow from field sampling to molecular analysis and data curation suitable for time-series environmental health assessment.
- Produces layered data products (metadata, taxonomic identifications, functional guilds, ET types, and qPCR-based abundance estimates) for cross-site comparisons and policy-relevant monitoring.
- Emphasizes data quality assurance, reproducible pipelines, and the storage/upload of created datasets to appropriate portals to enable broad access.

## Key challenges and opportunities for data value
- Challenge: increasing the utility of datasets by integrating with additional relevant environmental data to avoid single-use outputs.
- Opportunity: enabling broader access to underlying data to facilitate secondary analyses, cross-study integration, and enhanced policy and management insights.