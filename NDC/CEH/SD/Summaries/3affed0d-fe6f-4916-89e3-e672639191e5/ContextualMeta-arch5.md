# Using metabarcoding to compare the suitability of two blood-feeding leech species for sampling mammalian diversity in North Borneo

## Overview
- Purpose: Assess the suitability of two leech species (Haemadipsa picta and Haemadipsa sumatrana) for metabarcoding-based sampling of mammal diversity in North Borneo.
- Data described: three CSV datasets linked to the study:
  - Leech_Diet_Detections_pa.csv — presence/absence matrix of mammal taxa detections across leech samples (taxa as four-letter codes; rows = leech samples; columns = mammal taxa).
  - Leech_Diet_sample_Info.csv — sample metadata for each leech pool (leech species, poolCode, habitat, site, total detections, habitat type).
  - OTU_info.csv — OTU-level information including taxonomy, code, OTU ID, sequence data, BLAST bit scores, and percent identity.
- Study design:
  - Sampling sites within SAFE project blocks representing two habitat types: fragments and logged forest.
  - Two leech species collected during 20-minute searches in 25 m2 plots across blocks, February–June 2015, with four visits per plot.
  - Metabarcoding and high-throughput sequencing performed on pooled samples at University of Copenhagen and Queen Mary University London.
- Sequencing and analysis workflow (high-level):
  - Tissue digestion of leeches; pooling by species and block; amplification of mammal-specific 16S rRNA fragments with tagged primers.
  - Illumina MiSeq sequencing (150–250 bp, paired-end); demultiplexing; quality filtering; removing singletons; requiring detection in at least two PCR replicates.
  - OTU clustering at 97% similarity; OTU refinement; taxonomic assignment via MEGAN (>150 bit score, ≥90% similarity) and BLAST against a curated Bornean reference database.
  - Contamination controls via minimum reads in control samples.
- Outputs enable linking detections to sample metadata and OTU-level taxonomic information for downstream analyses.

## Data assets and structure
- Leech_Diet_Detections_pa.csv
  - Type: Presence/absence matrix.
  - Rows: leech samples.
  - Columns: four-letter codes for mammalian taxa (e.g., Cerv for Cervinae; Hede for Hemigalus derbyanus; Hymu for Hylobates sp; Musp for Muntiacus spp; etc.).
- Leech_Diet_Detections_sample_Info.csv
  - Type: Sample metadata.
  - Fields include: species (leech pool species: T = Haemadipsa picta; B = Haemadipsa sumatrana), poolCode, hab (fragment or logged), site (SAFE site codes: B, F, LF, LFE, VJR), totdetections, and log (habitat type flag).
- OTU_info.csv
  - Type: OTU-related taxonomy and sequence data.
  - Fields include: Common name, Family (subfamily if applicable), Order, Taxa assigned, Code, OTU, Bit Score, %Identity, Sequence.

## Data collection, processing and quality controls
- Field collection
  - Blocks span two habitat types: fragments and logged forest.
  - Two leech species collected: Haemadipsa picta (Tiger leech pool) and Haemadipsa sumatrana (Brown leech pool).
  - Sampling involved four visits per plot within February–June 2015.
- Laboratory workflow (metabarcoding and sequencing)
  - Tissue digestion of leeches; pooling within leech species and block; DNA extraction.
  - Amplification of a tagged mammal-specific 16S rRNA fragment; library preparation and indexing; Illumina MiSeq sequencing.
- Bioinformatics and data curation
  - Demultiplexing, quality filtering, removal of singletons.
  - OTU clustering at 97%; post-clustering refinement.
  - Taxonomic assignment via MEGAN with thresholds; BLAST against a curated GenBank-derived Bornean reference database.
  - Contamination control via minimum reads in control samples.

## Data governance and stewardship considerations
- Metadata and standards
  - Maintain clear definitions for sample metadata fields (species pools, poolCode, habitat, site, etc.) and for mammal taxon codes (four-letter taxa abbreviations) to ensure consistent interpretation.
  - Document reference databases and versioning used for BLAST and taxonomy (e.g., curated Bornean reference database).
  - Record all processing steps and software versions used in the pipeline (demultiplexing, filtering criteria, OTU clustering threshold, taxonomic assignment thresholds, etc.).
- Provenance and reproducibility
  - Link detections matrix to corresponding sample metadata and OTU records.
  - Preserve full pipeline provenance: from tissue digestion through sequencing to final taxonomic assignments.
- Data quality and sharing
  - Include QA/QC notes (e.g., criteria for removal of singletons, minimum reads in controls, presence in at least two PCR replicates).
  - Plan for data deposition in appropriate data portals or catalogues; document data sharing constraints, and any embargoes or licensing needs.
- discoverability and interoperability
  - Provide a data dictionary and codebooks mapping taxon codes to full taxon names, and mapping site/habitat codes to descriptive terms.
  - Ensure machine-readable formats (CSV with consistent encoding) and stable identifiers (e.g., poolCode, OTU IDs).

## Reuse and potential applications
- Enables cross-study comparisons of mammal biodiversity inferred from leech-derived DNA.
- Useful for updating or reanalyzing with new reference databases, alternative OTU clustering thresholds, or different taxonomic assignment tools.
- Supports methodological evaluation of leech species for non-invasive mammal monitoring and ecological surveys.

## Challenges and risks (relevant to data stewardship)
- Incomplete alignment between user needs and metadata scope; ensuring metadata completeness is critical.
- Timely acquisition of data and consistent adherence to metadata standards across all datasets.
- Interoperability across different data systems and formats; handling legacy or outdated references/databases.
- Managing large datasets and ensuring reproducibility across diverse computational workflows.

## Recommendations for data management and stewardship
- Create a comprehensive data dictionary and data provenance record detailing:
  - File names, descriptions, and content of all three CSV files.
  - Field definitions, units, allowed values, and code mappings (e.g., taxa codes, site codes, habitat codes).
  - Versions and sources of reference databases and software tools used in analysis.
- Preserve and publish full workflow provenance, including:
  - Step-by-step methods for the laboratory and computational pipeline.
  - Parameters for QC filters, OTU clustering, and taxonomic assignment thresholds.
- Ensure data and metadata alignment to enhance discoverability:
  - Link detections data to sampleInfo and OTU_info via poolCode and OTU IDs.
  - Provide a clear mapping between four-letter taxon codes and full taxon names.
- Plan for data sharing with appropriate governance:
  - Define licensing, access controls, and any embargo periods.
  - Provide guidance for re-use, including assumptions about reference databases and taxonomic resolution.