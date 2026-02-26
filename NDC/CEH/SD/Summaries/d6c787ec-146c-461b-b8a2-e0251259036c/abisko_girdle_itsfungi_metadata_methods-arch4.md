# Metadata, site descriptions and methods for 'Soil fauna abundance under birch and willow vegetation in girdled and non-girdled plots, subarctic Sweden, 2019' Metadata for 'Abisko_Relative_Abundance.csv'

- Overview
  - A girdling experiment in subarctic Sweden (birch forest and willow thickets) examining fungal communities in soil organic horizon (O horizon) across girdled versus control plots.
  - Sampling years: 2017, 2018, 2019; total plots analyzed: 22 (birch) plus 22 (willow) originally, with 59 samples advancing to analysis due to some losses.
  - Objective includes characterizing relative abundance of fungal species hypotheses (SHs) and linking to taxonomy and functional guilds.

- Data files and metadata
  - Abisko_Relative_Abundance.csv
    - Plot: Pair ID for adjacent plots.
    - Vegetation: Dominant vegetation type (birch or willow).
    - Treatment: girdled (g) or control (c).
    - Year: sampling year.
    - ITS_copy_numbers: ITS2 copy numbers per mg organic matter.
    - scata4589_XXXX: Relative abundance of distinct SHs (SH IDs prefixed by scata4589_).
    - Taxonomy linkage to Abisko_Fungi_Taxonomy.csv via SCATA_ID.
  - Abisko_Fungi_Taxonomy.csv
    - Taxonomic ranks: Phylum, Subphylum, Class, Order, Family, Genus, Species.
    - SCATA_ID: SH identifier corresponding to relative abundance data.
    - Representative_sequence: Most common genotype for each SH.

- Experimental design
  - Field setup: girdling of bark and phloem around base of stems to disrupt photosynthate transport.
  - Sample locations: six pairs of birch plots and five pairs of willow plots within a 0.88 km2 area, across a forest-tundra ecotone ~600 m elevation.
  - Plot geometry: birch plots radius 10 m; willow plots radius 2 m with trenched perimeters to exclude root ingrowth.
  - Girdling occurred in June 2017; leaf production outcomes varied by year and vegetation type.

- Sampling and laboratory methods
  - Soil sampling: organic horizon (O horizon) collected on 3 Aug 2017, 1 Aug 2018, and 5 Aug 2019.
  - Within-plot sampling: nine cores per plot (3x3 grid for birch; evenly distributed within trenched perimeter for willow).
  - Processing: cores homogenized; coarse roots (>2 mm) removed; samples frozen at -20°C; pooled within 6 hours.
  - DNA extraction: 50 mg sub-sample using NucleoSpin Soil Kit.
  - ITS2 amplification: fungal gITS7 forward primer with ITS4/ITS4arc reverse primer mix; minimal PCR cycles to reduce bias (51 samples with 23 cycles, 5 with 21 cycles, 3 with 25 cycles); duplicates per sample.
  - Sequencing: pooled PCR products purified and sequenced using Pacific Biosciences SMRT Sequel platform after adaptor ligation.
  - qPCR: ITS2 copy numbers estimated with ITS4/ITS4arc and gITS7 primers; standard curves from plasmid controls; correction for nonfungal amplification.

- Bioinformatics and taxonomic identification
  - Sequence processing: quality filtering, primer/adaptor removal, clustering into SHs with SCATA at ~98.5% similarity; plant sequences removed.
  - Reads: 181,560 total; 100,282 passed quality control.
  - SHs retained: those with >1% representation in at least one sample; final matrix: 521 SHs across 59 samples (59 samples used due to losses in some years/plots).
  - Reference datasets for taxonomy: Swedish Soil Inventory, Swedish Boreal Forest, Abisko database; classifications verified against UNITE at 98% similarity for species-level designations.
  - Functional guilds: SHs assigned to ECM fungi, moulds, litter saprotrophs, and root-associated ascomycetes using FungalTraits.
  - Ectomycorrhizal SHs: assigned to one of five Exploration Types (ET) per established datasets.

- Abundance quantification and data integration
  - Relative abundance of each SH and guild multiplied by total fungal ITS copy numbers per sample to estimate copy numbers for SHs and guilds.
  - Correction applied to account for nonfungal marker amplification based on sequencing results.
  - Final outputs link SH abundances in Abisko_Relative_Abundance.csv to taxonomy in Abisko_Fungi_Taxonomy.csv via SCATA_ID.

- Data quality, limitations, and notes
  - Sample loss: birch samples from 2019 partially lost, resulting in reduced replication for that year.
  - Paired design robustly maintained across years, but some plots/samples excluded from final matrix (59 of 66 possible).
  - PCR cycling varied by sample to minimize bias; duplicate PCRs pooled prior to sequencing.
  - Plant sequences removed to focus analyses on fungal communities.

- Data governance, reuse, and relevance for data leaders
  - Structured metadata file describing plots, treatments, vegetation, year, and per-SH abundances, enabling traceability and reuse.
  - SH-level data linked to detailed taxonomy and representative sequences, enabling cross-dataset comparisons and functional interpretation.
  - Taxonomic and functional assignments rely on established reference databases and community-accepted pipelines, supporting interoperability.
  - The dataset demonstrates end-to-end data lifecycle: field sampling, molecular assays, sequencing, bioinformatics, and quantified abundance measures with explicit metadata.
  - Useful for evaluating data strategy considerations: data availability, alignment of metadata with analyses, data quality control, and integration with wider data communities for forest-soil fungal ecology.