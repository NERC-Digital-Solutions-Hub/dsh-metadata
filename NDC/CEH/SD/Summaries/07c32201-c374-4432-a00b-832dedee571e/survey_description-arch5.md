# Forestry England 2023 eDNA soil survey

## Overview
- Wide-ranging environmental DNA (eDNA) soil survey to establish a baseline for future change.
- 656 soil samples collected from 21 Forestry England sites; analyzed via metabarcoding using three primers (ITS2, 18S, COI) by NatureMetrics.

## Study design and sampling
- Sampling at each site includes multiple plots; at each plot, samples from 5 locations; 9 subsamples per location combined into one composite sample.
- Minimum of 3 plots per site; larger sites use 1 plot per 100 ha; sampling typically conducted in specific months (e.g., autumn/winter).
- Detailed sample identification scheme used to encode year, district, site, project, plot, and sampling location.

## Field collection and handling procedures
- Conduct standard risk assessment and biosecurity for fieldwork; follow instructional video guidelines.
- Wear gloves to minimize contamination; change gloves between sampling locations.
- Label sample bags with a unique Sample ID (e.g., 2023SNF1P1S1) and record GPS, date, and a photo.
- Collect cores by inserting a syringe into the soil to a 10 mL mark, then extract and expel into a labeled bag; homogenize nine subsamples in a 10 m x 10 m plot.
- Use of metal soil samplers as an alternative to reduce plastic; clean tools with bleach between locations.
- Core locations arranged in a grid or systematic pattern; adjust for obstacles (roots, rocks) as needed.
- After collection, store samples in sealed bags within coolers; in-field storage cryopreservation as needed.
- In-lab: samples kept at 4°C for short-term or frozen for longer storage; NatureMetrics provides cold-storage return boxes and ice packs.

## Laboratory analysis
- Environmental DNA metabarcoding performed on all samples using ITS2 (fungi), 18S (invertebrates), and COI (mammals/fish/others).
- Results generated and stored by NatureMetrics; contact NatureMetrics for details.

## Data structure and files
- Fourteen data files and a survey description are provided, covering taxonomic data, counts, metrics, quality control, and metadata.
- Key data files include:
  - Species Data Table Percentages (ITS2): detects species per sample with percentage of DNA sequences; includes NMSeqID, Sequence, full taxonomy (Kingdom to Species), Common Name, IUCN status, Target Status, Invasive status, number of samples where OTU occurs, and sample IDs.
  - Species Data Table Read Counts (ITS2): same structure but with read counts instead of percentages.
  - Metrics by Sample (per primer): includes Sample ID, Sample Type, Species Richness, Number of OTUs named at species level, Fungal Functional Diversity, Evolutionary Diversity (Faith’s Phylogenetic Diversity), and Site.
  - Quality Control (per primer): records about sample processing, DNA amplification QC, Sequencing QC, Target OTUs Detected, and whether results were Reported.
  - Invert and Soil_Invert groups: read counts, percentages, metrics, and QC for 18S and COI respectively.
  - Metadata.csv: site, sample ID, sampling date, latitude, longitude, habitat, and notes on GPS errors.
  - Survey_description.docx: overview of the survey methodology and structure.

## Data fields and interpretation
- Species Data tables provide either percentage or count of DNA sequences per detected OTU per sample; includes taxonomic resolution (genus/species where possible) and status fields (IUCN, invasive, target vs non-target).
- Non-targets are reported and provide additional context but are not included in core metrics.
- Metrics by Sample summarize biodiversity and functional/phylogenetic diversity, aiding interpretation of soil biodiversity and ecosystem functioning.
- Metadata captures sampling context and potential GPS anomalies (13 samples with GPS coordinate errors noted).

## Quality control and data quality
- Quality Control tables document DNA amplification and sequencing QC outcomes, including whether target OTUs were detected and whether samples were reported.
- QC outcomes influence whether a sample’s data are included in final analyses and reporting.

## Metadata and data provenance
- Metadata file includes precise sampling date, latitude, longitude, habitat type, and site-level context.
- GPS data quality is explicitly QA’d; any anomalies are flagged for follow-up.

## Data stewardship implications
- The dataset is comprehensive and multifaceted, requiring careful governance to maintain consistency across primers and data tables.
- Actions for data stewards:
  - Ensure consistent sample IDs and linkage across all 14 data files and metadata.
  - Maintain documentation of field protocols, lab methods, and QC criteria for reproducibility.
  - Monitor GPS data quality and flag errors; preserve original coordinates alongside QA-adjusted values.
  - Store data in an accessible repository with clear metadata to support discovery and reuse.
  - Coordinate with NatureMetrics for data updates and clarifications; enable timelines for data sharing and potential revisions.
  - Preserve non-target data while emphasizing core target OTUs for reporting and downstream analyses.