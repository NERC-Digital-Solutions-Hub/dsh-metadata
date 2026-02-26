# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Overview
- Study assesses how two leech species (Haemadipsa picta and Haemadipsa sumatrana) contribute to sampling mammalian diversity via metabarcoding in North Borneo.
- Data are organized to support map-based analysis of mammal detections across sampled sites and habitats.

## Data products and structure
- Three CSV files central to the dataset:
  - Leech_Diet_Detections_pa.csv
    - Presence/absence matrix: mammal taxa (columns) x leech samples (rows).
    - Column headers use four-letter codes for mammalian taxa (e.g., Cerv, Hede, Hymu, Masp, etc.).
  - Leech_Diet_Detections_sample_Info.csv
    - Sample-level metadata for leech pools.
    - Fields include: species (leech pool: Tiger = H. picta; Brown = H. sumatrana), poolCode, habitat (frag or log), site (SAFE sites: B, F, LF, LFE, VJR), total detections, and other descriptors.
  - OTU_info.csv
    - Operational Taxonomic Unit (OTU) details for mammal assignments.
    - Fields include: Common name, Family (subfamily), Order, Taxa assigned, Code, OTU, Bit Score, %Identity, Sequence.
- Data support a linked workflow: detections by pool and sample, supplemented by OTU-level taxonomic context and sequence information.

## Sampling, sequencing, and bioinformatics (high-level)
- Study area and sampling design
  - Leech samples collected within SAFE project blocks: B, D, F, VJR, LF1, LF2, LF3, LFE.
  - Habitat types: fragments and logged forest.
  - Two leech species collected; sampling conducted during four visits per plot between February and June 2015.
  - Each plot involved 20-minute searches within 25 m^2 vegetation plots.
- Laboratory workflow (metabarcoding)
  - Tissue digestion of leech specimens.
  - Pooling digests by leech species and block; DNA extraction from pooled digests.
  - Amplification of a mammal-specific 16S rRNA fragment using tagged primers.
  - Library preparation: equimolar pooling, index PCR, Illumina MiSeq (150–250 bp, paired-end).
  - Bioinformatics: demultiplexing, read merging, quality filtering, removal of singletons, replication-based filtering (minimum appearance in two PCR replicates).
  - OTU clustering at 97%, followed by post-clustering filtering.
  - Taxonomy assignment via MEGAN (>150 bit score and 90% similarity); BLAST against a Bornean reference database.
  - Contamination control: samples filtered by minimum reads in control samples.

## Data specifics and fields (by file)
- Leech_Diet_Detections_pa.csv
  - Columns: presence/absence for each mammal taxon across samples.
  - Taxon codes include Cerv, Hede, Ecgy, Hymu, Masp, Hysp, Musp, Ruun, Rasp, Suba, Trsp, Trcr, Trfa, Vita.
- Leech_Diet_Detections_sample_Info.csv
  - Columns include:
    - species: leech pool species (T = H. picta, B = H. sumatrana)
    - poolCode: unique pool identifier
    - hab: habitat type (fragment or logged)
    - site: SAFE site code (B, F, LF, LFE, VJR)
    - frag/log: habitat subtype
    - totdetections: total detections in the pool
- OTU_info.csv
  - Columns include:
    - Common name, Family (subfamily), Order
    - Taxa assigned, Code, OTU
    - Bit Score, %Identity, Sequence

## Spatial and GIS relevance
- Spatial units and framing
  - Sites and blocks mapped across SAFE project locations; habitat types (fragments vs. logged forest) provide landscape context.
  - Data can be visualized as maps of mammal detections by site and by leech pool, with optional filtering by leech species.
- Potential map-based products
  - Presence/absence heatmaps or choropleth maps of mammal taxa across sites.
  - Leech-species-specific sampling coverage maps to assess spatial reliability.
  - OTU-to-species mappings overlaid with spatial distribution of sample pools.
- Integration opportunities
  - Combine with habitat maps, protected areas, or other spatial biodiversity data for policy and outreach visuals.
  - Link detections to sample locations, pool metadata, and sequencing quality controls for transparent GIS dashboards.

## Data quality and processing considerations
- Data are derived from pooled leech samples, introducing pooling-level aggregation that may affect site-level resolution.
- Multi-source data management: data reside in separate CSVs (detections, sample metadata, OTU information) requiring careful joins for GIS analyses.
- Quality controls include replication-based filtering and contamination checks through control-based thresholds.

## Practical guidance for GIS specialists
- How to use the data
  - Join Leech_Diet_Detections_pa.csv with Leech_Diet_Detections_sample_Info.csv on pool/sample identifiers to map detections by site, habitat, and leech species.
  - Use OTU_info.csv to translate OTU codes into mammal taxa and to incorporate sequence-based confidence metrics (Bit Score, % Identity) into map layers or tooltips.
  - Visualize by leech species to compare detection patterns between H. picta and H. sumatrana.
- Suggested visualizations
  - Site-level maps showing detected mammal taxa per site and per leech species.
  - Habitat-based comparisons (fragments vs. logged forest) of mammal detections.
  - OTU-level richness or taxonomic breadth per pool, with sequencing confidence annotations.

## Limitations and considerations for interpretation
- Detection data reflect presence/absence in pooled leech pools, not necessarily abundance or exact mammal counts.
- Spatial resolution tied to pool site locations; within-site heterogeneity may be undersampled.
- Taxonomic resolution depends on OTU clustering and reference database coverage; some identifications may be uncertain at finer levels.

## Summary takeaway for GIS use
- The dataset provides a structured, map-friendly framework to explore mammalian diversity detected through two leech species across multiple sites and habitats in North Borneo, with clear linkage between sample metadata, detections, and OTU-based taxonomic assignments. It supports comparative spatial analyses of detection patterns by leech species and habitat type, enabling informed visualizations and integrated GIS storytelling for policy, clients, or public audiences.