# Metadata for morphological data

- Overview
  - Three datasets of threespine stickleback morphological data, with corresponding photographs for the third dataset.
  - Each tps file contains x,y coordinates for 32 landmarks per specimen; landmarks 23–32 are semi-landmarks needing special analysis.
  - Images and data are organized to support morphometrics analyses across wild-caught and lab-reared individuals, from multiple lakes/ponds and temperature treatment regimes.
  - Data formats include TPS files, accompanying CSV metadata, and JPEG images (dataset 3).

- Dataset 1: curveAppendedWildThenLabData.tps
  - Accompanying file: data file 1 categories.csv
  - Design: first 331 specimens wild-caught, next 320 lab-reared; image names encode population information.
  - Metadata in accompanying file includes: population, thermal habitat, lab or wild status, and pair.
  - The column popprecise provides the exact population code (e.g., mw, mc, gts, cs, sw, sc, stc, stw, ac, aw, rkc, rkrw).

- Dataset 2: f2_ecomorph_crosses_temp_treatments.tps
  - Accompanying file: variables f2_ecomorph_crosses_temp_treatments.csv
  - Design: F2 generation from lab-reared crosses reared under two temperatures (12°C and 18°C).
  - Metadata includes: population, treatment in F1 and F2 generations, pair, individual ID, and experimental unit (EU); also includes thermal ecotype.

- Dataset 3: F2 hybrids images and data
  - Contents: several JPEG files of F2 hybrid fish organized in master folders SKR, MYV, and ASNH (populations Saudarkrokru, Myvatn, and Ashildarholtsvatn).
  - Within each population folder are subfolders with JPEG photos and corresponding tps data files (same landmarks as above).
  - Folder names reflect temperature treatment: 12at12, 12at18, 18at12, 18at18 (two generations at 12°C or 18°C; cross-generational temperatures indicated).

- Landmarks and analysis notes
  - 32 landmarks per specimen; semi-landmarks (23–32) require special consideration in analysis.
  - TPS files are readable by multiple morphometrics packages or can be opened as plain text.

- Population and sampling context
  - Specimens originate from lakes/ponds with coded sites and habitat types (ambient vs geothermal): Ashildarholtsvatn (AshnC, AshnW), Myvatn (MyvC, MyvW), Gardsvatn (CSWY), Grettislaug (GTS), Saudarkrokur (SkrC, SkrW), Steinstaddur (stnstW, stnstC), Reykholt (rkrc, rkrw).
  - Supp Table 1 provides exact locations and chemistry measures.

- Data governance and stewardship considerations for Data Stewards
  - Ensure metadata completeness and consistency across datasets (clear variable definitions, population codes, and habitat designations).
  - Validate data formats and interoperability (TPS with 32 landmarks; correct handling of semi-landmarks).
  - Maintain provenance and documentation of data processing steps (quality assurance, cleaning, transformations).
  - Track data availability, access controls, and any embargo or usage restrictions; plan for updates and versioning.
  - Coordinate with data creators to ensure alignment between datasets and accompanying metadata; facilitate cataloging and portal deposition.