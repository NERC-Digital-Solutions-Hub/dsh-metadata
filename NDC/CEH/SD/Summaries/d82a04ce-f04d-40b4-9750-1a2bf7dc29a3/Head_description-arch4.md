# Hydraulic head dataset (6 files), details as follows:

## Overview
- A bundled data package comprising three interlinked hydrological datasets collected across multiple sites and rivers in the UK.
- Datasets include hydraulic head, saturated hydraulic conductivity, and porewater chemistry.
- Time spans primarily 2013–2015 for most data, with head data extending to 2020 in some files; multiple sites are represented (River Ebble, Wylye, Avon, Nadder, Sem).

## Datasets Included
- Hydraulic head dataset (6 files)
  - Water height in metres above OS datum (river stage, bed and bank) derived from pressure transducers (Solinst or HOBO).
  - Location identifiers are OS Grid References (e.g., SU05598 25343 for Ebble; ST85779 38053 for Wylye; etc.).
- Hydraulic Conductivity dataset (6 files)
  - Saturated hydraulic conductivity (Ksat) in m/s from slug tests (falling/rising head) using HOBO pressure transducers in piezometers.
  - Each file includes site location and measurement details.
- Porewater chemistry dataset (6 files)
  - Porewater chemistry from samples taken via piezometer networks (riverbed and bankside locations).
  - Includes site coordinates, sample type, depth, and a broad suite of chemistry measurements (e.g., O2, Fe(II), Cl, nitrate, sulfate, DOC, major ions, silicate, Sr, DIC, methane, nitrous oxide, nitrate as N, phosphate as P, ammonia as N).

## Data Formats and Coverage
- Hydraulic head: six Excel spreadsheets; each contains date/time columns (dd/mm/yyyy hh:mm) plus head values (mAOD) per site.
- Hydraulic conductivity: six spreadsheets; five columns per sheet: piezometer ID, test type (Rising/Falling), start date/time, Ksat value, and quality comments.
- Porewater chemistry: six spreadsheets; standardized columns including Date, Site code, Sample type, Piezometer cluster (UC/DC), Depth, and numerous chemical analytes.

## Site and Instrumentation Metadata
- Sites include rivers Ebble, Wylye, Avon, Nadder, Sem; precise OS Grid References are provided.
- Field instruments listed: HOBO U20-001-01, Levelogger Edge (Solinst), Manta 2 (Eureka Water Probes).

## Data Structure and Labelling
- Piezometer labelling:
  - In-stream piezometers: upstream (UC) and downstream (DC) clusters, ~10 m apart, depths of 100 cm, 50 cm, 20 cm.
  - Porewater sampling tubes exist at 10 cm, 20 cm, 30 cm, 50 cm, 70 cm, 100 cm depths in UC/DC clusters.
  - Bank piezometers: LB (left bank) and RB (right bank), often in triangles; labels 1, 2, 3 indicate proximity to UC/DC clusters and screen depth approximates river bed depth.
- Data files are organized into three 6-file groups (head, conductivity, porewater), with consistent column structures described for each dataset.

## Quality Control and Data Processing
- Hydraulic head data corrected for drift (probe movement) using manual piezometer readings at ~2–4 week intervals with assumed linear drift.
- Slug tests (falling/rising head) used to compute Ksat; replicates conducted when possible; comparisons between test types provided; notes on data quality included.
- Documentation notes on data quality accompany datasets; queries directed to specific contact(s).

## Analytical Methods and QC
- Field oxygen measured with Unisense electrode; Fe(II) fixed in the field and analysed by UV spectrophotometry upon return.
- Ion analyses (Cl, nitrate, sulfate) via ion chromatography; detection limits and precision statistics provided; certified reference materials specified.
- Major cations (Ca, K, Mg, Na), silica, and Sr measured via ICP-OES with specified detection limits and precision; CRMs noted.
- Phosphate, ammonia, and nitrite analysed with Skalar Auto Analyzer; LODs and precision reported; CRMs noted.
- Dissolved organic carbon measured by non-purgeable organic carbon method; LOD and precision reported.
- All chemical data schemes and QA notes are documented; further queries directed to Kate Heppell.

## Data Structure Details
- Data organization specifics:
  - Hydraulic head: date/time (dd/mm/yyyy hh:mm) in column A, followed by head data per site.
  - Hydraulic conductivity: five columns per sheet (piezometer ID, test type, start date/time, Ksat, quality).
  - Porewater chemistry: comprehensive set of columns (Date, Site code, Sample type, Piezometer cluster, Depth, and numerous analyte measurements).
- Notable data markers: na (not analysed) and <LOD (below detection limit).

## Access and Contacts
- Queries about the datasets should be directed to:
  - Andy Binley (a.binley@lancaster.ac.uk)
  - Kate Heppell (c.m.heppell@qmul.ac.uk)

## Implications for Data Leaders
- The package demonstrates a multi-dataset data governance approach: integrated head, conductivity, and chemistry data with standardized labeling, timing, and site metadata.
- Emphasizes the importance of drift corrections, replicates, and detailed QA notes to ensure data reliability across datasets.
- Highlights the need for consistent data structures, clear metadata (locations, depths, instrument types), and well-documented analytical methods for effective data discovery, reuse, and cross-site comparisons.
- Encourages establishing processes for data access requests, cross-dataset integration, and potentially co-ownership of modular data products for broader community use.