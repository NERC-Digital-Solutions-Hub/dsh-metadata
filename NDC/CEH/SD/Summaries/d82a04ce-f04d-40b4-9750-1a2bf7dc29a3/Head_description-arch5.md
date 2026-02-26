# Hydraulic head dataset (6 files), details as follows:

## Overview
- A multi-dataset collection consisting of hydraulic head, hydraulic conductivity, and porewater chemistry data from in-stream and bank piezometer networks.
- Includes field instrumentation details, quality control procedures, analytical methods, and data structure conventions.
- Aimed at enabling data governance, discoverability, and reuse with clear provenance and metadata.

## Datasets included
- Hydraulic head (6 files)
  - CE_Head_data.csv, CW_Head_data.csv, GA_Head_data.csv, GN_Head_data.csv, AS_Head_data.csv, AP_Head_data.csv
  - Each file contains date/time and head measurements (expressed as mAOD) for site instrumentation; location provided as OS Grid References; transducers noted (Solinst HOBO variants).
  - Date ranges span 2013–2015 (varies by site).
- Hydraulic Conductivity (6 files)
  - CE_Hydraulic_conductivity.csv, CW_ Hydraulic_conductivity.csv, GA_ Hydraulic_conductivity.csv, GN_ Hydraulic_conductivity.csv, AS_ Hydraulic_conductivity.csv, AP_ Hydraulic_conductivity.csv
  - Ksat values from slug tests (falling or rising head) using HOBO transducers; includes site locations (OS Grid References).
- Porewater chemistry (6 files)
  - CE_porewater_chemistry.csv, CW_porewater_chemistry.csv, GA_porewater_chemistry.csv, GN_porewater_chemistry.csv, AS_porewater_chemistry.csv, AP_porewater_chemistry.csv
  - Analyte suite includes O2, Fe(II), Cl−, nitrate, sulfate, DOC, major cations/anions, trace parameters, and porewater depth; includes sample type, site code, and depth.

## Data collection and instrumentation
- Field instruments: HOBO U20-001-01, Levelogger Edge (Solinst), Manta 2 (Eureka) used for head and hydrology measurements.
- Data structure describes a dual-cluster piezometer setup (UC upstream, DC downstream) about 10 m apart, with bank piezometers LB and RB and sub-cluster labeling (1, 2, 3) corresponding to proximity to the clusters.
- Porewater sampling tubes integrated into multi-level piezometers (depths 10–100 cm) for in-stream and bank sites.

## Quality control and data processing
- Hydraulic head corrections account for probe drift via manual piezometer checks (every 2–4 weeks) with an assumed linear drift model.
- Falling/rising head slug test data used for Ksat calculations; replicate tests performed when possible and documented.
- Data quality notes accompany datasets; the term “classic” denotes expected log-linear head–time response.
- Queries about head datasets directed to Andy Binley (a.binley@lancaster.ac.uk).

## Analytical chemistry methods and QC
- Field oxygen measured with a Unisense electrode; Fe(II) fixed in the field and analyzed by UV spectrophotometry in the lab.
- Anions/cations and DOC analyzed via standard methods (Ion Chromatography, ICP-OES, Skalar Auto Analyzer) with specified detection limits and precision metrics.
- Certified Reference Materials used for QA/QC (listing per analyte and method); QC comments and detection limits documented.
- Queries about porewater chemistry datasets directed to Kate Heppell (c.m.heppell@qmul.ac.uk).

## Data structure and metadata conventions
- Piezometer labeling: UC/DC clusters; depths labeled (e.g., UC100, DC100); bank clusters LB/RB with sub-labels 1, 2, 3; bed-screen depths aligned to river center.
- Data organization: total of 6 head spreadsheets, 6 conductivity spreadsheets, and 6 porewater spreadsheets.
- File formats and columns:
  - Hydraulic head: date/time (dd/mm/yyyy hh:mm) in column A, head data in subsequent columns by site.
  - Hydraulic conductivity: 5 columns: piezometer ID, test type (Rising/Falling), start date/time, Ksat (m/s), quality control comments.
  - Porewater chemistry: Date, Site code, Sample type, Piezometer cluster, Depth, and a wide suite of chemical parameters (with na or <LOD where applicable).

## Data access, provenance, and contacts
- Head dataset queries: Andy Binley (a.binley@lancaster.ac.uk).
- Porewater chemistry QA/QC: Kate Heppell (c.m.heppell@qmul.ac.uk).
- Data likely intended for portal sharing and cataloging as discrete, well-annotated Excel spreadsheets per data type.

## Data quality notes and limitations
- Some fields contain missing values (na) or concentrations below detection limits (<LOD).
- Data include explicit quality control comments and notes on replicate tests; drift correction and calibration details are provided to assist governance and re-use.

## Governance considerations for Data Stewards
- Ensure consistent metadata across all 18 CSV/Excel files (head, conductivity, porewater) for easy discovery and integration.
- Maintain versioning and provenance trails, including instrument IDs, calibration dates, and QA/QC annotations.
- Verify and document data update procedures, and implement clear embargo or access policies if applicable.
- Facilitate interoperability by aligning units, column naming, and date formats across datasets.
- Provide data access contacts and ensure user support channels are established for queries and issue tracking.