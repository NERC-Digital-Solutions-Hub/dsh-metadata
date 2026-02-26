# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems   with   clay   additives   changing   crystallisation   kinetics   recorded   at   ambient temperature

## Overview
- Provides FTIR spectra of Poly(hydroxybutyrate) (PHB) with two clay additives (Cloisite 25A and 10A) at ambient temperature to study crystallisation kinetics from melt to fully formed film.
- Aims to understand how filler chemistry influences PHB crystallisation and mechanical property modulation.

## Data Contents and Structure
- File format: CSV (.csv)
- Columns: two columns per file
  - Column A: wavelength (cm^-1)
  - Column B: absorbance (a.u.)
- Metadata and headers: files contain no column names; description of variables provided in Table 1.
- Data per time stamp: table results from averaging 16 FTIR spectra per measurement (via OMNIC software)
- Spectral range and resolution: 600–4000 cm^-1 at 4 cm^-1 resolution
- Naming convention: % additive, PHB, sample number, position number (example: 5pc_Clay_10A_PHB_s1_p3)
- Temporal coverage: May–October 2021
- Data aggregation: spectra averaged to single time-stamped table for each measurement

## Data Collection and Processing
- Instrumentation: Thermo Nicolet iS5 FTIR with Specac Golden Gate heated stage; ATR-FTIR using a diamond crystal; data processed with OMNIC.
- Sample preparation: melt between kapton sheets using an aluminium oval mould; quench in liquid nitrogen; equilibrate at ambient temperature; measured at multiple positions within the sample.
- Calibration: standard protocol using polystyrene; baseline correction performed with airPLS (Zhang et al., 2010) via Python scripts.
- Data processing: baseline correction applied to each measurement; spectra collected at various crystallisation times and sample positions.

## Experimental Design and Scope
- Additives studied: two clays, Cloisite 25A (C25A) and Cloisite 10A (C10A)
- Concentrations: 0–5 wt% additive
- Objective: assess impact of filler chemistry on PHB crystallisation at temperatures below the polymer melting point

## Quality Assurance and Governance
- Standardized sample preparation protocol across all measurements
- Consistent material amounts, pressure, and temperature maintained
- Timing controlled with a stopwatch for melting, sampling, and crystallisation measurements
- Calibration and data processing follow manufacturer guidelines and published methods

## Documentation and References
- Baseline correction method: adaptive iteratively reweighted penalized least squares (airPLS) – Zhang, Z.-M.; Chen, S.; Liang, Y.-Z., Analyst, 2010
- DOI: 10.1039/B922045C

## Data Stewardship Notes
- Metadata enrichment recommended for discoverability: include exact additive identity, concentration, sample IDs, crystallisation times, and measurement positions
- Consider adding explicit column headers or accompanying metadata files to mitigate the current lack of named columns
- Temporal and methodological details (instrument, calibration, processing) should be captured in dataset documentation to support reuse and interoperability