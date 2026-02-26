# Isothermal crystallisation of PHBV-based systems recorded using Fourier transform infrared spectroscopy (FTIR) at various crystallisation temperatures

## Overview
- Biodegradable PHBV polymer system studied to understand crystallite formation from melt to fully formed film.
- Focuses on how hydroxyvalerate (HV) content affects crystallisation at different temperatures.
- Data derived from ATR-FTIR spectroscopy with a diamond crystal, averaged from multiple spectra per measurement.

## Data content and structure
- Contains FTIR spectra for PHBV with varying HV content (0%, 7%, 12%, 21% mol) at multiple crystallisation times.
- Spectra are saved as CSV files, each file representing a time stamp and polymer chemistry.
- Each CSV has two columns: wavelength (cm⁻¹) and absorbance (arbitrary units). No column headers.
- Data represent averages of 16 FTIR spectra per measurement (OMNIC software), 600–4000 cm⁻¹, 4 cm⁻¹ resolution.
- Temporal sampling: spectra collected every 1–1.5 minutes across several sample positions.
- Files include notes on baseline correction and sample position.

## File format and naming conventions
- File format: .csv
- Naming convention includes: HV content, temperature, time from measurement start, and sample position (e.g., 7p hv at tc_90 with t-1min).
- Indicators:
  - _1 at end of filename indicates baseline correction was applied.
  - phb indicates 0% HV samples; phbv indicates HV-containing samples.
  - _p2, _p3, _p4 denote different sample positions (uniformity checks).

## Experimental methods and processing
- Collection location and period: University of Strathclyde, May–October 2021.
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage; OMNIC software.
- Sample preparation: melt between kapton sheets, pressed in aluminium mould, then quenched in liquid nitrogen; measured at set temperatures.
- Data collection: spectra every 1–1.5 minutes at various sample positions.
- Baseline correction: airPLS algorithm (Zhang et al., 2010) applied in Python.
- Crystallinity indices (possible calculations from spectra): 
  - 1227/1180 cm⁻¹ (crystalline vs amorphous)
  - 1380/1186 cm⁻¹
  - 1230/1453 cm⁻¹
  These methods are described in cited literature (Kann et al., Middleton et al., Xu et al.).
- Calibration: polystyrene standard prior to measurements.

## Data content governance and provenance
- Data are organized by HV content, temperature, time, and sample position, enabling traceability of crystallisation conditions.
- Documentation notes the preparation protocol, measurement timing, and positions to support reproducibility.
- Baseline correction and spectral averaging steps are explicitly described to support reproducible preprocessing.

## Quality control and limitations
- Consistent sample preparation protocol across measurements; use of stopwatch to ensure timing consistency.
- Uniform spectral acquisition settings (range and resolution) and averaging procedure.
- Data files intentionally omit column headers; users must map columns to wavelength and absorbance.
- Baseline correction applied selectively (indicated by filename suffix).

## Temporal and access scope
- Temporal coverage: May–October 2021.
- Data format and naming designed to support discoverability and reuse in studies of crystallisation kinetics and PHBV material properties.

## Usage considerations
- Suitable for analyses of temperature-dependent crystallisation, HV-content effects, and crystallinity index comparisons.
- Requires parsing of CSVs without headers and interpretation of naming conventions to identify HV content, temperature, time, and position.
- Apply or reproduce baseline correction as described if reprocessing is needed.

## References for context
- Kann et al., 2014; Middleton et al., 2001; Xu et al., 2002; Zhang et al., 2010 (baseline correction method)