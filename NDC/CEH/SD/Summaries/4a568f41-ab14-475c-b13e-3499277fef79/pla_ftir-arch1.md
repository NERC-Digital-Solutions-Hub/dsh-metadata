## This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ). The data was collected using Fourier Transform Infrared Spectroscopy (FTIR) at various crystallisation temperatures. It includes FTIR spectra of PLA taken at different time intervals to explore the formation of crystallites within the polymer matrix, ranging from the melt state to a fully formed film.

## Overview
- Dataset on isothermal crystallisation of PLA examined via FTIR.
- Focus on formation of crystallites as PLA transitions from melt to crystalline film.
- Data collected at multiple crystallisation temperatures below PLA's melting point.

## Data content and structure
- Measurement type: ATR-FTIR with a diamond crystal.
- Data aggregation: average of 16 FTIR spectra per timestamp/chemistry condition (via OMNIC software).
- Wavelength range: 600 to 4000 cm^-1.
- Spectral resolution: 4 cm^-1.
- Organization: tables corresponding to each timestamp and polymer chemistry.
- File structure: .csv files containing two columns (A: wavelength in cm^-1, B: absorbance in arbitrary units). Files lack column names.

## File naming conventions
- Example: "PLA T=110C t=72min".
- A trailing "1" indicates baseline correction applied to the corresponding file without the "1".

## Data recording, processing, and baseline treatment
- Baseline correction: performed using the airPLS algorithm (applied via Python scripts).
- Temporal sampling: spectra collected every 1 minute during crystallisation at each temperature.
- Data range and context: captures crystallisation at temperatures below the melting point.

## Experimental design and sampling
- Sample preparation: PLA melted between two Kapton sheets, pressed in an aluminium oval mould.
- Post-melting handling: cooled rapidly in liquid nitrogen before positioning on the FTIR stage.
- Temperature exposure: crystallisation performed at a range of temperatures below PLA’s melting temperature to establish temperature–crystallisation relationships.

## Instrumentation and calibration
- Instrument: Thermo Nicolet iS5 spectrometer.
- Attached equipment: Specac Golden Gate heated stage.
- Software: OMNIC.
- Calibration: standard polystyrene calibration per manufacturer protocol.

## Quality control and reproducibility
- Consistent sample preparation protocol for all measurements.
- Use of a stopwatch to standardise melting, removal, and crystallisation timing.
- Uniform sample amount, pressure, and temperature across measurements.
- All samples prepared following the same procedure to ensure comparability.

## Temporal coverage
- Data collection period: April to October 2023.

## Reference for baseline correction method
- Zhang ZM, Chen S, Liang YZ. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst. 2010;135(5):1138-46. DOI: 10.1039/b922045c.