# Global_river_decomposition_assay_data_2016_17.csv

## Overview
- Purpose: Data to investigate how decreasing catchment glacier cover influences fungal decomposition of organic matter in mountain rivers.
- Scope: Field observations, laboratory processing, and statistical analysis from sites in Alaska, Austria, Ecuador, France, New Zealand, and Norway during 2016–2017.
- Data file: Accompanies the data file Global_river_decomposition_assay_data_2016_17.csv.
- Data types: Three observation categories documented (physicochemical parameters, cotton-strip decomposition metrics, and fungal ITS/cbhI molecular data with community composition).

## Data contents and structure
- Three data groups (Table 2 definitions):
  - Physicochemical data: catchment glacier cover (%CGC), mean river temp (temp, °C), pH, optical turbidity (turb, NTU), Pfankuch index (1/Pfankuch).
  - Decomposition data: tensile-strength loss metrics (TS_DD, TS_D, and SD variants) with temperature-adjusted degree-days (DD) and days; units include (%)(N/degree-day) and (%)(N/day); includes standard deviation (SD).
  - Fungal ITS and cbhI data: ITS and cbhI gene copy numbers per cm² of cotton strip (via qPCR), saprotrophs/Ascomycota/Tetracladium relative abundances (PCR-based, OTU-level proportions or copy numbers).
- Units and parameter definitions are provided explicitly (Table 2).

## Study sites and geographic coverage
- Site list includes multiple labeled locations (A1–A14, E1–E10, F1–F10, NZ1–NZ3, N1–N14, USA1–USA5) with corresponding latitude/longitude coordinates.
- Geographic spread encompasses Europe, North America, New Zealand, Ecuador, and additional regions (as listed in the site table).

## Data collection and methods
- Cotton-strip assay:
  - Four cotton strips per site (up to six at highly unstable sites).
  - Incubation period: 31–39 days.
- Physicochemical measurements:
  - temp: mean river water temperature during incubation periods; measured with various data loggers (iButton, HOBO, TinyTag) depending on site.
  - pH: initial site measurement with multiple handheld meters.
  - turb: ex-situ optical turbidity from initial 100 mL sample using HACH equipment.
  - Pfankuch: bottom-component index of channel stability measured at study start (except Alaska).
- Decomposition measurements:
  - TS_DD: tensile-strength loss per degree-day, using temperature-adjusted degree-days.
  - TS_D: tensile-strength loss per day.
  - TS_DD_SD: standard deviation of TS_DD across replicates.
  - Notes: some assays (E9, E10, F11) were lost during incubation.
- Molecular data (ITS and cbhI):
  - ITS: CTAB DNA extraction, qPCR targeting ITS2; copy number per cm² of cotton strip.
  - cbhI: qPCR for cellulose-degrading cbhI gene; copy number per cm².
  - sapro, asco, tetra: PCR/NGS-based estimates of relative abundance of saprotrophs, Ascomycota, and Tetracladium; analysis via Illumina MiSeq, quality control, OTU classification (RDP/UNITE), and trophic guild assignment (FUNGuild).

## Data processing, standards, and provenance
- Degree-day calculations: used to normalize decomposition data across sites with temperature variation.
- Sequencing and annotation workflow:
  - Illumina MiSeq for fungal community profiling.
  - OTU assignment via RDP classifier; UNITE database; trophic-mode annotation via FUNGuild.
- Referenced protocols and literature are provided (cellulose-decomposition cotton-strip protocol, DNA/RNA extraction methods, and qPCR/NGS analysis pipelines).

## Data quality, gaps, and limitations
- Temperature data gaps: certain sites (E9, E10, F11) lacked temperature records due to instrument error.
- Incubation outcomes: a subset of assays were lost during incubation (noted per-site).
- Metadata and units are clearly specified to support reproducibility, but some sites have incomplete ancillary measurements.

## Data governance, discoverability, and usability
- Data are organized with explicit variable definitions and units to support cross-site comparisons and meta-analyses.
- Site coordinates enable spatial analyses and integration with glacier-cover data.
- Provenance traces back to field collection, lab processing, and sequencing/analysis steps, with cited standard methods and references.
- Clear data description supports discoverability and reuse for researchers studying data integration, environmental microbiology, and decomposition ecology.

## Practical implications for Data Leaders
- Data strategy alignment:
  - The dataset exemplifies multi-modal data integration (physical environment, process measurements, and molecular ecology) requiring coherent metadata and data lineage.
- Data quality management:
  - Track and document missing data (e.g., temp gaps) and incident losses (assays lost) to maintain transparency for downstream analyses.
- Data standards and interoperability:
  - Maintain consistent units, naming conventions, and data formats (Table 2 definitions) to enable reproducibility across future studies.
- Metadata, provenance, and governance:
  - Preserve protocols, instrument details, and processing pipelines; reference external protocols and repositories to facilitate reuse.
- User needs and collaboration:
  - Data products support cross-disciplinary use (ecology, biogeochemistry, microbiology) and can inform assessments of data availability, gaps, and harmonization across networks of partners.
- Actionable improvements:
  - Address data gaps (temperature coverage) and standardize site-level metadata to improve discoverability and reliability for future data integration and system-wide data products.