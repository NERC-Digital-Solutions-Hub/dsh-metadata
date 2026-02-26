# Calibration of a sensor for mercury (II) ions using a Fluorimeter

## Overview
- Dataset collection showing calibration of a mercury (II) sensor using a fluorimeter with HgCl2 or HgNO3.
- Tests cover a range of sample conditions: sensor concentrations, water-to-methanol co-solvent ratios, and the role of acid for HgNO3 stability.
- Calibration is based on measuring luminescent response with excitation at 500 nm; a linear relation to Hg(II) concentration is used to determine unknown sample concentrations.
- Calibration graphs for raw fluorimeter data are included in a PowerPoint file.
- Real-sample testing includes dental clinical and amalgam samples using a 1 µM sensor across media (saliva, distilled water, amalgam separator supernatant).
- ICP-MS data are provided to validate the fluorescence-based calibration and to monitor soluble mercury in dental amalgam samples kept at 11°C or 37°C, in water and saliva; supernatants are filtered prior to ICP-MS measurement.

## Data content and structure
- Dataset files: raw fluorimeter measurements related to Hg(II) calibration under varying conditions.
- Calibration graphs: PowerPoint file containing the calibration curves derived from the fluorimeter data.
- Real-sample data: measurements for dental clinical and amalgam samples using a 1 µM sensor across different media.
- Validation data: ICP-MS measurements used to confirm fluorimeter-based calibration and track soluble mercury in dental amalgams under specified temperatures and media.
- Metadata: concentration settings for sensor, water/methanol ratios, acid conditions, sample media, and temperature conditions.

## Experimental variables and measurements
- Sensor concentration variations and solvent conditions (water to methanol ratios).
- Analyte forms: HgCl2 and HgNO3.
- Excitation wavelength: 500 nm; luminescent response corresponding to Hg(II) concentration.
- Media for real samples: saliva, distilled water, and amalgam separator supernatant.
- Additional temperature contexts for validation: 11°C and 37°C.
- Analytical method for validation: ICP-MS to corroborate calibration and assess soluble mercury content.

## Calibration and validation outcomes
- A linear relationship between luminescent response and Hg(II) concentration enables concentration estimation of unknown samples from fluorimeter data.
- Calibration graphs are provided to support the linear relationship in the datasets.
- ICP-MS data validate the fluorescence-based calibration and provide an independent measure of soluble mercury in dental amalgams under different media and temperatures.

## Data formats and accessibility
- Fluorimeter data (raw measurements) and associated calibration results are organized across dataset files.
- Calibration outcomes are summarized in a PowerPoint with embedded graphs.
- ICP-MS results accompany the fluorimeter data as a validation dataset.
- Real-sample measurements are linked to media conditions and sensor concentration used.

## GIS-Relevant considerations and integration
- The data are laboratory-scale measurements tied to specific experimental conditions; for GIS use, consider integrating with spatial or facility-level data if linking to sampling sites, clinics, or environmental monitoring locations.
- To create map-based data products, harmonize units, document metadata (sensor concentration, solvent ratio, acid conditions, media, temperature), and unify data across files (raw fluorimeter, calibration graphs, and ICP-MS results).
- Address multi-resolution data: calibration/validation data (lab-scale) versus real-sample measurements (potentially linked to locations or clinical settings).
- Ensure data standards and provenance are captured to enable reproducibility and cross-dataset comparisons.

## Potential limitations and considerations for GIS workflows
- Data are dispersed across multiple file types (raw data, presentation graphs, validation measurements), requiring careful data fusion and metadata curation.
- Variability in sample conditions (solvent composition, acid presence, media) may affect comparability; metadata should capture these factors explicitly.
- The document focuses on calibration and validation steps; spatial context (locations, deployment sites) would need to be added for mapping or regional analysis.