# Details of Data Structure

- Context and purpose
  - 17 .dat files containing electrical resistivity tomography (ERT) survey data from the MAKUTAPORA basin, Tanzania, collected 28/06/2019 to 16/07/2019.
  - Data formatted as ASCII delimited (comma, space, or line break) for use with res2dinv software; created from raw .stg files from an AGI SuperSting R8 (STING) meter using a bespoke Python script that also added topographic data.

- File structure and content
  - Each .dat file begins with header lines describing the survey and data:
    - Line 1: survey line name
    - Line 2: electrode spacing
    - Line 3: array type (11 = Non Conventional/general array; other codes listed for reference)
    - Line 4: Sub-Array type (0 = none, 1 = general)
    - Line 5: header option (invert using apparent resistivity or direct resistance)
    - Line 6: 1 indicates resistance value
    - Line 7: number of data points
    - Line 8: type of x-location (0 = none; 2 = topographic data present)
    - Line 9: IP data flag (0 = none; 1 = present)
  - Data lines (subsequent lines)
    - Each line corresponds to one electrode arrangement (dipole spacing) and has 10 columns:
      - Column 1: number of electrodes (4)
      - Columns 2-9: x and z coordinates of C1, C2, P1, P2 electrodes
      - Column 10: data value (resistance or apparent resistivity)
    - Units for column 10 are ohm metre (Ωm), corresponding to subsurface resistivity.
  - A total of 10 data columns per line reflect measurements across various dipole spacings for a given arrangement.

- Data provenance and identifiers
  - Data generated from raw .stg files using a bespoke Python code.
  - Topographic data added during processing.
  - Each .dat file corresponds to a survey with identifiers such as Survey_01 and a suffix (e.g., _NZ01) indicating location/survey.

- Supporting documentation and metadata
  - SupportingDocumentation.txt: detailed information on collection/generation methods and quality control; references to the associated paper.
  - Supp_Table_for_Survey.csv: survey numbers and suffixes, coordinates (start/end easting/northing), line geometry (length), and survey parameters (dipole size, max dipole, number of electrodes, electrode spacing).
  - A map of survey lines and a .kmz file of these lines are provided in the associated paper.

- Practical notes for analysis
  - Inversion compatibility: data are prepared for res2dinv; for inversion, choose between apparent resistivity and resistance per the header settings.
  - Topography: topographic coordinates are included; account for topography during inversion.
  - Consistency and units: ensure consistent use of Ωm units across datasets and during model fitting.
  - Metadata and traceability: use Supp_Table_for_Survey.csv to link data points to geometry and survey parameters for reproducibility and integration with other datasets.