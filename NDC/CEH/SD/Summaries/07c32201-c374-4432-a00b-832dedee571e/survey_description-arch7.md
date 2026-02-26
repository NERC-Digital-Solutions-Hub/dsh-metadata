# Forestry England 2023 eDNA soil survey

## Overview
- A wide-ranging soil eDNA survey across 21 Forestry England sites, collecting 656 samples.
- Aims to establish a baseline to detect future change.
- Environmental DNA metabarcoding performed on all samples using three primers: ITS2 (fungi), 18S (invertebrates), and COI (soil invertebrates/metazoa) by NatureMetrics.

## Sampling design and field methods
- Sampling framework:
  - At each site: multiple plots; at each plot: 5 sampling locations; at each location: 9 subsamples combined into one composite sample.
  - Minimum 3 plots per site; larger sites scale with area (1 plot per 100 ha for large complex sites; fewer for large simple sites).
  - Sampling typically in autumn or winter to target life-cycle periods of key groups.
- Field procedures and contamination control:
  - Complete risk assessment and biosecurity; gloves worn and changed between locations.
  - Unique sample IDs composed of year, district, site, project number, plot, and sampling location (e.g., 2023SNF1P1S1).
  - Core sampling using a syringe up to the 10 mL mark; adjust if obstacles are encountered; non-target adjustments allowed.
  - Composite samples created by homogenising nine subsample cores in a snap-lock bag; measures taken to prevent contamination.
  - Field storage in cooled conditions; samples kept at 4°C for short-term storage or frozen for longer transit; ice packs provided for shipping.
  - Alternative metal soil samplers available to reduce plastic use; sterilisation between locations recommended.
- Spatial design:
  - Cores collected in a grid pattern (10 m x 10 m) with potential S-shaped spacing; cores moved to gaps between plants in dense vegetation.
  - Documentation includes GPS location, date, and a photo for each sample.

## Data structure and contents
- Primary data files (14 total) from three primers:
  - ITS2 (Fungi): Fungi_percent.csv, Fungi_counts.csv, Fungi_metrics.csv, Fungi_QC.csv
  - 18S (Invertebrates): Invert_percent.csv, Invert_counts.csv, Invert_metrics.csv, Invert_QC.csv
  - COI (Soil Invertebrates/Metazoa): Soil_Invert_percent.csv, Soil_Invert_counts.csv, Soil_Invert_metrics.csv, Soil_Invert_QC.csv
  - Metadata.csv and Survey_description.docx
- Key data types:
  - Species Data Table Percentages: detected species per sample with percentage of DNA sequences, taxonomic lineage, NMSeqID, sequence data, common name, IUCN status, target status, invasive status, and sample occurrence counts.
  - Species Data Table Read Counts: similar to percentages but with raw read counts.
  - Metrics by Sample: per-sample metrics including:
    - Sample ID (Client Label)
    - Sample Type (field sample or control)
    - Species Richness (number of OTUs/species)
    - Number of OTUs named at species level
    - Fungal Functional Diversity (requires ≥3 species)
    - Faith's Phylogenetic Diversity (Evolutionary Diversity)
    - Site (sampling site)
  - Quality Control Table: per-sample QC details (DNA amplification, sequencing QC, target OTUs detected, percentage of target vs non-target, and overall reporting outcomes).
  - Metadata: site, sample ID, sampling date, latitude, longitude, GPS error notes, habitat type, and a flag for coordinates that may be erroneous.

## Data products and GIS relevance
- Spatially-referenced taxon data:
  - Per-sample species detections (percent and counts) with taxonomic assignments and metadata, enabling mapping of species distributions and taxonomic groups.
- Diversity and ecosystem function metrics:
  - Map Species Richness, Fungal Functional Diversity, and Faith's Phylogenetic Diversity across samples/sites to visualize spatial patterns of biodiversity and potential ecological niches.
- Quality and provenance:
  - QC and metadata enable filtering for high-quality samples and addressing GPS coordinate uncertainties in GIS analyses.
- Linking to site context:
  - Site-level field data and habitat type allow aggregation to site polygons and habitat-based thematic mapping.

## GIS-ready considerations and workflow recommendations
- Data preparation:
  - Import per-primer readouts and metadata as point features using Sample ID as the key; harmonize coordinate data from Metadata (lat/long) and flag or exclude samples with GPS errors.
  - Convert to a geodatabase or GIS-friendly formats; maintain the original Sample ID for traceability.
- Spatial analyses and mapping:
  - Create layers for:
    - Sample points with attributes: date, habitat, site, QC status, target detection status.
    - Per-sample metrics: Species Richness, Fungal Functional Diversity, Faith's PD (from Metrics by Sample).
    - Taxon-specific presence: separate layers or joined tables for ITS2, 18S, and COI results.
  - Produce choropleth maps by site or by grid to show spatial variation in diversity metrics.
  - Time-aware mapping by sampling date to examine temporal changes (baseline established; potential future updates).
- Data quality handling:
  - Use Metadata and QC fields to filter samples; address GPS errors by validating against site boundaries or excluding flagged points.
  - Acknowledge limitations of taxonomic resolution due to reference databases; interpret non-target vs target proportions carefully.
- Practical notes:
  - Ensure consistent coordinate reference system (e.g., WGS84) and document any coordinate corrections.
  - Consider integrating habitat type and site polygons for regional analyses and policy-oriented visuals.

## Use cases for policy and management
- Baseline biodiversity mapping across forestry sites to inform monitoring programs.
- Spatial prioritization of habitats with higher phylogenetic diversity or fungal functional diversity.
- Cross-site comparisons to identify ecological responses to management or environmental changes.
- Data-backed communication of ecosystem health to policy colleagues, clients, and the public.

## Metadata and provenance considerations
- GPS accuracy notes: 13 samples flagged for lat/long discrepancies; these should be verified or flagged in GIS projects.
- Sampling date and habitat metadata provide contextual layers for temporal and habitat-based analyses.
- Data provenance: three primers with separate result files enable cross-primer synthesis and validation.