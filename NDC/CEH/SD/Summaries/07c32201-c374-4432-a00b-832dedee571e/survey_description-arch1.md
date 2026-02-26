# Forestry England 2023 eDNA soil survey

- A wide-ranging survey collecting 656 soil samples from 21 Forestry England sites to establish a baseline for future change; environmental DNA metabarcoding conducted with ITS2, 18S, and COI by NatureMetrics.

## Aim and scope
- Baseline eDNA data to detect future ecological change across multiple Forestry England sites.
- Taxonomic and functional biodiversity information derived from three genetic markers (ITS2 for fungi, 18S for general eukaryotes, COI for metazoans).

## Study design and field sampling
- Sites and plots
  - Minimum of 3 plots per site (adjusted by site size and complexity; 1 plot per 100 ha for large complex sites; fewer for large simple sites).
- Sampling per plot
  - Each plot comprises 5 sampling locations.
  - At each location, 9 subsamples are collected and combined into one composite sample.
  - Standard field risks, biosecurity procedures, and gloves are used to minimise contamination.
- Sampling cadence
  - Sampling window focused on specific months (e.g., autumn or winter) to target arthropods and fungi life cycles.
- Sample labeling and collection
  - Detailed sample IDs incorporating year, district, site, project, plot, and sampling location (e.g., 2023SNF1P1S1).
  - Sub-sample cores collected with a syringe, homogenised in a snap-lock bag, and stored in a cool bag with ice.
  - Optional metal soil samplers allowed; all tools cleaned between locations and bleached as needed.
- Storage and handling
  - Field bags sealed, data sheets completed with GPS, date, and photos.
  - In-lab handling includes cold storage; samples kept at 4°C for a few days or frozen for longer transport.

## Laboratory methods
- Environmental DNA metabarcoding
  - Three primers used: ITS2 (fungi), 18S (general eukaryotes), COI (metazoans).
  - Analysis performed by NatureMetrics.

## Data structure and outputs
- Fourteen data files plus descriptive documents are provided:
  - Fungi_percent.csv (ITS2): Species data table percentages.
  - Fungi_counts.csv (ITS2): Species data table read counts.
  - Fungi_metrics.csv (ITS2): Metrics by sample.
  - Fungi_QC.csv (ITS2): Quality control for samples.
  - Invert_percent.csv (18S): Species data table percentages.
  - Invert_counts.csv (18S): Species data table read counts.
  - Invert_metrics.csv (18S): Metrics by sample.
  - Invert_QC.csv (18S): Quality control for samples.
  - Soil_Invert_percent.csv (COI): Species data table percentages.
  - Soil_Invert_counts.csv (COI): Species data table read counts.
  - Soil_Invert_metrics.csv (COI): Metrics by sample.
  - Soil_Invert_QC.csv (COI): Quality control for samples.
  - Metadata.csv: Site, sample IDs, sampling date, latitude/longitude, habitat, etc.
  - Survey_description.docx: Description of the survey (parallels to method document).
- Species Data Table Percentages (per sample)
  - Contains detected species with DNA sequence percentage per sample, NMSeqID, sequence, taxonomic assignments (Kingdom to Species), common name, IUCN status, target status, invasive status, and number of samples where OTU occurs.
- Species Data Table Read Counts (per sample)
  - Similar structure to percentages but reports read counts instead of percentages, enabling downstream publication and analyses.
- Metrics by Sample Table
  - Per-sample metrics including: Sample ID, sample type (field vs control), Species Richness, number of species named at species level, Fungal Functional Diversity, Evolutionary Diversity (Faith’s Phylogenetic Diversity), and site information. Fungal Functional Diversity and Evolutionary Diversity require ≥3 species to be computed.
- Quality Control Tables
  - Detailed QC for each sample: kit info, NMID, sample type, volume filtered, date received, DNA amplified QC, sequencing QC, target OTUs detected, percent target/non-target, and reported outcomes including contamination flags if present.
- Metadata
  - Location and date, habitat type, and notes on GPS accuracy; 13 samples flagged for GPS coordinate inconsistencies.

## Key metrics and interpretations
- Species Richness
  - Count of OTUs/species detected per sample.
- Fungal Functional Diversity
  - Measures breadth of functional roles across fungi within a sample; higher values imply more nutrient cycling pathways.
- Evolutionary Diversity (Faith’s Phylogenetic Diversity)
  - Assesses phylogenetic breadth and ecological niches; higher values indicate greater biodiversity and ecosystem resilience.

## Data quality and provenance
- Quality control emphasizes adequate DNA amplification and sequencing, target OTU detection, and contamination checks.
- Metadata includes GPS accuracy notes; 13 samples have GPS errors, with raw coordinates still provided for traceability.
- Clear documentation of sample handling steps and storage conditions to ensure reproducibility.

## Considerations for analysis and reuse
- Data are organized by primer and taxon group (fungi, invertebrates/other eukaryotes via 18S, and COI metazoans), with both relative (percent) and absolute (read counts) abundance measures.
- Taxonomic assignments depend on reference databases; species-level IDs may be unavailable for some sequences.
- Non-target detections are reported and distinguishable from targets in QC and reporting.
- Data and accompanying descriptions support reproducible analyses and potential data portal deposition with metadata.

## Practical notes for analysts
- Ensure alignment of sample IDs across files to enable integrated analyses (e.g., linking Species Data Tables with Metrics by Sample and QC tables).
- Consider both target OTUs and non-target detections in ecological interpretations.
- Use Faith’s PD and fungal functional diversity cautiously, ensuring sufficient species counts per sample (3+ species required).
- Be mindful of GPS caveats when spatial analyses are conducted; consider validating coordinates against site records.