# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems   with   clay   additives   changing   crystallisation   kinetics   recorded   at   ambient temperature

## Overview
- Datasets describing FTIR (ATR-FTIR) spectra of PHB-based systems with two clay additives (Cloisite 25A and Cloisite 10A) to study how filler chemistry affects crystallisation within the polymer matrix from melt to film at ambient temperature.
- Aims to explore crystallite formation and crystallisation kinetics under varying additive types and concentrations.

## Data content
- ATR-FTIR spectra collected at multiple crystallisation times for PHB with additives.
- Two additives studied: Cloisite 25A (C25A) and Cloisite 10A (C10A); additives investigated across 0–5 wt%.
- Spectra averaged from 16 individual FTIR measurements per time point using OMNIC software.
- Wavelength range: 600–4000 cm-1; spectral resolution: 4 cm-1.
- Data saved in CSV format, with two columns: Column A = wavelength (cm-1); Column B = absorbance (a.u.); no column headers in files.

## File naming and structure
- Naming convention example: % additive, PHB, sample number, position number (e.g., 5pc_Clay_10A_PHB_s1_p3).
- Each file corresponds to a specific time stamp and polymer chemistry, representing the averaged spectrum for that condition.

## Temporal coverage and conditions
- Data collection period: May–October 2021.
- Sample preparation: PHB melted between two kapton sheets, formed in an aluminium oval mould; rapid cooling in liquid nitrogen; spectra collected at ambient temperature.
- Measurements taken at multiple positions within each sample.

## Experimental design
- Two clay additives evaluated (C25A and C10A) to assess the impact of small chemistries on PHB crystallisation.
- Studied across various additive concentrations (0–5 wt%) and temperatures below PHB melting temperature to establish temperature-crystallisation correlations.

## Instrumentation and calibration
- Instrument: Thermo Nicolet iS5 FTIR spectrometer with Specac Golden Gate heated stage; data processed with OMNIC software.
- Calibration: Performed using standard polystyrene calibration procedure as recommended by the manufacturer.

## Data processing and quality control
- Baseline correction applied using the airPLS algorithm (Zhang et al., 2010) via Python scripts.
- All samples prepared with consistent protocol: identical powder amounts, pressure, and temperature; timing controlled with a stopwatch to ensure comparability.
- Data processing included generating CSV files with standardized formatting, enabling cross-comparison across times and additives.

## Data usage and interpretation
- Intended to support analysis of crystallite formation and crystallisation kinetics in PHB matrices with different clay fillers.
- Facilitates exploration of how additive chemistry influences structural evolution from melt to fully formed film.
- The dataset structure supports self-service analysis by end users via the included CSV files, with clear metadata on additives, concentrations, and experimental conditions.

## Variables and metadata
- Variables in the data files: 
  - Wavelength (cm-1)
  - Absorbance (a.u.)
- Additional methodological metadata:
  - Sample preparation details, additive types, concentrations, measurement times, and instrumentation settings.
  - Baseline correction method and reference for the approach.

## Reference
- Baseline correction method: Zhang, Zhi-Min; Chen, Shan; Liang, Yi-Zeng. Baseline correction using adaptive iteratively reweighted penalized least squares, Analyst, 2010, 135(5), 1138-1146. DOI: 10.1039/B922045C.