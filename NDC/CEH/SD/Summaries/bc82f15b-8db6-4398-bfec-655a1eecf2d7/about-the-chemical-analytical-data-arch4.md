# These dataset files show the calibration of a sensor for mercury (II) ions using a Fluorimeter and either HgCl2 or HgNO3

## Purpose and approach
- Calibrate a mercury(II) sensor by recording luminescent response with a fluorimeter (excitation at 500 nm) across varying Hg(II) concentrations.
- Use calibration to enable measurement of unknown samples.
- Validate calibration with complementary data and real-sample testing.

## Experimental design and datasets
- Tests conducted under multiple conditions:
  - Varied sensor concentrations.
  - Varied water to methanol co-solvent ratios to support probe solubility.
  - Assessment of acid effects, particularly nitric acid for HgNO3 stability.
- Dataset files encode experimental parameters in filenames (sensor concentration and water:methanol ratio).
- Calibration results are presented as linear relationships between luminescent response and Hg(II) concentration.
- Calibration graphs are provided in a PowerPoint file mapped to raw fluorimeter data.

## Real-sample testing and media
- Dental clinical and amalgam samples tested using a 1 μM sensor.
- Media tested: saliva, distilled water, and amalgam separator supernatant to observe measurable responses.

## Validation and monitoring with ICP-MS
- ICP-MS data accompany calibration to:
  - Validate sensor calibration.
  - Monitor soluble mercury content in dental amalgam samples.
- Sample conditions for ICP-MS evaluations:
  - Solutions held at 11°C or 37°C.
  - Analyses performed in water and saliva.
  - Supernatants filtered prior to ICP-MS measurement.

## Data management and interpretation
- Data types include fluorimetric calibration data, real-sample response data, and ICP-MS validation data.
- Metadata considerations evident from file naming conventions (sensor concentration, solvent ratios) and explicit mention of excitation wavelength and media.
- Framework supports cross-method validation (fluorimetry vs ICP-MS) and application to quantify unknown samples across different matrices.

## Practical implications for data leadership
- Data assets cover generation, calibration, validation, and real-sample testing, enabling traceability and reproducibility.
- Metadata clarity (concentrations, solvent ratios, temperatures, media) enhances discoverability and reuse.
- Cross-validation between analytical methods strengthens trust in sensor-based measurements and informs broader data strategy for sensor calibration programs.