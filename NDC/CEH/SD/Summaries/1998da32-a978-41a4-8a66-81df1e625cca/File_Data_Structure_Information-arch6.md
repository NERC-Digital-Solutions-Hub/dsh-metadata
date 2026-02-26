# Details of Data Structure

## Overview
- Dataset comprises 17 .dat files from electrical resistivity tomography (ERT) geophysical surveys.
- Collected in MAKUTAPORA basin, Tanzania, between 28/06/2019 and 16/07/2019.
- Data prepared for use with res2dinv inversion software; files include added topographic data and metadata.

## Data files and structure
- File format: ASCII-delimited (.dat) with comma, space, or line-ending separators.
- Designed to be read by res2dinv (Data file operations and format described in res2dinv manual).
- Each .dat file contains a survey line with the following line-based metadata:
  - Line 1: Survey line name
  - Line 2: Electrode spacing
  - Line 3: Array type (codes; only non-conventional/general arrays used: 11)
  - Line 4: Sub-Array type (0 = none specific, 1 = general)
  - Line 5: Inversion mode header (choose apparent resistivity or direct resistance)
  - Line 6: Indicator (1 to use resistance value)
  - Line 7: Number of data points
  - Line 8: Type of x-location (0 = none, 1 or 2 = topography present; 2 used here)
  - Line 9: IP data flag (0 = none, 1 = present)

- Subset of subsequent lines: apparent resistivity readings for each dipole spacing
- Each data line represents one electrode arrangement and contains 10 columns:
  - Column 1: Number of electrodes (4)
  - Columns 2–9: x and z locations for C1, C2, P1, P2 electrodes
  - Column 10: Resistance value
- Units: column 10 values are in ohm-meters (Ωm), corresponding to subsurface resistivity readings.

## Data content and interpretation
- Apparent resistivity readings are provided for multiple electrode configurations per line.
- The dataset uses a 4-electrode array with ten data entries per line, enabling resistivity modeling.
- The data include topographic coordinates (x, z) for each measurement point.

## File generation and provenance
- .dat files were generated from raw .stg files produced by an AGI SuperSting R8 (STING) resistivity meter.
- A bespoke Python script was used to convert raw data to the .dat format and to add topographic data.

## Metadata and supporting materials
- Survey numbering convention: e.g., Survey_01 with suffix _NZ01 indicating location.
- SupportingDocumentation.txt: detailed information on data collection, generation methods, and quality control.
- Sup_Table_for_Survey.csv: metadata table with:
  - Survey numbers and suffixes
  - Start/end coordinates (eastings/northings)
  - Line geometry (length)
  - Survey parameters (dipole size, max dipole, number of electrodes, electrode spacing)
- A map of survey lines and a corresponding .kmz file are available in the associated paper.

## Usage and data products
- Primary use: input for inversion (res2dinv) to derive subsurface resistivity models.
- Topographic data included to improve inversion accuracy.
- Facilitates creating downstream data products such as resistivity profiles, maps, and interpretable charts for broader analysis or public communication.
- Data can be combined with other survey data or spatial datasets for broader geophysical or hydrogeological studies.

## Considerations for data support
- Array type specified as non-conventional/general (code 11); users should refer to res2dinv documentation for interpretation.
- Data quality and completeness depend on the underlying survey execution and processing documented in SupportingDocumentation.txt and the associated paper.
- For re-use, consult Sup_Table_for_Survey.csv and the provided maps/kmz to understand spatial context and survey coverage.