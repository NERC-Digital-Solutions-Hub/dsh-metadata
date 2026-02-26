# Forestry England 2023 eDNA soil survey

- A large-scale baseline survey collecting 656 soil samples from 21 Forestry England sites to detect future change using environmental DNA (eDNA) metabarcoding.
- Three PCR primers used for metabarcoding: ITS2 (fungi), 18S (general eukaryotes/invertebrates), and COI (animals).
- Data generated include species presence/abundance (percentages and read counts), various biodiversity metrics, and comprehensive quality control (QC) information.

## Study design and sampling framework

- Sampling design aims to cover multiple plots per site, with a minimum of three plots per site; larger or more complex sites use a one-plot-per-100-hectare rule as appropriate.
- Within each plot, samples are collected from 5 locations, with 9 subsamples per location, combined into one composite site sample.
- Seasonal targeting to capture taxa with seasonally varying DNA (e.g., autumn/winter emphasis for fungi and arthropods in below-ground life stages).
- Detailed field protocols include risk assessments, biosecurity, glove usage, strict labeling, contamination prevention, and standardized core collection procedures.
- Option to use metal soil samplers to reduce plastic use; cores collected in a grid or adapted path (S-shape) to navigate vegetation and obstacles.
- Samples stored in cool conditions in the field, with explicit guidance for fridge/freezer preservation and return logistics (NatureMetrics cold-storage box and ice packs).

## Sample processing and laboratory protocol

- Environmental DNA metabarcoding conducted by NatureMetrics using three primers (ITS2, 18S, COI) to capture diverse taxonomic groups.
- Sample handling emphasizes contamination avoidance (gloves changed between locations, sealed bags, cleaned tools with bleach wipes, data sheets with GPS and date).
- Subsamples are homogenised into a single composite sample per plot, with careful labeling and tracking from field to lab.

## Data structure and content (14 files)

- Species Data Table Percentages (ITS2, 18S, COI): detects species in samples and the percentage of DNA sequences assigned to each species; includes taxonomic lineage, NMSeqID, sequence, common name, IUCN status, invasiveness, and prevalence across samples.
- Species Data Table Read Counts (ITS2, 18S, COI): analogous to percentages but reports raw read counts per species per sample.
- Metrics by Sample: includes sample-level metrics such as Species Richness, OTUs named at species level, Fungal Functional Diversity (based on a phylogenetic tree), Evolutionary Diversity (Faith's Phylogenetic Diversity), and site identifiers.
- QC Tables: record quality control outcomes for each sample, including DNA amplification success, sequencing QC, target OTU detection, and whether data were reported; includes target vs non-target proportions.
- Metadata: site, sample ID, sampling date, latitude/longitude, GPS error notes, and habitat type; highlights GPS coordinate anomalies (noted for 13 samples).
- Survey_description and related files: provide context and documentation for the dataset.

## Metrics and interpretation

- Species Richness: number of OTUs/species detected per sample.
- Fungal Functional Diversity: inferred through a functional hierarchy; indicates potential pathways of nutrient cycling and soil fertility when multiple taxa are present.
- Evolutionary Diversity (Faith's PD): measures breadth of phylogenetic relationships among detected taxa; higher values suggest greater ecological niches and ecosystem functioning.
- Target vs Non-Target proportions: percentage of DNA sequences belonging to targeted groups versus incidental detections, useful for assessing assay focus and incidental biodiversity information.
- QC-driven reporting: presence/absence of detectable targets, sequencing success, and contamination flags to ensure reliability of results.

## Quality control, data governance, and accessibility

- Comprehensive QC workflow reported at the sample level, including DNA amplification success, sequencing QC, and whether target OTUs were detected.
- Data transparency features:
  - Detailed metadata (location, sampling date, habitat) and GPS QA notes identifying potential coordinate errors.
  - Traceable sample identifiers (Sample ID, NMID, kit information) and a structured data schema across multiple files.
  - Availability of both percent-based and count-based data to support a range of analyses.
- Data governance considerations highlighted by the dataset’s structure:
  - Clear provenance from field collection to lab processing.
  - Standards for sample handling, cross-contamination prevention, and data curation (e.g., vendor-provided and lab-recorded QC metrics).
  - Metadata documenting data quality and potential limitations (e.g., GPS discrepancies).

## Limitations and notable considerations

- GPS coordinate errors in 13 samples require caution in spatial analyses and site attribution.
- Presence of non-target detections alongside target groups necessitates careful interpretation of ecological signals and management implications.
- Field and laboratory processes emphasize contamination prevention, but the complexity of eDNA data means careful QC and validation are essential for policy-relevant decisions.

## Relevance for monitoring frameworks

- Provides a robust baseline of soil biodiversity across Forestry England sites, enabling future change detection and policy evaluation.
- Multi-layer biodiversity metrics (species richness, functional diversity, evolutionary diversity) offer nuanced indicators of ecosystem health and functioning.
- The combination of comprehensive metadata, QC reporting, and clear sample provenance aligns with data governance best practices, supporting transparency, reproducibility, and data sharing opportunities.
- The structured data products (large suite of files with explicit descriptions) facilitate integration into monitoring dashboards, reports, and decision-making tools for environmental health monitoring.