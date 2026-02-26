# Recovery and isolation of Kenyan Bacteroides spp. hosts from human and cattle faeces

## Purpose and scope
- Document the experimental design, sampling regime, and data collection methods used to recover and isolate Kenyan Bacteroides spp. hosts from human and cattle faeces, plus environmental monitoring for faecal indicators and bacteriophages.
- Provide a data-centric record of locations, sampling dates, laboratory procedures, and resulting datasets intended for subsequent phage detection and comparative analyses.

## Data collected and data files (data items and structure)
- Location data:
  - LocationOfFaecalSampling.csv — GPS coordinates of sampling sites (human pit latrines and cattle faecal sources); locational context in Siaya County, Kenya.
- Host isolation datasets:
  - IsolationOfBacteroidesHostsWeek10-6-18StepA.csv
  - IsolationOfBacteroidesHostsWeek10-6-18StepB.csv
  - IsolationBacteroidesHostsWeek17-6-18StepA.csv
  - IsolationBacteroidesHostsWeek17-6-18StepB.csv
  - These files contain codes, faecal origins (human or cattle), and details of the ten selected potential Bacteroides spp. hosts.
- Environmental detection datasets:
  - DetectionOfFIB&MSTmarkers.csv — detection levels of faecal indicator bacteria (Total coliforms, E. coli, intestinal enterococci) and somatic coliphages in water sources and at a wastewater plant; coordinates and sampling dates linked to sampling sites.
- Additional contextual data (sampling and dates):
  - Sampling of human and cattle faeces occurred 7–8 June 2018; isolation occurred 10–21 June 2018 at KEMRI Kisian labs; environmental sampling dates include 18–21 June 2018, 05–08 November 2018, and 13 June 2019.
- Phage detection data (implied workflow):
  - Bacteroides spp. phage detection using Kenyan hosts and a human-specific host, with subsequent plaque assays (PFU) in semi-solid media.

## Data collection and processing workflows
- Field sampling:
  - Human faeces: pooled samples (~25 g) from five pit latrines per school, collected with sterile tools and kept at ~4°C.
  - Cattle faeces: pooled samples (~25 g) from five stools at shorelines near water sources, collected similarly.
  - Samples transported to KEMRI Kisian labs within ~4 hours; stored up to 24 hours in refrigeration.
- Ethical approvals:
  - University of Southampton (ref 31554; approved 12/02/2018) and KEMRI SERU/CGHR (ref KEMRI/SERU/CGHR/091/3493; approved 17/10/2017); consent forms used for school headteachers.
- Laboratory workflow for Bacteroides hosts:
  - Isolation on BBE agar under anaerobic/aerobic conditions with stepwise subculturing and Gram staining to select Gram-negative obligate anaerobes.
  - Subculture to BBE and BPRM media, growth assessment, cryopreservation in Bovine Serum, and storage at -20°C for downstream phage testing.
  - Selection of 10 new potential hosts ( five from cattle, five from human sources) with specific codes (e.g., SIN.19, KN.1, etc.).
- Environmental detection workflows:
  - Detection of faecal indicator bacteria (FIB) and somatic coliphages (ISO methods 9308-1 and 7899-2; ISO 10705-2) via membrane filtration and selective plating (CCE agar, Slanetz and Bartley agar).
  - Detection of somatic coliphages using E. coli WG-5 and plaque assays on Modified Scholten’s medium; plaque counts converted to PFU/100 mL.
  - Detection of bacteriophages infecting Bacteroides spp. using GB-124 and Kenyan hosts (WAA.1, TIB.1, TIA.1, ONA.3, LU.2; SIN.19, KN.1, KN.2, KN.3, KN.8) with BPRMB/BPRMA and semi-solid media for plaque enumeration.
- Data lineage and records:
  - All data are tied to specific CSV files and linked to sampling locations and dates, enabling traceability from field collection to laboratory results.

## Geospatial and temporal metadata
- GPS coordinates collected using hand-held GPS devices; coordinates stored in LocationOfFaecalSampling.csv using World Geodetic System standards.
- Temporal data include precise sampling dates (7–8 June 2018 for faecal sampling; 10–21 June 2018 for host isolation; 18–21/06/2018; 05–08/11/2018; and 13/06/2019 for FIB/MST/phage detections).

## Standards, formats, and metadata considerations
- Data formats: CSV files for locations, host isolation results, and environmental detections.
- Geospatial metadata: coordinates standardized to WGS; explicit location contexts provided via accompanying CSV file.
- Analytical standards: ISO reference methods used for FIB and coliphage detection; standardized growth/media conditions described for reproducibility.
- Documentation of methods/parameters: detailed lab protocols, culture conditions, and incubation times included to support data reproducibility and future reuse.

## Ethical approvals, consent, and governance
- Ethics approvals recorded from University of Southampton and KEMRI; participant information and consent forms used for sampling from schools.
- Data governance considerations include handling of sample origin (human vs. cattle), maintenance of traceability through coded hosts, and explicit documentation of processing steps to support auditability.

## Data quality, provenance, and limitations
- Provenance established through stepwise documentation: field collection, transport, isolation, culture, and storage before phage assays.
- Quality controls embedded in methods: positive controls and blanks described for FIB and phage assays; use of standardized ISO methods for analysis.
- Limitations not explicitly stated but implied by field logistics and potential variability in sample transfer and stepwise processing across facilities and dates.

## Data access, sharing, and preservation
- Data are organized into clearly named CSV files with explicit linkage between sampling events, isolates, and environmental detections.
- For stewardship and reuse, ensure metadata completeness (sampling dates, locations, host codes, culture/media conditions, and assay parameters) to facilitate secondary analyses and cross-study comparisons.
- Preservation status implied by existing cryopreservation of isolates and temporal storage in the laboratory, with future reuse contingent on data traceability and documentation.

## Key data stewardship considerations
- Maintain consistent naming conventions for host codes and CSV files to preserve lineage and reproducibility.
- Ensure metadata capture of sample type, origin (human vs. cattle), collection method, and storage conditions accompanies all datasets.
- Retain links between field data, laboratory processing steps, and final detection results to enable end-to-end data lineage.
- Adhere to ISO method reporting for FIB and phage assays to support cross-study comparability.