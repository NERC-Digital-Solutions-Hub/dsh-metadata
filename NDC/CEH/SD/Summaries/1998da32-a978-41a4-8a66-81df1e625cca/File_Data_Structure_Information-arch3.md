# Details of Data Structure

- 17 .dat files from electrical resistivity tomography (ERT) geophysical surveys conducted in the MAKUTAPORA basin, Tanzania, between 28/06/2019 and 16/07/2019.
- Data were generated from raw .stg files produced by an AGI SuperSting R8 (STING) resistivity meter and converted via a bespoke Python script; topographic data were added during conversion.
- Each .dat file includes a survey number (e.g., Survey_01) and a suffix (e.g., _NZ01) indicating location and survey sequence.

- Data format and organization
  - ASCII-delimited data: comma, blank space, or line feed/return separators.
  - Structured for use with the res2dinv program (provided by Geometrics).
  - Line 1: Name of the survey line.
  - Line 2: Electrode spacing.
  - Line 3: Array type (examples: Wenner=1, Pole-pole=2, Dipole-dipole=3, Pole-dipole=6, Schlumberger=7, Equatorial dipole-dipole=8, Non-conventional/general array=11). This dataset uses array 11.
  - Line 4: Sub-Array type (0 none/specific, 1 general).
  - Line 5: Header option for inverted data (apparent resistivity vs. direct resistance values).
  - Line 6: Indicator (1) to invert as resistance values.
  - Line 7: Number of data points.
  - Line 8: Type of x-location (0 if no topography; 1 or 2 if topography data present). Topographic data is present here (value 2).
  - Line 9: IP data flag (0 none, 1 present).

- Data points (in subsequent lines)
  - Each line corresponds to a specific electrode arrangement.
  - 10 columns per line; 4-electrode array results in 10 data columns.
  - Columns 1: Number of electrodes (4).
  - Columns 2–9: x and z locations of C1, C2, P1, P2 electrodes respectively.
  - Column 10: Resistance value (unit: ohm-metre, Ωm), corresponding to apparent resistivity measurements.

- Units and interpretation
  - Measured values in column 10 are in Ωm (apparent resistivity values for inversion or resistance values as indicated).
  - Data are intended for use with resistivity inversion (res2dinv) to derive subsurface resistivity models.

- Data provenance and supporting materials
  - The .dat files were produced from raw .stg files (STING) and augmented with topographic information via a custom Python script.
  - SupportingDocumentation.txt provides detailed methods used to collect/generate the data and quality control approaches.
  - Supp_Table_for_Survey.csv lists survey numbers and suffixes, coordinates (easting/northing of line endpoints), geometry (line length), and survey parameters (dipole size, max dipole, number of electrodes, electrode spacing).
  - A map of survey lines and a .kmz file are available in the associated paper.

- References and related resources
  - res2dinv manual (Data file operations and data format, page 11; Appendix L: Non-conventional or general arrays) for more detail on file structure and usage.
  - Associated paper contains the map, supplementary maps, and additional context for the dataset.
  - AGI STING equipment link for device specifications.

- Practical considerations for monitoring/framework use
  - Demonstrates a well-documented data structure with explicit line definitions, electrode geometry, and topographic inclusion, facilitating reproducibility and re-use in monitoring analyses.
  - Metadata and ancillary files (SupportingDocumentation.txt, Supp_Table_for_Survey.csv) support transparent data provenance and governance.
  - Potential reliance on custom scripts for data conversion and topographic augmentation; ensuring access to these scripts and versioning would support data quality and reuse.