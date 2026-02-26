# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Overview
- Metadata, sampling design, and molecular workflow to study soil fungal communities in girdled vs. non-girdled plots in subarctic Sweden.
- Data include relative abundances of fungal species hypotheses (SHs), taxonomic classifications, functional guilds, and ITS copy numbers.

## Study area and experimental design
- Location: 4–5 km south of the Abisko Scientific Research Station, Sweden, in a permafrost-free forest–tundra ecotone.
- Plant groups: mountain birch (Betula pubescens) and willow thickets (Salix lapponum).
- Experimental setup: girdling initiated in June 2017 with six pairs of birch plots and five pairs of willow plots; girdled (g) vs. control (c) plots.
- Girdling effect: disrupted photosynthate transport; leaf production differences observed in 2018–2019 (birch mostly failed in girdled canopies by 2019; willow girdling affected leaves in 2018–2019).
- Plot geometry: birch plots circular radius 10 m; willow plots radius 2 m with trenched perimeters to prevent root ingrowth.
- Replication: total of 22 plots (6 birch pairs, 5 willow pairs).

## Soil sampling
- Horizon and cores: organic soil horizon (O) sampled on 3 Aug 2017, 1 Aug 2018, 5 Aug 2019.
- Sampling design: nine 3.8 cm diameter cores per plot; birch plots sampled on a 3×3 m central grid; willow plots distributed across the trenched plot area.
- Sample processing: litter layer and underlying mineral horizons removed; cores homogenised and pooled within 6 hours; coarse roots (>2 mm) removed; samples stored at -20°C.
- Replicate details: 59 samples progressed to analysis; some birch samples from 2019 were lost.

## DNA amplification and sequencing
- DNA extraction: from ~50 mg soil sub-sample using NucleoSpin Soil Kit.
- Target: fungal ITS2 region amplified with gITS7 forward primer and a mixed ITS4/ITS4arc reverse primer set to capture general fungi and Archaeorhizomycetes.
- PCR: duplicates per sample; ~23 cycles (range 21–25 cycles); low-cycle bias strategy.
- Library prep: pooling of duplicate PCR products, purification, and normalization using Qubit; sequencing on Pacific Biosciences SMRT Sequel.
- PCR controls: inhibition tests conducted with plasmid standards to ensure no significant inhibition.

## Bioinformatics and taxonomic assignment
- Sequence processing: SCATA pipeline for quality filtering (mean quality score ≥20), primer/tag removal, and clustering into SHs at 98.5% similarity.
- Post-processing: plant sequences removed; 181,560 raw reads, 100,282 passed QC; final matrix comprised 38,659 reads across 521 SHs in 59 samples.
- Taxonomy: SHs clustered with reference datasets (Swedish Soil Inventory, Swedish Boreal forest, Abisko database) and validated against UNITE at 98% similarity for species-level IDs.
- Functional guilds: SHs assigned to ECM fungi, moulds, litter saprotrophs, and root-associated ascomycetes (root-associated group includes ericoid mycorrhizal fungi and root endophytes; treated as an unspecified group where ecology is uncertain).
- Ectomycorrhizal SHs: assigned to exploration types (ET) per Agerer et al.

## Quantification and data processing
- ITS copy numbers: estimated by qPCR using ITS2 primers and SYBR Green chemistry; reactions included standard curves from linearized plasmids.
- Abundance scaling: SH and guild relative abundances were scaled by total fungal ITS copy numbers (adjusted for nonfungal sequence contributions) to estimate absolute copy numbers per sample.
- Data normalization: approach preserves semi-quantitative interpretation of fungal communities across samples.

## Metadata and data structure
- Data files described:
  - Abisko_Relative_Abundance.csv: relative abundances of SHs per sample, linked by SCATA_ID.
  - Abisko_Fungi_Taxonomy.csv: taxonomic classification for SHs (Phylum–Species) and Representative_sequence.
- Key identifiers: SHs tied to SCATA_ID; taxonomic fields include Phylum, Subphylum, Class, Order, Family, Genus, Species, with Representative_sequence representing the dominant genotype.

## Notes on limitations and context
- Some birch samples from 2019 were lost, reducing replication for that year and leaving 59 usable samples from 66 plots.
- The methodology emphasizes a semi-quantitative view of fungal communities via ITS2 copy numbers and SH-level abundances, with careful attention to PCR bias minimization and cross-dataset taxonomic validation.