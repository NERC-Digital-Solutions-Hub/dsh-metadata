# Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019

## Overview
- Metadata and methods for studying soil fungal communities in girdled vs. non-girdled plots under birch and willow vegetation in subarctic Sweden (2017–2019), with data products suitable for GIS-based analysis.
- Primary data products: Abisko_Relative_Abundance.csv (relative abundances of fungal species hypotheses and ITS copy numbers) and Abisko_Fungi_Taxonomy.csv (taxonomy mapping and representative sequences).

## Study design and site context
- Girdling experiment in a boreal-subarctic forest-tundra ecotone near Abisko, Sweden.
- Plots: six pairs of mountain birch forest plots and five pairs of willow shrub plots, spanning 0.88 km2.
- Treatments: girdled (g) vs. control (c); girdling performed June 2017 by removing bark and phloem around canopy stems.
- Plot geometry: birch plots radius 10 m; willow plots radius 2 m with trenched perimeters to prevent root ingrowth.
- Vegetation outcomes: leaf production largely failed in girdled birch/ willow canopies by 2018–2019.

## Sampling design and field procedures
- Soil horizon: organic O horizon sampled on three dates — Aug 3, 2017; Aug 1, 2018; Aug 5, 2019.
- Within-plot sampling: nine 3.8 cm cores per plot; birch plots sampled on a 3x3 m central grid, willow plots distributed evenly within the trenched area.
- Sample processing: litter layer removed, cores homogenised within 6 hours, coarse roots (>2 mm) removed, samples frozen at -20°C, later pulverised.
- Replicates: 59 samples advanced to analysis (some birch forest samples from 2019 lost).

## DNA extraction, amplification, and sequencing
- DNA extraction: 50 mg soil sub-sample using NucleoSpin Soil Kit.
- Target region: fungal ITS2 amplified with gITS7 and ITS4/ITS4arc primers, with selective cycling to minimize biases.
- PCR: duplicates per sample, 50 µl reactions, specific cycling conditions (5 min initial denaturation; variable cycles; final extension).
- Post-PCR processing: duplicate products pooled, purified with AMPure beads, quantified, equal DNA amounts pooled, cleaned with CyclePure kit.
- Sequencing: PacBio SMRT Sequel platform after adaptor ligation.

## Bioinformatics and taxonomic assignment
- Sequence processing: SCATA pipeline; quality filtering (mean QC ≥ 20), primer/tag removal, 90% similarity threshold for tag screening, pairwise comparison with USEARCH, single-linkage clustering at 98.5% similarity to define species hypotheses (SHs).
- Data filtering: plant sequences removed; SHs retained if contributing >1% of fungal sequences in at least one sample.
- Taxonomy: SHs clustered using reference datasets (Swedish Soil Inventory, Swedish Boreal forest, Abisko database) and verified against UNITE at 98% similarity for species-level IDs.
- Functional guilds: SHs assigned to guilds (ectomycorrhizal, moulds, litter saprotrophs, root-associated ascomycetes) via FungalTraits; ectomycorrhizal SHs further classified into exploration types (ET) per established datasets.
- Data structure: final matrix includes 521 SHs across 59 samples; plant sequences removed; fungal copy numbers scaled to total fungal ITS copies corrected for nonfungal contribution.

## ITS copy number quantification
- Quantitative PCR (qPCR) used to estimate ITS2 copy numbers.
- Reactions: 20 µl including template DNA, ITS primers (as above), and controls; standard curves created from plasmid templates.
- Output: relative abundance of SHs and functional guilds derived by multiplying SH and guild proportions by total fungal ITS copy numbers (adjusted for nonfungal sequence presence).

## Data products and field-ready attributes
- Abisko_Relative_Abundance.csv: 
  - Plot/Pair identifiers, Vegetation (birch or willow), Treatment (g or c), Year, ITS copy numbers, SH-specific relative abundances (SH IDs prefixed with scata4589_), and associated metadata.
- Abisko_Fungi_Taxonomy.csv:
  - Taxonomic levels: Phylum, Subphylum, Class, Order, Family, Genus, Species; SCATA_ID linking to SHs in abundance matrix; Representative_sequence for each SH.

## Spatial and GIS considerations
- Spatial context: plots distributed across 0.88 km2 area with defined central sampling areas (birch) and trenched willow plots; coordinates provided for site location (approx. 68°18′N, 18°49′E, ~600 m a.s.l.).
- GIS-ready elements: plot-level attributes (vegetation type, girdling status, year), SH-level microbial data, and functional classifications enable map-based visualization of fungal community structure by vegetation, treatment, and time.
- Potential analyses: spatial distribution of SHs and guilds, compare girdled vs. control effects, vegetation-driven community shifts, integration with soil CO2 flux or root/microbial activity data (as in Parker et al. 2020).

## Data quality, limitations, and considerations
- Some 2019 birch samples lost; incomplete replication for that year.
- Semi-quantitative nature of metabarcoding and PCR biases; attempts to minimize biases via low-cycle counts and duplicate reactions.
- Large complexity: 521 SHs across 59 samples; data integration requires careful normalization and consideration of detection limits.
- Cross-dataset taxonomic harmonization relies on UNITE and FungalTraits databases; potential for unresolved or broad ecologies in some SHs (notably certain ericoid/root-associated taxa).

## References and related work
- Parker et al. (2020): rhizosphere allocation and soil CO2 efflux context for study area.
- Foundational references for primers, clustering, and functional ecology of ectomycorrhizal fungi and FungalTraits (Agerer 2001; Lindahl et al.; Tedersoo & Smith 2013; Põlme et al. 2020).