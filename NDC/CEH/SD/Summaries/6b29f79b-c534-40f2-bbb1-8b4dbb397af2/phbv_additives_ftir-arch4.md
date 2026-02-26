The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems   with   clay   additives   changing   crystallisation   kinetics   recorded   at   ambient temperature

## Overview
- Describes a dataset of PHB-based systems with clay additives (Cloisite 25A and 10A) studied to understand how filler chemistry affects crystallisation.
- Focuses on FTIR (ATR-FTIR) spectra collected at multiple crystallisation times to explore crystallite formation from melt to fully formed film.

## Dataset Description
- Data type: FTIR spectra of PHB with two clay fillers at various crystallisation times.
- Purpose: Investigate the influence of filler chemistry on PHB crystallisation.
- Scope: Data collected for samples with 0–5 wt% additive concentration across a range of sub-melting temperatures.

## Data Collection and Processing
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; OMNIC software.
- Sample preparation: Melt PHB between two Kapton sheets, cast in aluminium mould, then rapidly cooled in liquid nitrogen; spectra collected at ambient temperature.
- Spectral details: ATR-FTIR, diamond crystal; 600–4000 cm−1; spectral resolution 4 cm−1.
- Processing: Baseline correction using airPLS (Zhang et al., 2010) via Python scripts.
- Temporal scope: May–October 2021.

## Experimental Design
- Additives: Cloisite 25A (C25A) and Cloisite 10A (C10A).
- Concentrations: 0–5 wt% additive.
- Conditions: Studied at temperatures below PHB melting to establish temperature-crystallisation correlations.
- Replication: Each measurement aggregates data from multiple spectral acquisitions (average of 16 spectra per measurement).

## File Format and Naming
- File format: CSV.
- Data columns: Column A = wavelength (cm−1); Column B = absorbance (a.u.). No column headers in uploaded files.
- Naming convention: % additive, PHB, sample number, position number (e.g., 5pc_Clay_10A_PHB_s1_p3).

## Data Quality and Documentation
- Calibration: Instrument calibrated using standard polystyrene protocol per manufacturer guidelines.
- Consistency: Identical preparation protocol for all samples; timing, pressure, and temperature standardized with a stopwatch.
- Metadata: Descriptions aligned with Table 1 (wavelength and absorbance; no explicit column names in data files).

## Access, Reuse, and References
- Reusability: Data supports analysis of crystallisation kinetics and filler effects in PHB systems; baseline-corrected spectra suitable for comparative studies.
- Reference material: Baseline correction method (airPLS) cited (Zhang et al., Analyst, 2010); methodological details available via the cited publication.

## Data Governance and Stewardship Considerations for Data Leaders
- Discoverability: Data stored as CSVs with descriptive naming; consider adding explicit metadata to improve findability and interoperability.
- Metadata and standards: Current files lack column headers; advisable to adopt a formal metadata schema (variables, units, measurement conditions, sample identifiers).
- Data accessibility: Ensure clear licensing and access terms; document data provenance and processing steps for reproducibility.
- Versioning and updates: Establish version control and update log as new measurements or additives are added.
- Collaboration: Align dataset with broader polymer crystallisation data to facilitate cross-study synthesis; share naming conventions and processing scripts to promote reuse across networks.