# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ). The data was collected using Fourier Transform Infrared Spectroscopy (FTIR) at various crystallisation temperatures.

## Overview
- Dataset on isothermal crystallisation of PLA, using ATR-FTIR spectra to monitor crystallite formation from melt to film.
- PLA chosen for its renewable-resource basis and potential for compostable products.

## Data structure and organization
- Data organized into tables corresponding to each timestamp and polymer chemistry.
- Each table represents the average of 16 FTIR spectra.
- Wavelength range: 600 to 4000 cm⁻¹.
- Spectral resolution: 4 cm⁻¹.
- Time-resolved data collected every 1 minute during crystallisation.

## Data format and naming conventions
- File format: CSV.
- Two columns: A = wavelength (cm⁻¹), B = absorbance (a.u.).
- Naming convention example: "PLA T=110C t=72min".
- If a file ends with "1", baseline correction was applied to the corresponding non-1 file.

## Data values and metadata
- Data lacks column names in the uploaded CSVs; files contain only data values.
- Table 1 provides variables: Wavelength (cm⁻¹) and Absorbance (a.u.).

## Collection, processing, and experimental design
- Instrumentation: FTIR spectrometer (Thermo Nicolet iS5) with Specac Golden Gate heated stage.
- Sample preparation: PLA melted between Kapton sheets in an aluminium oval mould; cooled rapidly in liquid nitrogen before FTIR stage; equilibrated at target temperature.
- Spectra collection: every 1 minute; saved as CSV files.
- Baseline correction: airPLS algorithm applied in Python scripts.

## Calibration and quality control
- Instrument calibration: standard protocol using polystyrene standard.
- Quality control: identical preparation protocol for all samples; consistent amounts, pressure, and temperature; timing tracked with a stopwatch.

## Temporal coverage and sampling
- Data collection window: April to October 2023.
- Temperature range: below PLA melting temperature; designed to establish temperature–crystallisation relationships.

## Instrumentation and processing details
- Instrument: Thermo Nicolet iS5 with Specac Golden Gate heated stage; OMNIC software for data handling.
- Baseline correction reference: Zhang ZM et al. (2010) on adaptive iteratively reweighted penalized least squares (airPLS).

## Relevance to GIS Specialists (data governance and visualization considerations)
- Illustrates rigorous metadata, data provenance, and QA practices that support reproducible data products.
- Demonstrates handling time-series spectral data, with clear naming, versioning (baseline-corrected vs non-corrected), and processing steps that aid traceability in map-based or dashboard visualizations.
- Though not geospatial, the dataset highlights how to document data collection context, instrumentation, calibration, and processing—principles transferable to geospatial data workflows (standards, metadata, QA, and reproducibility).

## References
- Zhang ZM, Chen S, Liang YZ. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst. 2010 May;135(5):1138-46. doi: 10.1039/b922045c.