# Forestry England 2023 eDNA soil survey

## Overview
- Wide-ranging environmental DNA (eDNA) soil survey to establish a baseline for future change.
- 656 soil samples collected from 21 Forestry England sites.
- eDNA metabarcoding performed using ITS2, 18S, and COI primers by NatureMetrics.

## Study design and field collection
- Sampling structure
  - Multiple plots per site; minimum of 3 plots per site; larger sites scale to 1 plot per 100 ha (or fewer for large simple sites).
  - At each plot: 5 sampling locations; at each location: 9 subsamples combined into one composite sample.
  - One kit per sampling location; grid-based collection with some flexibility (S-shaped pacing allowed).
- Timing and scope
  - Sampling months chosen to align with target taxa (e.g., autumn/winter for arthropods; autumn for fungi).
- Field protocols to prevent contamination
  - Pre-field risk assessment and biosecurity; use of gloves; change gloves between locations.
  - Labeling scheme: sample ID includes year, district, site code, project number, plot, and sampling location.
  - Litter management: push aside leaf litter but avoid highly fragmented material; core collected with syringe to 10 mL mark; use mallet if needed.
  - Core handling: suction to transfer soil into snap-lock bags; seal between subsamples; clean equipment between locations.
  - Storage: cool bag with ice packs in the field; samples kept at 4°C for short-term; freeze before return if not shipped promptly; optional use of metal soil samplers to reduce plastic and improve reliability; bleach wipes between locations.
  - Core processing: nine subsample cores per 10 m x 10 m plot homogenised in a single bag; massaged and rolled to expel air before sealing.
- Logistics
  - Cores may be moved to avoid obstacles; if vegetation or rock blocks a point, relocate to a feasible spot.
  - Detailed documentation: GPS location, photo, date recorded on data sheet; sample and data sheets placed in grey storage bag for transport.

## Laboratory processing and storage
- Environmental DNA metabarcoding performed on all samples using three primers (ITS2 for fungi, 18S for general eukaryotes, COI for animals) by NatureMetrics.
- Storage and return
  - NatureMetrics provides a cold-storage return box for 5–50 samples; ice packs require 72 hours to freeze before shipping.

## Data structure and file overview
- Fourteen data files plus a survey description and metadata, organized by primer target and data type:
  - Fungi-related: Fungi_percent.csv, Fungi_counts.csv, Fungi_metrics.csv, Fungi_QC.csv (primer ITS2)
  - Invertebrate/other eukaryotes (18S): Invert_percent.csv, Invert_counts.csv, Invert_metrics.csv, Invert_QC.csv (primer 18S)
  - Soil COI (metazoans): Soil_Invert_percent.csv, Soil_Invert_counts.csv, Soil_Invert_metrics.csv, Soil_Invert_QC.csv (primer COI)
  - Metadata.csv: site, sample IDs, GPS coordinates, habitat, etc.
  - Survey_description.docx: methodology and data structure summary
- Content highlights by file type
  - Species Data Table Percentages
    - Detected species per sample; percentage of DNA sequences per species.
    - Fields include NMSeqID, Sequence, Kingdom, Phylum, Class, Order, Family, Genus, Species, Common Name, IUCN Threat Status, Target Status, Invasive Status, Number of samples where OTU occurs, Sample IDs (e.g., 2023SNF1P1S2).
  - Species Data Table Read Counts
    - Similar to percentages but with read counts (DNA sequence counts) per species per sample.
  - Metrics by Sample Table
    - Per-sample metrics: Species Richness (OTUs/species), Number of OTUs named at species level, Fungal Functional Diversity, Evolutionary Diversity (Faith’s Phylogenetic Diversity), Site, Sample Type (field vs. control).
  - Quality Control Table
    - Sample-level QC status: Kit ID, NMID, Client Label, Sample Type, Volume Filtered, Date Received, DNA Amplified QC, Target OTUs Detected, Sequencing QC, % Target, % Non-Target, Reported, and related notes.
  - Metadata
    - Site, Sample ID, Sampling date, Latitude, Longitude, GPS error notes, Habitat description.

## Key metrics and interpretation
- Species Richness: number of OTUs/species detected per sample.
- Fungal Functional Diversity: breadth of fungal functional roles per sample; higher values imply more nutrient-cycling pathways.
- Evolutionary Diversity (Faith’s PD): phylogenetic breadth of detected taxa; higher values indicate a more functionally diverse ecosystem.
- Target vs. Non-Target composition: percentage breakdown helps distinguish focal taxa from incidental detections; non-targets still provide ancillary information.

## Data quality, governance, and usability
- Quality control is documented per sample, including DNA amplification success and sequencing QC; only samples passing QC contribute to reported results.
- Metadata quality notes
  - GPS validation identified errors in 13 samples; these are flagged in the metadata with notes on location discrepancies.
- Data traceability and reuse
  - Use of NMSeqID and standardized Sample IDs enables traceability across sites and analyses.
  - Data are structured for cross-site biodiversity comparisons and longitudinal baselines.
- Access and contact
  - Data are associated with NatureMetrics processing; for more information or access to data, contact NatureMetrics and Forestry England as indicated in the documentation.

## Implications for Data Leaders
- End-to-end data stewardship: clear sampling design, robust field protocols, and comprehensive QC enable trustworthy, reusable data assets.
- System-wide data perspective: data are organized by site, sample, and primer, supporting cross-network comparisons and collaboration with partners.
- Data gaps and challenges to anticipate
  - Incidental (non-target) detections provide additional insights but require careful interpretation.
  - GPS discrepancies require curation to ensure accurate site-level analyses.
  - Taxonomic assignments depend on reference databases; some detections may be at higher taxonomic levels if exact matches are unavailable.
- Practical takeaways
  - The document demonstrates a rigorous data structure with explicit data products, making it suitable for integration into wider data ecosystems and long-term biodiversity monitoring programs.