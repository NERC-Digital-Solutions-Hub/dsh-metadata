Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview
- Describes a dataset of FTIR spectra for Poly(hydroxybutyrate-co-valerate) (PHBV) with varying hydroxyvalerate (HV) contents, recorded during isothermal crystallisation at different temperatures.
- Aims to explore crystallite formation within the polymer matrix from melt to fully formed film.
- Data intended to support understanding of crystallisation behaviour relevant to biodegradable packaging materials.

## Data Content and Format
- FTIR spectra collected via ATR-FTIR with a diamond crystal; spectra averaged from 16 scans per measurement.
- Wavelength range: 600–4000 cm−1; spectral resolution: 4 cm−1.
- Data stored as CSV files with two columns: wavelength (cm−1) and absorbance (a.u.); no column headers in the data tables.
- Each file corresponds to a specific HV content, temperature, time into the experiment, and sample position; file naming encodes these factors and whether baseline correction was applied.
- Baseline correction performed using the airPLS algorithm.

## Samples and Variables
- HV contents studied: 0% (PHB), 7%, 12%, and 21% HV.
- Experimental conditions span temperatures below the melting point to establish temperature–crystallisation relationships.
- Time resolution: spectra collected approximately every 1–1.5 minutes.
- Measurements taken at multiple sample positions to assess uniformity.

## Experimental Methods
- Sample preparation: polymer melted between two kapton sheets in an aluminium oval mold; cooled rapidly in liquid nitrogen; placed on a heated FTIR stage.
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; data processed with OMNIC software.
- Calibration: performed per manufacturer protocol using polystyrene standards.

## Data Processing and Quality Control
- Baseline correction applied to files using airPLS; baseline-corrected and uncorrected versions exist based on filename conventions.
- Crystallinity index can be estimated using published peak-ratio methods (examples provided):
  - 1227/1180 cm−1 (crystalline vs amorphous)
  - 1380/1186 cm−1
  - 1230/1453 cm−1
- Quality control ensured uniform sample preparation (same powder quantity, pressure, and temperature), with timing tracked via stopwatch.

## Temporal Coverage and Provenance
- Data collection period: May to October 2021.
- Location: University of Strathclyde, using FTIR spectrometer with a heated stage.

## Data Governance, Metadata, and Access
- Data is available as CSV files; table structure is described, though the files lack explicit column names.
- Metadata is embedded in file naming conventions, detailing HV content, temperature, time, and measurement position.
- Clear documentation of baseline correction and crystallinity calculation methods is provided to support reproducibility.
- References included for crystallinity analysis methods and baseline correction technique.

## Potential Uses for Monitoring Frameworks
- Provides a transparent, well-documented dataset suitable for validating materials monitoring metrics related to crystallisation in biodegradable polymers.
- Can inform policy-oriented assessments of material performance and environmental impact by linking processing conditions to material structure.
- Demonstrates data governance practices (metadata encoding, baseline corrections, reproducible processing) that support data sharing and quality assurance in environmental health monitoring contexts.

## References
- Kann et al. 2014; real-time FTIR studies and crystallinity analysis methods
- Middleton et al. 2001; ratio-based crystallinity indicators
- Xu et al. 2002; in situ FTIR crystallisation studies
- Zhang et al. 2010; airPLS baseline correction methodology