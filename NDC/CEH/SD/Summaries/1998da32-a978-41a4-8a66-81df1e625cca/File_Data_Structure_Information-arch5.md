# Details of Data Structure

## Overview
- 17 .dat files from electrical resistivity tomography (ERT) surveys in the MAKUTAPORA basin, Tanzania (28/06/2019–16/07/2019).
- Data prepared for the res2dinv program; ASCII-delimited; produced from raw .stg files from an AGI SuperSting R8, with bespoke Python code adding topographic data.

## Data format and structure
- ASCII delimited: comma, space, or LF/CR separators; structured for res2dinv ingestion.
- Line-by-line metadata (per file):
  - Line 1: Survey line name
  - Line 2: Electrode spacing
  - Line 3: Array type (codes; general array used: 11)
  - Line 4: Sub-array type (0 none, 1 general)
  - Line 5: Header (inversion data choice: apparent resistivity or resistance values)
  - Line 6: 1 indicates resistance value
  - Line 7: Number of data points
  - Line 8: Type of x-location (0 none; 1 or 2 topography present; here 2)
  - Line 9: IP data flag (0 none; 1 present)
- Data rows: one line per electrode arrangement with 10 columns
  - Column 1: Number of electrodes (4)
  - Columns 2–9: x and z locations of C1, C2, P1, P2
  - Column 10: Resistance value (units: ohm-meters, Ωm)
- Data choices: apparent resistivity values or direct resistance values based on Line 5
- Data points are arranged for a 4-electrode array; each file contains measurements across multiple dipole spacings (10 data columns per line)

## Data provenance and generation
- Generated from raw .stg files produced by AGI SuperSting R8 (STING) resistivity meter
- A bespoke Python script converted .stg to .dat and added topographic data

## Metadata and accompanying files
- Survey identifiers: each .dat file includes a survey number (e.g., Survey_01) and a suffix (e.g., _NZ01) indicating location
- SupportingDocumentation.txt: details collection/generation methods and QC
- Supp_Table_for_Survey.csv: survey numbers and suffixes, start/end coordinates (easting/northing), line geometry (length), and survey parameters (dipole size, max dipole, number of electrodes, electrode spacing)
- A map of survey lines and a .kmz file are available in the associated paper

## Data governance and accessibility considerations
- Metadata should capture: array type (11 general array), topography presence (Line 8 = 2), data type (resistance vs. apparent resistivity), electrode geometry, and units (Ωm)
- Data lineage and provenance: document the transformation from .stg to .dat via the Python script, plus topographic augmentation
- QC and standards: reference SupportingDocumentation.txt and the associated paper for quality control methods
- Accessibility and discoverability: maintain consistent naming (Survey_XX, suffix), provide ancillary files (Supp_Table_for_Survey.csv, map, .kmz) for context and reuse

## Relevance and use for stakeholders
- Core dataset for subsurface characterization using resistivity data; essential for res2dinv analyses
- Enables cross-referencing of coordinates, electrode geometry, and measurement values across lines
- Supports reproducibility through explicit data structure, provenance, and accompanying metadata

## Potential challenges for stewardship
- Aligning legacy array type (11 general array) with broader metadata schemas
- Ensuring complete metadata coverage for user needs and discoverability
- Managing large data transfers and ensuring interoperability with other formats or software
- Clarifying data licensing, access rights, and any embargoes via accompanying documentation and associated paper