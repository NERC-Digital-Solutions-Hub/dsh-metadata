# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Overview
- This document provides metadata and methodological details for two data files: Abisko_Relative_Abundance.csv and Abisko_Fungi_Taxonomy.csv.
- It describes the study design, sampling, laboratory workflows, bioinformatic processing, and quantitative PCR (qPCR) approaches used to characterize fungal communities in soil from girdled and non-girdled plots in subarctic Sweden.
- It links relative abundance data (species hypotheses) to taxonomic classifications and functional guilds, with guidance on data provenance, processing steps, and potential limitations.

## Metadata files
- Abisko_Relative_Abundance.csv
  - Columns include: Plot (Pair ID for adjacent plots), Vegetation (birch or willow), Treatment (girdled 'g' or control 'c'), Year, ITS_copy_numbers, scata4589_XXXX (relative abundance of distinct species hypotheses), and SCATA_IDs linking to Abisko_Fungi_Taxonomy.csv.
- Abisko_Fungi_Taxonomy.csv
  - Columns include: Phylum, Subphylum, Class, Order, Family, Genus, Species, SCATA_ID, and Representative_sequence (most common genotype for each SH).

## Experimental design and site
- Girdling experiment in a permafrost-free forest-tundra ecotone near the Abisko Scientific Research Station, Sweden.
- Six pairs of birch plots and five pairs of willow plots across a 0.88 km2 area.
- Girdling performed in June 2017 by removing bark and phloem, disrupting photosynthate transport to roots.
- Plot sizes: birch plots radius 10 m; willow plots radius 2 m (trenched perimeter to prevent root ingrowth).
- Post-girdling dynamics: leaf production in girdled birch mostly failed by 2019; girdled willow shrubs failed in 2018-2019. Leaves remained until senescence in 2017 for birch prior to girdling.

## Sampling and laboratory methods
- Soil horizon: organic O horizon sampled on 3 Aug 2017; 1 Aug 2018; 5 Aug 2019.
- Sampling per plot: nine 3.8 cm cores collected (birch grids 3x3 m; willow plots evenly across trenched area).
- Processing: litter and mineral horizons removed; cores homogenized and pooled within 6 hours; coarse roots >2 mm removed; samples frozen at -20°C.
- DNA extraction: 50 mg sub-sample using NucleoSpin Soil Kit.
- ITS2 amplification: fungal gITS7 forward primer with ITS4/ITS4arc mix; PCR duplicates per sample; minimized cycles (23 cycles for most, some 21 or 25).
- PCR setup: final 50 µL reactions with ~25 ng DNA, standard reagents, and specific primer concentrations.
- Post-PCR: duplicate products pooled, purified with AMPure beads, quantified (Qubit), DNA amounts equalized, and pooled for sequencing.
- Sequencing: PacBio SMRT Sequel platform after adaptor ligation (SciLifeLab NGI, Uppsala).

## Bioinformatic processing and fungal taxonomic identification
- Approach: metabarcoding of pooled DNA to identify species hypotheses (SHs) using SCATA pipeline.
- Quality control: reads filtered (mean quality ≥20), primers/tags removed; sequences compared with USEARCH; SHs clustered at 98.5% similarity; plant sequences removed.
- Data: 181,560 reads generated; 100,282 passed QC; final matrix used 59 samples with 52,? actually 521 SHs across 59 samples (final analysis).
- Reference context: three reference datasets used to aid taxonomic classification (Swedish Soil Inventory, Swedish Boreal Forest, Abisko database) and verified against UNITE at 98% similarity for species-level IDs.
- Functional guilds: assigned SHs to guilds (ectomycorrhizal fungi, moulds, litter saprotrophs, root-associated ascomycetes) using FungalTraits; root-associated ascomycetes include ericoid mycorrhizal fungi and root endophytes (kept as an undefined group when ecology was unclear).
- Ectomycorrhizal SHs: assigned to one of five exploitation types (ET) per established datasets.

## ITS region quantitative PCR
- ITS2 copy numbers estimated by qPCR using IQ SYBR Green on an iQ5 system.
- Reactions: ~5 ng DNA template per 20 µL, ITS4/ITS4arc and gITS7 primers, with BSA and specific cycling parameters.
- Quality checks: inhibition tests using plasmid standards indicated no significant inhibition.
- Quantification: standard curves from serial dilutions of linearized plasmids containing ITS2; corrected for nonfungal amplification; SH and guild copy numbers derived by multiplying relative abundances by total fungal ITS copy numbers.

## Data quality, limitations, and caveats
- Some birch forest samples from 2019 were lost, reducing replicates; 59 samples proceeded to analysis from an initial 66 plots.
- Potential biases: PCR cycle number variation, primer biases, and pooling steps; long-term storage and handling considerations.
- Dataset scope: provides a semi-quantitative view of fungal communities across girdled vs. control plots and birch vs. willow hosts, with careful linkage between SH abundance and taxonomy.

## Data governance, sharing, and provenance
- Data are described with explicit provenance: sampling dates, plot descriptions, DNA extraction and sequencing methods, and processing steps.
- Metadata emphasizes reproducibility, with explicit links between SHs (scata4589_ IDs), their taxonomy in Abisko_Fungi_Taxonomy.csv, and their relative abundances in Abisko_Relative_Abundance.csv.
- The document notes the importance of sharing limitations and updates, and records the processes used to generate and process data for publication and repository deposition.

## Key terms and data relationships
- Species hypothesis (SH): a clusterized fungal sequence representing a putative species-level taxon.
- SCATA_ID: unique identifier linking SHs to their taxonomic assignments.
- Relative abundance data: SH-level abundances per sample, linked to taxonomy and functional guild.
- Functional guilds: ecological roles assigned to SHs (e.g., ECM, moulds, litter saprotrophs, root-associated ascomycetes).
- Ectomycorrhizal exploration types (ET): categorized for ECM SHs according to established typologies.

## References
- Parker et al. (2020) on canopy-to-soil carbon dynamics.
- Key methodological and taxonomic references for primers, clustering, and fungal trait databases (e.g., UNITE, FungalTraits, ITS primer sets, SCATA, UPARSE).