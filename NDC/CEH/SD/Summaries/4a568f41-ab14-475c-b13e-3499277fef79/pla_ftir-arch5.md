# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA )

## Dataset purpose and scope
- Dataset captures crystallisation behavior of PLA under isothermal conditions using FTIR spectroscopy.
- Aims to explore formation of crystallites from melt state to fully formed film across different crystallisation temperatures.
- Data type: FTIR spectra (ATR-FTIR with diamond crystal) collected at multiple time points.

## Data content and structure
- Data format: CSV files.
- Variables: two columns per file — wavelength (cm⁻¹) and absorbance (a.u.); files lack column headers.
- Each table corresponds to a timestamp and a specific polymer chemistry/experiment condition.
- Each data point is the average of 16 FTIR spectra, processed with baseline correction as described.
- File naming convention: PLA T=[temperature]C t=[time]min, with optional trailing 1 indicating baseline correction on the uncorrected file.
- Spectral range: 600–4000 cm⁻¹; spectral resolution: 4 cm⁻¹.

## Experimental design and collection methods
- Temperature range: isothermal crystallisation at temperatures below PLA’s melting point to establish temperature–crystallisation relationships.
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; OMNIC software used for processing.
- Sample preparation: PLA melted between two Kapton sheets, formed in an aluminium oval mould, then cooled (liquefied via liquid nitrogen) before FTIR measurement.
- Data collection cadence: spectra recorded every 1 minute; saved as CSV files.
- Calibration: instrument calibrated per manufacturer protocol using a polystyrene standard.

## Data processing and quality control
- Baseline correction: adaptive iteratively reweighted penalized least squares (airPLS) applied via Python scripts.
- Consistency: identical sample preparation protocol across all measurements (same powder amount, pressure, temperature).
- Quality control measures documented (timing, melting, crystallisation records) to ensure comparability.

## Metadata, documentation, and standards
- Table 1 describes variables (Wavelength, Absorbance) but files lack explicit column names.
- Record includes approach to baseline correction and the exact method used (airPLS) with citation.
- Reference for baseline correction method provided: Zhang et al. 2010.
- Temporal coverage: data collected April–October 2023.

## Instrumentation, calibration, and data provenance
- Instrument: Thermo Nicolet iS5 with heated stage; head geometry and OMNIC software specified.
- Calibration steps: manufacturer-recommended protocol using polystyrene standard.
- Provenance: data lineage preserved through explicit naming conventions and processing steps (baseline correction indicator).

## Implications for data sharing and reuse (Data Steward perspective)
- Discoverability: ensure metadata includes wavelength range, resolution, timestamp, temperature, and timepoint to enable search and filtering.
- Interoperability: consider adding explicit column headers (e.g., Wavelength_cm-1, Absorbance_a.u.) to CSVs; maintain consistent units.
- reproducibility: provide a readme with full description of naming convention, baseline correction flag, and Python scripts used for airPLS baseline correction.
- Data quality: maintain documentation of calibration, sample prep protocol, and measurement cadence to support validation and reuse.
- Accessibility: confirm whether CSVs are accompanied by the raw spectra files and any processed derivatives, and clarify licensing or data-use terms if available.

## Potential challenges and considerations
- Metadata completeness: some files lack column names, which may hinder automated ingestion.
- Format interoperability: CSV with two columns and no headers requires schema inference for reuse.
- Large datasets: time-series spectra across multiple temperatures may result in a high number of files; consider centralized metadata index for easier discovery.