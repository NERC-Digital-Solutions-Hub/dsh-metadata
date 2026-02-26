# Forestry England 2023 eDNA soil survey

- Purpose and scope
  - Wide-ranging environmental DNA (eDNA) soil survey to establish a baseline for future change.
  - 656 soil samples from 21 Forestry England sites; metabarcoding performed using ITS2, 18S, and COI primers by NatureMetrics.

- Collection design and field procedures
  - Multi-plot sampling per site: multiple plots, 5 sampling locations per plot, 9 subsamples per location, 1 kit per location.
  - Minimum target: at least 3 plots per site; plotting strategy scales with site size (1 plot per 100 ha for larger sites, fewer for large simple sites).
  - Seasonal sampling window to align with lifecycle stages of organisms (e.g., autumn/winter for fungi and some arthropods).
  - Sample ID format and labeling: year, district, site, project, plot, sampling location (e.g., 2023SNF1P1S1).
  - Litter handling and core collection: remove surface litter, use syringe-based core to 10 mL mark, adjust for obstacles, use gloves to avoid contamination, label bags, and maintain clean transfer between locations.
  - Homogenization and packaging: combine nine subsample cores per plot into one composite sample, seal to prevent contamination, and clean tools between locations.
  - Storage and transport: field cooling; use grey bags within cool packs; if delayed, refrigerate at 4°C for short-term or freeze before return; NatureMetrics cold-storage box available for 5–50 samples.
  - Alternative equipment: metal soil samplers suggested to reduce plastic use; sterilize between locations.
  - Documentation: record sample ID, GPS, photo, and date; grid or S-shaped core pattern guidance; maintain traceability.

- Laboratory workflow and data generation
  - Environmental DNA metabarcoding performed on all samples using ITS2 (Fungi), 18S (Invertebrates), and COI (Soil Invertebrates) by NatureMetrics.
  - Contact NatureMetrics for details and support.

- Data structure and contents
  - Fourteen data files in total, organized by primer and metadata:
    - Fungi-related: Fungi_percent.csv, Fungi_counts.csv, Fungi_metrics.csv, Fungi_QC.csv (ITS2)
    - Invertebrates (18S): Invert_percent.csv, Invert_counts.csv, Invert_metrics.csv, Invert_QC.csv
    - Soil/COI: Soil_Invert_percent.csv, Soil_Invert_counts.csv, Soil_Invert_metrics.csv, Soil_Invert_QC.csv
    - Metadata and survey context: Metadata.csv, Survey_description.docx
  - Species Data Table Percentages (per sample)
    - Contains detected species with percentage of DNA sequences per species.
    - Includes NMSeqID (unique sequence code), Sequence, taxonomic assignments (Kingdom to Species), Common Name, IUCN status, Target status, Invasive status, and occurrence counts across samples.
    - Also notes Non-Targets and sample-level presence (sample IDs like 2023C BP1 P1 S2).
  - Species Data Table Read Counts (per sample)
    - Similar structure to percentages but reports raw read counts instead of percentages.
  - Metrics by Sample Table
    - Per-sample metrics including: Sample ID (Client Label), Sample Type (field vs control), Species Richness, Number of OTUs named at species level, Fungal Functional Diversity, Evolutionary Diversity (Faith’s Phylogenetic Diversity), Site.
    - Describes how metrics are calculated and their interpretation (e.g., higher Fungal Functional Diversity implies more nutrient-cycling pathways).
  - Quality Control Table
    - Sample-by-sample QC status: kit ID, NMID, Client Label, Sample Type, Volume Filtered, Date Received.
    - DNA Amplified and Sequencing QC pass/fail indicators, Target OTUs Detected, and % Target vs % Non-Target.
    - Reported field indicating whether target or non-target species were detected and notes on contamination (e.g., field blanks).
  - Metadata
    - Core fields: Site, Sample ID, Sampling date, Latitude, Longitude, Lat/Long Error, Habitat.
    - Note on GPS issues: 13 samples show GPS coordinates that do not match expected sites; QA highlights and original coordinates retained for traceability.

- Key outputs and potential data products
  - Species presence/abundance tables by sample (percentages and read counts) enabling cross-site comparisons.
  - Sample-level biodiversity and ecological metrics (Species Richness, Fungal Functional Diversity, Evolutionary Diversity) for dashboards, reports, or publications.
  - QC-driven data quality assessment to support reliable downstream analyses and reproducibility.
  - Metadata and GPS information to support spatial analyses and data governance.

- Data quality and governance notes
  - Explicit quality control steps documented for each sample, including DNA amplification and sequencing QC.
  - Some GPS coordinate discrepancies identified and flagged in metadata, with original values retained.
  - Data structure is designed to support traceability from sequence data back to samples, kits, and field collection events.

- Practical implications for data support
  - Emphasizes rigorous field data capture, consistent sample IDs, and comprehensive metadata to enable self-serve data exploration and robust analyses.
  - The structured outputs (percentages, counts, and multiple metrics) support building dashboards, pivots, and comparative analyses across sites and time.
  - Clear pathways for data quality improvement and dissemination, including sharing early prototypes and possibly advocating for improved data creation and standardization across projects.