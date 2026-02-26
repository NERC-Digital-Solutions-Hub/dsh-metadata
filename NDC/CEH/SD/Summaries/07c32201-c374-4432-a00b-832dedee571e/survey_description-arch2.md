# Forestry England 2023 eDNA soil survey

## Overview and aims
- Wide-ranging baseline soil survey to detect future change in environmental conditions.
- 656 soil samples collected from 21 Forestry England sites nationwide.
- Environmental DNA metabarcoding performed on all samples using three primers: ITS2 (Fungi), 18S (eukaryotes), and COI (animals) by NatureMetrics.
- Outputs designed to support consistent, time-series assessments of environmental health and policy performance.

## Sampling design and field methods
- Multi-plot design: minimum of three plots per site (adjusted for site size: 1 plot per 100 ha for large complex sites; fewer for large simple sites).
- Within each plot: 5 sampling locations; at each location, 9 subsamples combined into one composite sample.
- Subsample collection protocol:
  - Conduct standard risk assessment and biosecurity.
  - Wear gloves to prevent contamination; change gloves between locations.
  - Use a fixed sample ID scheme encoding year, district, site, project, plot, and location.
  - Collect cores by inserting a syringe/core to a 10 mL mark; use a rubber mallet if needed; move around obstacles.
  - Combine 9 subsamples per plot into a single 10 mL composite sample in a snap-lock bag; homogenise.
  - Label bags, avoid cross-contamination, and keep samples cool in the field (ice packs or cold storage).
  - Prefer metal soil samplers to reduce plastic use; clean between locations.
  - Record GPS, date, and photo; store data on a data sheet.
- Sample handling and storage:
  - Field bags sealed between subsamples; cores cleaned between locations with bleach wipes.
  - In-field storage: fridge at 4°C for a few days if shipping to lab soon; otherwise freeze prior to transport.
  - Return kit provided by NatureMetrics for 5–50 samples; ice packs must be pre-frozen for 72 hours.
- Documentation and traceability:
  - Cores collected in a grid/S-pattern; GPS and site notes logged for each sample.
  - Data sheets and labelled bags stored together in a cool container for transport.

## eDNA analysis and lab specifics
- Three primers used for metabarcoding: ITS2 (Fungi), 18S (eukaryotes), COI (metazoans).
- Analysis conducted by NatureMetrics; contact NatureMetrics for details.

## Data collected and key outputs
- Data files (14 total) span species detection, read counts, quality control, and metadata:
  - Species Data Table Percentages (per sample): detected species with percentage of DNA sequences; taxonomic details include NMSeqID, sequence, taxonomic levels, common name, IUCN status, target vs non-target, invasive status, and sample occurrence.
  - Species Data Table Read Counts: analogous to percentages but with raw read counts for publishable analyses.
  - Metrics by Sample: per-sample metrics including Species Richness, OTUs named at species level, Fungal Functional Diversity, Evolutionary Diversity (Faith’s Phylogenetic Diversity), and site information.
  - Quality Control Tables: detailed progress and outcomes of QC steps (DNA amplification, sequencing QC, target OTUs detected, and overall reported status); includes Field blanks considerations.
  - Metadata: site, sample ID, sampling date, latitude/longitude (with an explicit note on GPS errors for 13 samples), habitat type.
  - Survey_description.docx: document describing the survey (context and methods).
- Key metrics explained:
  - Fungal Functional Diversity: functional diversity inferred from a tree of detected functions; higher values suggest more nutrient-cycling pathways and potentially higher soil fertility.
  - Faith’s Phylogenetic Diversity (Evolutionary Diversity): diversity based on how distantly related detected species are; broader and deeper phylogenetic representation indicates richer ecological niches.

## Quality assurance, data integrity, and accessibility
- Emphasis on verification, QA/QC, and data cleaning as part of the monitoring workflow.
- Sample-level QC includes DNA amplification success, sequencing QC, and whether target OTUs were detected; “Reported” indicates samples that passed QC and contained target and/or non-target data.
- GPS data quality noted; 13 samples flagged for lat/long discrepancies to aid data correction and interpretation.
- Data are structured to enable re-use and cross-site comparisons; outputs are designed to be accessible for monitoring over time and for sharing underlying data where appropriate.

## Site, habitat, and metadata considerations
- Site-level context captured to support habitat-based analyses.
- Metadata includes broad habitat type, sampling date, and precise site identifiers; explicit attention to location accuracy improves spatial analyses and trend detection.

## Implications for environmental monitoring and use
- Provides a standardized, auditable baseline dataset for soil biodiversity and ecosystem function across multiple Forestry England sites.
- Multimarker approach (ITS2, 18S, COI) enables broad taxonomic coverage including fungi, invertebrates, and other eukaryotes.
- Outputs support assessment of biodiversity status, functional capacity, and evolutionary diversity, contributing to gap analyses and policy evaluation over time.
- The structured data framework and QA emphasis align with the Analysts Monitoring the Environment archetype’s goals of verifiable, openly comparable environmental health data and transparent methodologies.