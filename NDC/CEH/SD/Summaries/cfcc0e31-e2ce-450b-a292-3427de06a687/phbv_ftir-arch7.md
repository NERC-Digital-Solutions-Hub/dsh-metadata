# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview for GIS Specialists
- A data resource describing how crystallization of PHBV-based polymers occurs over time at different temperatures and HV contents (0, 7, 12, 21% mol).
- Aimed at understanding spatially-resolved crystallite formation within a polymer film, with measurements taken at multiple positions on each sample.
- PHBV is highlighted as a biodegradable polymer with potential packaging applications; data could support life-cycle or material property mapping in a broader GIS-enabled decision workflow.

## Data Content and Structure
- Spectral data type: Attenuated Total Reflectance FTIR (ATR-FTIR) spectra collected with a diamond crystal.
- Data representation: CSV files, two columns per file (Wavelength in cm^-1, Absorbance in absorbance units). No explicit column headers.
- Per-measurement summary: spectra are averages of 16 individual FTIR spectra, collected at a given crystallisation time and polymer chemistry.
- Wavelength range: 600 to 4000 cm^-1 with a spectral resolution of 4 cm^-1.
- Derived measures: crystallinity index can be calculated using established peak/ratio methods (e.g., 1227/1180, 1380/1186, or 1230/1453).

## File Format, Naming, and Metadata
- File format: .csv
- Naming convention encodes:
  - HV content (PHB zero HV or PHBV with various HV percentages)
  - Temperature of crystallisation
  - Time from the start of the measurement
  - Sample position on the film (p2, p3, p4 indicate different positions)
  - Optional trailing “_1” indicates baseline correction has been applied
- Important metadata cues embedded in filenames to enable multi-factor analysis across HV content, temperature, time, and spatial position.

## Data Collection Methods
- Equipment and setup:
  - FTIR spectrometer (Thermo Nicolet iS5) with Specac Golden Gate heated stage.
  - Sample preparation involved melting between two Kapton sheets, solidifying in a mould, then quenching in liquid nitrogen before analysis.
- Measurement protocol:
  - Spectra collected every 1 to 1.5 minutes from multiple positions on each sample.
  - Baseline correction performed using the airPLS algorithm (Zhang et al., 2010) via Python scripts.
- Calibration:
  - Instrument calibrated per manufacturer guidelines using a polystyrene standard.
- Data processing:
  - Baseline-corrected files are indicated by the filename suffix.
  - Crystallinity indices can be computed from specific peak ratios described in the referenced literature.

## Temporal and Spatial Coverage
- Temporal coverage: May to October 2021.
- Time resolution: measurements taken at minute-level intervals during isothermal crystallisation.
- Temperature coverage: multiple crystallisation temperatures below the melting point (exact temperatures not listed here).
- HV contents studied: 0% (PHB), 7%, 12%, and 21% mol HV.
- Spatial coverage: measurements taken at multiple designated positions on each sample (_p2, _p3, _p4) to assess uniformity.

## Data Quality and Provenance
- Consistent sample preparation protocol across experiments.
- Uniform measurement timing and positioning within each experiment.
- Baseline correction documented and identifiable via filename convention.
- Data presented as tables without headers; explicit variables described in accompanying notes (Wavelength and Absorbance).

## GIS-Relevant Opportunities and Considerations
- Data modeling:
  - Transform CSVs into a tidy, georeferenced-like dataset with fields: HV_content, crystallisation_temp, time_from_start, sample_position, wavelength, absorbance, baseline_corrected (bool), crystallinity_index (derived).
- Visualization possibilities:
  - Time-series maps/plots of crystallinity index across the sample surface (positions p2/p3/p4) and as a function of HV content and temperature.
  - Heatmaps showing spatial variation of absorbance at key wavelengths linked to crystalline vs amorphous phases.
  - Multidimensional faceted visualizations: HV content × temperature × time × position.
- Integration potential:
  - Combine with other material-property GIS layers (e.g., biodegradability, mechanical properties) to support packaging development or material selection workflows.
- Data preparation guidance:
  - Create a standardized schema with explicit headers for Wavelength, Absorbance, HV_content, Temperature, Time, Position, BaselineCorrected, and optional CrystallinityIndex.
  - Document units and reference wavelengths for crystallinity ratios to enable reproducible geospatial analyses.

## References and Methods Notes
- Crystallinity assessment methods cited (Kann et al. 2014; Middleton et al. 2001; Xu et al. 2002) for calculating crystallinity indices from FTIR peaks.
- Baseline correction method: adaptive iteratively reweighted penalized least squares (airPLS), as described by Zhang et al. (2010).
- Sample content and naming conventions described for interpreting HV content, temperature, time, and spatial positions.

## Key Variables and Units
- Wavelength (cm^-1)
- Absorbance (arbitrary units)
- Time from start (minutes)
- Temperature (°C) used during crystallisation
- HV content (mol%)
- Sample position identifiers (_p2, _p3, _p4)