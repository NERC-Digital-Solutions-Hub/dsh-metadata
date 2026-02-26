# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ). The data was collected using Fourier Transform Infrared Spectroscopy (FTIR) at various crystallisation temperatures. It includes FTIR spectra of PLA taken at different time intervals to explore the formation of crystallites within the polymer matrix, ranging from the melt state to a fully formed film.

## Overview
- Describes a dataset on the isothermal crystallisation of poly(lactic acid) (PLA).
- Data collected with FTIR at various crystallisation temperatures to monitor crystallite formation from melt to film.

## Data contents and format
- Technique: Attenuated Total Reflectance FTIR (ATR-FTIR) with a diamond crystal.
- Organization: data in tables by timestamp and polymer chemistry; each table is the average of 16 FTIR spectra (measured via OMNIC software).
- Wavelength range: 600 to 4000 cm⁻¹.
- Spectral resolution: 4 cm⁻¹.
- File format: .csv with two columns (A: wavelength cm⁻¹, B: absorbance a.u.).
- Naming convention: PLA T=110C t=72min, etc.; a trailing 1 indicates baseline correction applied to the file without 1.

## Data structure and variables
- Table-like data structure described as Table 1; uploaded data lacks column names.
- Variables (as described): Wavelength (cm⁻¹), Absorbance (a.u.).

## Temporal coverage
- Data collected from April to October 2023.

## Methods and instrumentation
- Instrument: Thermo Nicolet iS5 FTIR spectrometer with Specac Golden Gate heated stage.
- Sample preparation: melt PLA between Kapton sheets in an aluminium oval mould; quench in liquid nitrogen; place on FTIR stage and equilibrate at target temperature.
- Data acquisition: spectra collected every 1 minute and saved as .csv files.
- Baseline correction: performed with airPLS algorithm via Python scripts.

## Calibration and quality control
- Calibration: standard manufacturer protocol using a polystyrene standard.
- Quality control: consistent sample preparation (same powder amount, pressure, and temperature); timing tracked with a stopwatch for melting, removal, and crystallisation.

## Experimental design
- PLA samples examined at temperatures below their melting point to establish the temperature–crystallisation relationship.

## Reference
- Zhang ZM, Chen S, Liang YZ. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst. 2010;135(5):1138-46. doi: 10.1039/b922045c.