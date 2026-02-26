# This document provides additional information about a dataset concerning the isothermal crystallisation of poly(lactic acid) (PLA ). The data was collected using Fourier Transform Infrared Spectroscopy (FTIR) at various crystallisation temperatures. It includes FTIR spectra of PLA taken at different time intervals to explore the formation of crystallites within the polymer matrix, ranging from the melt state to a fully formed film.

## Overview
- Dataset investigates PLA crystallisation under isothermal conditions using ATR-FTIR with a diamond crystal.
- Captures the progression from molten material to crystallised film by recording spectra at multiple time points across a range of crystallisation temperatures.

## Data content and structure
- Each table corresponds to a specific timestamp and polymer chemistry context; tables represent the average of 16 FTIR spectra per condition.
- Spectra cover a wavelength range of 600 to 4000 cm⁻¹ with a spectral resolution of 4 cm⁻¹.
- File content is organized into CSV files with two columns:
  - Column A: Wavelength (cm⁻¹)
  - Column B: Absorbance (a.u.)
- The uploaded data lacks column names; only the data values are present.

## File format, naming conventions, and metadata
- File format: .csv
- Naming convention: PLA T=<temperature>C t=<time>min (e.g., PLA T=110C t=72min)
- Baseline correction indicator: If a file ends with 1, it indicates baseline correction has been applied to the file without the trailing 1.
- Table 1 describes variables: Wavelength (cm⁻¹) and Absorbance (a.u.).

## Data collection method and instrumentation
- Instrumentation: Thermo Nicolet iS5 spectrometer with Specac Golden Gate heated stage and OMNIC software.
- Sample preparation: PLA melted between two Kapton sheets using an aluminium oval mould; after melting, samples were immersed in liquid nitrogen and measured at the FTIR stage, equilibrated at the target temperature.
- Data acquisition: FTIR spectra collected every 1 minute and saved as CSV files.

## Data processing and quality control
- Baseline correction: Applied using the airPLS algorithm via Python scripts.
- Calibration: Per manufacturer protocol using a polystyrene standard.
- Quality control: Consistent preparation protocol across samples; standardized amounts of powder, pressure, and temperature; stopwatch used to time melting, removal, and crystallisation steps to ensure comparability.

## Experimental design and scope
- Temperature range: Isothermal crystallisation conducted at temperatures below PLA’s melting point to establish a temperature–crystallisation relationship.
- Temporal coverage: Data collected from April to October 2023.
- Purpose: Support analysis of crystallisation kinetics and development of crystallites by comparing spectra over time and temperature.

## Data usage and considerations for data products
- Suitable for building self-serve data products (e.g., dashboards) that track spectral changes over time and temperature to infer crystallinity progression.
- Considerations:
  - Data has no column headers; parsing must rely on the two-column structure and domain knowledge.
  - Baseline-corrected files are identifiable by a trailing “1” in the filename; ensure correct pairing with uncorrected versions if needed.
  - Absorbance units are arbitrary (a.u.); cross-file normalization may be required for comparative analytics.
  - Wavelength alignment should be verified across files for consistent comparative analysis.

## Reference
- Zhang ZM, Chen S, Liang YZ. Baseline correction using adaptive iteratively reweighted penalized least squares. Analyst. 2010 May;135(5):1138-46. doi: 10.1039/b922045c. Epub 2010 Feb 19. PMID: 20419267.