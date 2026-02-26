# ReadMe file for SpringCH4Data.csv

- Purpose and scope: CH4 emissions measured from plots with control (no urine), artificial sheep urine, and real sheep urine treatments in a semi-improved upland grassland; spring 2016; randomised block design.
- Location and site details: Henfaes Research Station, Abergwyngregyn, North Wales (270 m above sea level; 53°13'N, 4°0'W).
- Data provenance and authorship: data collected by an automated greenhouse gas monitoring system; data authors should be acknowledged if reused or reproduced.
- Instrumentation and data collection: automated system at Queensland University of Technology, Institute for Future Environments, Brisbane, Australia, using a SRI 8610 GC.
- Sampling protocol: eight CH4 flux measurements per chamber per day; 1-hour chamber closure with four gas samples analyzed per closure; calibration standard processed after every fourth gas sample.
- Chamber specifications: basal area 0.25 m2; dimensions 50 cm × 50 cm × 15 cm (L × W × H).
- Data content and processing: the dataset contains quality-assessed flux data (not raw gas concentrations).
- Quality assurance: inspection of raw data files and GC chromatograms for anomalies; data points removed if anomalies (e.g., peak interference) were found.
- Data structure and schema:
  - Timestamp format: dd/mm/yy hh:mm
  - Columns B–M: CH4 fluxes (mg CH4-C m-2 h-1)
  - Metadata encoded in headers: treatment (Control, ArtUrine, Urine) and chamber/plot identifiers
- Usage and attribution: authors must be acknowledged for reused/reproduced data; dataset includes QA notes and treatment/plot mapping to support reuse and metadata traceability.
- Limitations and considerations for stewardship:
  - Flux data reflect processed, QA’d measurements, not raw concentrations
  - Site- and time-specific measurements; potential limitations for extrapolation beyond the study conditions
  - Documentation covers instrumentation, protocol, and data structure; no explicit update/versioning information provided.