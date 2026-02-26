# Metadata, site descriptions and methods for 'Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019'

## Overview
- Describes metadata, site description, and methods for a girdling experiment assessing soil fungal communities in a subarctic forest–tundra ecotone near Abisko, Sweden.
- Includes experimental design, sampling timeline (2017–2019), laboratory workflows (DNA extraction, PCR, sequencing), bioinformatic processing, and quantitative approaches for estimating fungal abundance.
- Data and metadata underpin analyses of how girdling (disrupting phloem transport) affects soil fungal communities under birch and willow vegetation.

## Data and metadata
- Key datasets:
  - Abisko_Relative_Abundance.csv: relative abundances of fungal species hypotheses (SHs) per sample; copy-number-informed estimates after normalization.
  - Abisko_Fungi_Taxonomy.csv: taxonomic assignments for SHs (phylum to species) and a linking SCATA_ID to SHs.
- Metadata fields describe each plot and treatment:
  - Plot (Pair ID for adjacent plots), Vegetation (birch or willow), Treatment (girdled ‘g’ or control ‘c’), Year, ITS_copy_numbers, scata4589_XXXX (SH IDs), and Representative_sequence per SH.
- Functional categorization:
  - SHs assigned to functional guilds (e.g., ectomycorrhizal, moulds, litter saprotrophs, root-associated ascomycetes) via FungalTraits.
  - Ectomycorrhizal SHs further classified into tenable exploration-types (ET) based on established datasets.

## Experimental design: girdling and plots
- Location: 4–5 km south of the Abisko Scientific Research Station, Sweden (68°18 N, 18°49 E; ~600 m.a.s.l.).
- Design: girdling experiment across plots
  - Birch plots: 6 pairs (Betula pubescens) with dense ericoid understorey.
  - Willow plots: 5 pairs (Salix lapponum).
- Girdling: conducted June 2017; bark and phloem removed around circumference to disrupt photosynthate transport from canopy to roots.
- Plot sizes:
  - Birch: circular area with radius 10 m.
  - Willow: circular area with radius 2 m (with trenched perimeter to prevent root ingrowth).
- Post-treatment management: resprouting shoots from below girdle-line removed; leaf phenology differed between girdled and control plots (birch mostly leafed in 2018; girdled birch leaves largely failed by 2019; girdled willow leaves in 2018–2019).

## Sampling and laboratory methods
- Soil sampling:
  - Timepoints: 3 August 2017, 1 August 2018, 5 August 2019.
  - Plots: 22 total (6 birch pairs, 5 willow pairs; plus additional arrangements within plot areas).
  - Birch plots: 9 cores collected in a 3×3 grid within a central area.
  - Willow plots: 9 cores distributed across the plot within the trenched perimeter.
  - Processing: litter layer removed; mineral horizons removed below organic horizon; cores homogenised and pooled within 6 hours; coarse roots >2 mm removed; samples frozen at -20°C until analysis.
  - Replicates: some 2019 birch samples lost; 59 samples proceeded to analysis.
- DNA extraction and amplification:
  - DNA extraction: 50 mg sub-samples using NucleoSpin Soil Kit.
  - Target region: ITS2 (fungal) amplified with gITS7 forward primer and a reverse primer mix of ITS4 and ITS4arc to capture general eukaryotes plus Archaeorhizomycetes.
  - PCR details: duplicates per sample; ~23 cycles (range 21–25); 50 µL reactions with standard components; 0.5 µM gITS7, 0.3 µM ITS4, 0.1 µM ITS4arc.
  - Purification and pooling: AMPure beads; quantification with Qubit; equal DNA amounts pooled; cycle-purified further.
  - Sequencing: PacBio SMRT Sequel after adaptor ligation; performed by SciLifeLab NGI (Uppsala, Sweden).
- Controls and bias considerations:
  - Cycle numbers kept minimal to reduce biases; duplicate PCRs per sample; PCR inhibition tested with plasmid controls showed no significant inhibition.

##Bioinformatic processing and taxonomic identification
- Sequencing output: 181,560 reads; 100,282 passes QC.
- SH (species hypothesis) clustering:
  - Quality filtering: mean quality score ≥ 20; primer/adaptor tags removed.
  - Clustering: USEARCH-based, single-linkage at 98.5% similarity to define SHs.
  - Non-fungal reads removed (plants).
  - Retained SHs contributing >1% of fungal sequences in at least one sample.
  - Final matrix: 59 samples × 521 SHs comprising 38,659 reads.
- Taxonomy and references:
  - Three reference datasets used to aid taxonomic classifications: Swedish Soil Inventory, Swedish Boreal forest, and Abisko database; cross-validated against UNITE at 98% similarity for species-level calls.
  - Functional guilds assigned via FungalTraits; root-associated ascomycetes included as an “unspecified” group due to broad ecology.
  - Ectomycorrhizal SHs annotated with ET (exploration types) where possible.
- Output integration:
  - SH abundances integrated with functional guilds and ET types for downstream analyses (e.g., carbon dynamics, rhizosphere interactions).

## ITS region quantitative PCR (qPCR)
- Quantification strategy:
  - ITS2 copy numbers estimated by qPCR using IQ SYBR Green on an iQ5 system.
  - Reactions: ~5 ng DNA, 0.1% BSA; primers ITS4/ITS4arc and gITS7 as above.
  - Cycling: 40 cycles with standard profile including 78 °C melt step; inhibition checks with plasmid standards indicated no significant inhibition.
  - Standard curves: generated from serial dilutions of linearized plasmids containing ITS2.
  - Abundance estimation: SH and guild relative copy numbers scaled by total fungal ITS copy numbers to produce per-sample estimates.
- Rationale: semi-quantitative approach that complements relative abundances from sequencing.

## Data governance, sharing, and reporting
- Output types: metadata, raw sequencing-derived SH abundances, taxonomic assignments, functional guild categorizations, and qPCR-derived copy numbers.
- Data sharing considerations:
  - Public sharing of underlying datasets can be a barrier; the document notes data governance and openness as central to monitoring frameworks for ensuring data are shareable, well-documented, and managed to standards.
- Dissemination:
  - Core results and datasets underpin analyses reported in Parker et al. (2020) and related references.

## Key challenges and monitoring considerations
- Data availability and access: ensuring timely access to data across organisations.
- Metadata adequacy: ensuring complete, clear, and machine-readable metadata for reuse.
- Silos and governance: overcoming organizational silos and establishing data governance for sharing and reuse.
- Data transformation: formats often require transformation to be readily usable; ensuring standardization and interoperability.
- Communicating findings: translating complex fungal community results into clear, policy-relevant insights.
- Openness and standards: setting and maintaining data standards at the source to support long-term monitoring and decision-making.

## References
- Parker et al. (2020) and supporting methodological references for primer design, OTU/SH clustering, and taxonomic frameworks.