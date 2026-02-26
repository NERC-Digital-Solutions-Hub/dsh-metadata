# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview
- Describes a dataset of FTIR (ATR-FTIR) spectra for Poly(hydroxybutyrate-co-valerate) (PHBV) with varying hydroxyvalerate (HV) contents, recorded during isothermal crystallisation at different temperatures.
- Aims to explore crystallite formation within the PHBV polymer matrix as it transitions from melt to fully formed film.
- Data support for evaluating crystallinity evolution and crystallisation kinetics.

## Data content and format
- Data saved as .csv files with two columns and no column names:
  - Column A: Wavelength (cm-1)
  - Column B: Absorbance (a.u.)
- Spectra are averaged from 16 FTIR scans per measurement and cover the spectral range 600–4000 cm-1 with a resolution of 4 cm-1.
- Temporal sequence: spectra collected at successive crystallisation times (every 1–1.5 minutes).

## Sample conditions
- HV contents investigated: 0% HV (PHB) and 7%, 12%, 21% HV in PHBV.
- Purpose: to capture a wide range of thermal properties and crystallisation behaviours.
- Crystallisation performed at temperatures below the melting temperature.

## File naming and metadata
- Naming convention: %HVcontent, temperature, time from the beginning of the measurement (examples provided in the text). 
  - e.g., a PHB sample corresponds to 0% HV; other files indicate HV content, temperature, and elapsed time.
- Suffixes:
  - _1 at end of file indicates baseline correction was applied to the corresponding file without the 1.
  - _p2, _p3, _p4 indicate different positions on the sample after the measurement to record uniformity.
- Baseline-corrected files may include a trailing _1.

## Experimental setup and data collection
- Instrumentation: ATR-FTIR spectroscopy using a Thermo Nicolet iS5 spectrometer with a Specac Golden Gate heated stage.
- Sample preparation: polymer melts pressed between two kapton sheets using an aluminium oval mould; cooled rapidly in liquid nitrogen before measurement.
- Data collection: spectra collected at various positions on the sample, every ~1–1.5 minutes during crystallisation.

## Data processing and quality control
- Baseline correction performed using the airPLS algorithm (Zhang et al., 2010) via Python scripts.
- Calibration performed per manufacturer standard using a polystyrene standard.
- Consistent sample preparation protocol: identical powder amounts, pressure, and temperature across measurements.
- Quality control ensured via standardized timing (melting, removal, crystallisation records).

## Data analysis approaches
- Crystallinity index can be calculated from FTIR data using multiple methods:
  - Ratio of crystalline 1227 cm-1 to amorphous 1180 cm-1 (Kann et al., 2014)
  - Ratio of reference band 1380 cm-1 to amorphous band 1186 cm-1 (Middleton et al., 2001)
  - Ratio of crystalline 1230 cm-1 to reference 1453 cm-1 (Xu et al., 2002)
- Data supports tracking crystallisation kinetics and temperature–crystallisation correlations across HV contents.

## Temporal coverage and scope
- Data collected from May to October 2021 at the University of Strathclyde.

## Instrumentation and calibration details
- Instrument: Thermo Nicolet iS5 spectrometer with Specac heated stage; OMNIC software used for data handling.
- Calibration: manufacturer-standard calibration with polystyrene; consistent workflow across all measurements.

## References
- Kann, Y. et al., Polymer Testing, 2014.
- Middleton, A.C. et al., J. Appl. Polym. Sci., 2001.
- Xu, Jun et al., Polymer, 2002.
- Zhang, Z.-M. et al., Analyst, 2010 (airPLS baseline correction).