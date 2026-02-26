# The Fourier Transform Infrared Spectroscopy (FTIR) spectra of poly(hydroxybutyrate)-based systems   with   clay   additives   changing   crystallisation   kinetics   recorded   at ambient temperature

## Aim and scope
- Provides additional information to a dataset on PHB-based systems with additives recorded by FTIR at ambient temperature.
- Aims to explore crystallite formation within the polymer matrix from melt to fully formed film.

## Data content and structure
- FTIR spectra of Poly(hydroxybutyrate) (PHB) with two clay fillers (Cloisite 25A, C25A, and Cloisite 10A, C10A) at various crystallisation times.
- Technique: Attenuated Total Reflectance (ATR-FTIR) with a diamond crystal.
- Wavelength range: 600–4000 cm^-1 with spectral resolution of 4 cm^-1.
- Data format: CSV files with two columns (A: wavelength cm^-1, B: absorbance a.u.). In uploaded data, no column names are present; data described as in Table 1.
- Each time stamp’s data represent an average of 16 FTIR spectra per measurement (OMNIC software).

## File naming and organization
- Naming convention examples: % additive, PHB, sample number, position number, e.g. 5pc_Clay_10A_PHB_s1_p3.
- Data organized per sample/condition and crystallisation time.

## Experimental design and materials
- Additives: two clays (C25A and C10A) chosen as non-hazardous, naturally occurring materials.
- PHB systems studied across 0–5 wt% additive concentration to assess impact on crystallisation.
- Temperature conditions: below PHB melting to establish temperature–crystallisation relationships.
- Objective: understand how filler chemistry modulates crystallisation kinetics in PHB.

## Sample preparation and data collection
- Sample preparation: PHB melted between kapton sheets, pressed in a mould, then quenched in liquid nitrogen; measured at ambient FTIR stage.
- FTIR data acquisition: spectra collected at multiple positions within the sample and saved as CSV files.
- Data processing: baseline correction performed using airPLS (adaptive iteratively reweighted penalized least squares) with Python scripts.

## Instrumentation, calibration, and quality control
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; OMNIC software.
- Calibration: polystyrene standard used for calibration as per manufacturer protocol.
- Quality control: uniform sample preparation protocol, consistent melting/removal timing via stopwatch, identical powder量, pressure, and temperature for each measurement.

## Temporal coverage
- Data collected from May to October 2021.

## Data processing and reproducibility
- Baseline correction applied to spectra using airPLS (Zhang et al., 2010) implemented in Python.
- Data files reflect multiple crystallisation times and positions to capture the crystallisation process from melt to film.

## Reference
- Zhang, Zhi-Min; Chen, Shan; Liang, Yi-Zeng. Baseline correction using adaptive iteratively reweighted penalized least squares, Analyst, 2010, 135(5), 1138-1146. The Royal Society of Chemistry. doi: 10.1039/B922045C