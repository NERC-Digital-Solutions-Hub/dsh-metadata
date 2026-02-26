# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ).

## Overview
- Describes a dataset on the isothermal crystallisation of PLA using FTIR spectroscopy to study crystallite formation from melt to film.
- Uses ATR-FTIR with a diamond crystal to capture spectra at multiple crystallisation temperatures and times.

## Data content
- FTIR spectra are organized into tables corresponding to each timestamp and polymer chemistry; each table is the average of 16 spectra.
- Data includes spectral measurements over 600–4000 cm⁻¹ at specific crystallisation times, with a spectral resolution of 4 cm⁻¹.
- File format: CSV with two columns (A: wavelength in cm⁻¹, B: absorbance in arbitrary units). Files lack explicit column names.

## File naming conventions
- Naming format: PLA T=<temperature>C t=<time>min (e.g., PLA T=110C t=72min).
- A trailing “1” indicates a file that has undergone baseline correction in a separate file without the trailing 1.

## Temporal and experimental scope
- Temporal coverage: April–October 2023.
- Sample preparation: PLA melted between two Kapton sheets in an aluminium oval mold, then cooled in liquid nitrogen before ATR-FTIR measurement.
- Data collected every 1 minute during crystallisation at set temperatures below the melting point.

## Methods and instruments
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; OMNIC software.
- Baseline correction: airPLS algorithm applied via Python scripts.
- Experimental design: PLA samples investigated across a range of sub-melting temperatures to establish temperature–crystallisation relationships.

## Calibration and quality control
- Calibration carried out using manufacturer-recommended protocol with a polystyrene standard.
- All samples prepared using identical protocol (same powder amount, pressure, temperature); timing recorded with a stopwatch to ensure consistency.

## Data structure and metadata considerations
- Data presented as a 2-column CSV per file; lacks explicit column names; Table 1 in the dataset describes variables (Wavelength, Absorbance).
- Baseline correction status is indicated by file naming (presence of trailing 1).

## Relevance to monitoring frameworks
- Provides a well-documented data generation workflow, including instrumentation, calibration, and QC steps, useful for data provenance and governance in monitoring frameworks.
- Highlights common barriers for reuse in monitoring contexts: metadata completeness, consistent naming, and explicit baseline treatment, all of which are partially addressed in the dataset description.
- Demonstrates need for clear metadata about experimental conditions (temperature, time, baseline correction) to support integration into broader environmental health monitoring datasets.

## Data provenance and governance notes
- Baseline correction method cited (airPLS) with a reference to the original methodology.
- Data organized and quality-controlled with standardized preparation and timing protocols, aiding traceability and reproducibility.

## Reference
- Zhang ZM, Chen S, Liang YZ. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst. 2010 May;135(5):1138-46. doi: 10.1039/b922045c. Epub 2010 Feb 19.