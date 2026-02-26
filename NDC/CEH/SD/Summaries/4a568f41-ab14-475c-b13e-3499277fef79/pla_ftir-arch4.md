# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ).

## Overview
- Presents a dataset on the isothermal crystallisation of PLA.
- Uses FTIR spectroscopy to monitor crystallisation at various temperatures, from melt to fully formed film.
- Employs ATR-FTIR with a diamond crystal.

## Dataset content
- Data type: FTIR spectra collected as CSV files.
- Instrumentation: ATR-FTIR (diamond crystal) with a Thermo Nicolet iS5 spectrometer.
- Spectral data: wavelength range 600 to 4000 cm⁻¹; average of 16 spectra per timestamp.
- Time points: spectra recorded at specific crystallisation times, with data organized into tables by timestamp and polymer chemistry.
- File format: CSV with two columns—A: wavelength (cm⁻¹), B: absorbance (a.u.).
- Naming conventions: files named as PLA T=<temperature>C t=<time>min (e.g., PLA T=110C t=72min); a trailing 1 indicates baseline correction applied.
- Baseline correction: applied to files with a trailing 1, using airPLS.

## Data structure and metadata
- Lacks explicit column headers in the uploaded files; describes variables as wavelength and absorbance (Table 1).
- Data spans April–October 2023.
- Data organized by timestamp and polymer chemistry; includes notes on baseline-corrected versions.

## Data collection and processing
- Experimental setup: samples melted between Kapton sheets, moulded, then cooled in liquid nitrogen and equilibrated at the target temperature on the FTIR stage.
- Acquisition: spectra collected every 1 minute and saved as CSV files.
- Baseline correction: performed with the airPLS algorithm via Python scripts.

## Calibration, QA and reproducibility
- Instrument calibration: per manufacturer protocol using a polystyrene standard.
- Experimental consistency: identical sample preparation, quantities, pressure, temperature, and timing across measurements; stopwatch used to coordinate melting, removal, and crystallisation events.

## Tools, formats and access
- Data formats: CSV files with two columns (wavelength and absorbance); filenames encode temperature and time; baseline-corrected files end with a trailing 1.
- Software and processing: OMNIC software for data collection; Python scripts for baseline correction.
- Reference for baseline correction method: Zhang ZM et al., 2010.

## Instrumentation and settings
- Spectrometer: Thermo Nicolet iS5.
- Stage: Specac Golden Gate heated stage.
- Software: OMNIC.

## Reproducibility and quality control
- Standardized preparation protocol and measurement procedure to ensure comparability across samples and times.
- Clear documentation of naming and baseline correction to support traceability.

## Relevance for Data Leaders
- Demonstrates end-to-end data handling: experimental design, data capture, processing, and metadata considerations.
- Highlights practical data governance needs:
  - Metadata gaps: lack of explicit column names in CSV files; recommendation to embed descriptive headers and metadata.
  - Metadata enrichment: include variables like temperature, time, baseline correction flag, and spectral range in a metadata record.
  - File naming conventions are explicit but could be complemented with embedded metadata to ease discovery and interoperability.
  - Baseline correction is tracked via filename; consider capturing as metadata rather than file-name convention for better data discovery.
- Potential for reuse across similar polymer crystallisation studies and for linking to broader data systems or data-sharing networks, once metadata is standardized and documented.