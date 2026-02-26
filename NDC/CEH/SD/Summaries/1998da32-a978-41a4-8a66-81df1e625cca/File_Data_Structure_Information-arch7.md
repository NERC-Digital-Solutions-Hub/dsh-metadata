# Details of Data Structure

## Overview
- 17 .dat files from electrical resistivity tomography surveys in the MAKUTAPORA basin, Tanzania (28/06/2019 to 16/07/2019).
- Data formatted for res2dinv processing; ASCII delimited with items separated by comma, space, or line breaks.
- Generated from raw .stg files produced by an AGI SuperSting R8 resistivity meter; a bespoke Python script converted to .dat and added topographic data.

## Data format and structure
- res2dinv-compatible file structure; array type 11 indicates Non-Conventional or general arrays.
- Line definitions in each .dat file:
  - Line 1: Name of survey line
  - Line 2: Electrode spacing
  - Line 3: Array type (Wenner=1, Pole-pole=2, Dipole-dipole=3, Pole-dipole=6, Schlumberger=7, Equatorial dipole-dipole=8, Non Conventional/general array=11)
  - Line 4: Sub-Array type (0 = none, 1 = general)
  - Line 5: Header (inversion data type: apparent resistivity values or direct resistance values)
  - Line 6: Indicator (1 to indicate resistance value)
  - Line 7: Number of data points
  - Line 8: Type of x-location (2 if topographic data is present)
  - Line 9: IP data flag (0 for none, 1 if present)
- Data rows: each line represents measurements for one electrode arrangement; 10 columns for a 4-electrode array:
  - Column 1: Number of electrodes (4)
  - Columns 2–9: x and z locations of C1, C2, P1, P2 electrodes
  - Column 10: Resistance value
- Units: column 10 values are in ohm-meters (Ωm)
- References to further details in the res2dinv manual (Data file operations, Data format; Appendix L for non-conventional/general arrays)

## Data generation and location metadata
- .dat files generated from raw .stg files from the AGI SuperSting R8 (STING) resistivity meter
- A bespoke Python code converted raw data to .dat and added topographic data
- Each .dat file includes a survey number (e.g., Survey_01) and a suffix (e.g., _NZ01) indicating location and survey instance

## Supporting materials and metadata files
- SupportingDocumentation.txt: detailed collection/generation methods and quality control; additional information available in the associated paper
- Supp_Table_for_Survey.csv: details of survey numbers and suffixes, coordinates (eastings and northings of start and end), line geometry, and survey parameters (dipole size, max dipole, number of electrodes, electrode spacing)
- A map of survey lines and a .kmz file of these lines are provided in the associated paper

## GIS usage and integration
- Provides line geometries and coordinates suitable for GIS mapping and analysis
- Topographic data included for measurement locations, enabling terrain-aware visualization
- Supp_Table_for_Survey.csv facilitates linking survey geometries with parameters for visualization and interpretation
- Map and KMZ files enable visualization in GIS tools and Google Earth for contextual understanding of survey coverage