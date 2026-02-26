# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems   with   clay   additives   changing   crystallisation   kinetics   recorded   at   ambient temperature

## Overview
- A dataset describing PHB-based systems with clay additives studied by ATR-FTIR at ambient temperature to explore crystallite formation from melt to fully formed film.
- Focus on how filler chemistry (two clays: Cloisite 25A and Cloisite 10A) influences PHB crystallisation.

## Data and Methods
- Data type: FTIR spectra collected as CSV tables, with two columns: wavelength (cm-1) and absorbance (a.u.). Each table corresponds to a given time point and polymer chemistry.
- Spectral range: 600–4000 cm-1; spectral resolution: 4 cm-1.
- Averaging: Each measurement is the average of 16 FTIR spectra.
- Data processing: Baseline correction performed using the airPLS algorithm implemented in Python.
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage and OMNIC software.
- Sample preparation: Melting the PHB powder between two Kapton sheets in an aluminium oval mold, then cooling in liquid nitrogen and placing on the FTIR stage at ambient temperature. Measurements taken at various positions on the sample.

## Experimental Design and Samples
- Additives: Cloisite 25A (C25A) and Cloisite 10A (C10A).
- Concentrations: 0–5 wt% additive in PHB.
- Objective: Investigate how small changes in clay chemistry affect polymer crystallisation and the temperature-crystallisation relationship.

## Data Format and Naming
- File format: CSV.
- File content: Table with two columns (Wavelength, Absorbance) and no column names in the data files.
- Naming convention example: % additive, PHB, sample number, position number, e.g. 5pc_Clay_10A_PHB_s1_p3.

## Calibration and Quality Control
- Instrument calibration: Per manufacturer protocol using a polystyrene standard.
- Quality control: Consistent sample preparation protocol, identical amounts of powder, pressure, and temperature; use of a stopwatch to standardise melting, removal, and crystallisation timing.

## Temporal Coverage
- Data collected from May to October 2021.

## Processing and Reference
- Baseline correction reference: Zhang, Zhi-Min; Chen, Shan; Liang, Yi-Zeng. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst, 2010, 135(5), 1138-1146.

## Relevance for Environmental Analysts
- Standardized, time-resolved FTIR data on PHB crystallisation with fillers supports assessment of material performance and environmental compatibility in packaging.
- Clear documentation of data collection, processing, and file standards facilitates data sharing, integration with other datasets, and reuse for monitoring environmental health and policy performance related to biodegradable polymers.