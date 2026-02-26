# Hydraulic head dataset (6 files), details as follows:

- Overview
  - A combined data package consisting of three related datasets: hydraulic head, hydraulic conductivity (Ksat), and porewater chemistry.
  - Each dataset comprises six Excel spreadsheets, for a total of 18 spreadsheets.
  - Data cover multiple river sites in the region, with detailed site-specific metadata and sampling design.

## Datasets and contents

- Hydraulic head dataset (6 files)
  - Files (examples): CE_Head_data.csv, CW_Head_data.csv, GA_Head_data.csv, GN_Head_data.csv, AS_Head_data.csv, AP_Head_data.csv
  - Description: Water height in metres above OS datum (river stage, bed and bank) measured with pressure transducers (Solinst or HOBO).
  - Locations (OS Grid References):
    - CE_Head_data.csv: SU05598 25343 (River Ebble)
    - CW_Head_data.csv: ST85779 38053 (River Wylye)
    - GA_Head_data.csv: SU09723 57824 (River Avon)
    - GN_Head_data.csv: ST92380 27376 (River Nadder)
    - AS_Head_data.csv: ST92346 27381 (River Sem)
    - AP_Head_data.csv: ST89198 28431 (River Sem)
  - Time spans vary by site, with data spanning early to mid-2010s (e.g., 2013–2015 periods noted in descriptions).
  - Data format: Each spreadsheet uses date and time (dd/mm/yyyy hh:mm) in column A followed by head values (mAOD) for multiple piezometers.

- Hydraulic Conductivity dataset (6 files)
  - Files (examples): CE_Hydraulic_conductivity.csv, CW_Hydraulic_conductivity.csv, GA_Hydraulic_conductivity.csv, GN_ Hydraulic_conductivity.csv, AS_ Hydraulic_conductivity.csv, AP_ Hydraulic_conductivity.csv
  - Description: Saturated hydraulic conductivity (Ksat) in m/s derived from slug tests (falling or rising head) using HOBO pressure transducers in piezometers.
  - Locations (OS Grid References): same sites as head data
    - CE: SU05598 25343 (River Ebble)
    - CW: ST85779 38053 (River Wylye)
    - GA: SU09723 57824 (River Avon)
    - GN: ST92380 27376 (River Nadder)
    - AS: ST92346 27381 (River Sem)
    - AP: ST89198 28431 (River Sem)
  - Data format: 5 columns per file: piezometer ID, Rising or falling test, Start date/time, Saturated hydraulic conductivity (m/s), and quality control comments.
  - QA: Includes replicates where possible; tests compare falling vs rising head results; data quality notes accompany each dataset.

- Porewater chemistry dataset (6 files)
  - Files (examples): CE_porewater_chemistry.csv, CW_porewater_chemistry.csv, GA_porewater_chemistry.csv, GN_porewater_chemistry.csv, AS_porewater_chemistry.csv, AP_porewater_chemistry.csv
  - Description: Pore water chemistry from samples collected via porewater sampling tubes in piezometer networks (riverbed and banks).
  - Location metadata: OS Grid References match above sites
  - Sample identifiers: In-stream bed and bank locations; porewater sample tubes extend to screen depths
  - Analytes included (example columns): Oxygen, Fe(II), Chloride, Nitrate, Sulphate, Dissolved Organic Carbon, Al, Ca, K, Mg, Na, Si, Sr, Dissolved Inorganic Carbon, methane, nitrous oxide, nitrate as N, phosphate as P, ammonia as N; Depth of porewater; Sample type and cluster (UC=upstream, DC=downstream); Depths (m)
  - Data quality: 'na' indicates not analysed; <LOD indicates below detection limit

## Field instruments and QA/QC

- Field equipment
  - HOBO U20-001-01 data loggers
  - Levelogger Edge (Solinst)
  - Manta 2 (Eureka Water Probes)

- Quality control and processing notes
  - Hydraulic head data corrected for drift (probe movement) using manually dipped piezometer levels, assuming linear drift.
  - Slug tests (falling/rising head) used to compute Ksat; repeat tests performed when possible; comparisons of methods provided.
  - Data quality notes included; queries about datasets directed to specific contacts.
  - Analytical chemistry methods:
    - Oxygen by field electrode; Fe(II) by UV after field fixation
    - Chloride, nitrate, sulphate by ion chromatography with specified limits of detection and repeatability
    - Major cations (Ca, K, Mg, Na, Sr) by ICP-OES with detection limits and precision
    - Phosphate, ammonia, nitrite by Skalar Auto Analyser with LODs and accuracy references
    - Dissolved Organic Carbon by non-purgeable organic carbon method
  - References for materials and standards included (certified reference materials and accuracy ranges)
  - Contacts for queries:
    - Andy Binley (a.binley@lancaster.ac.uk) for hydraulic head and Ksat datasets
    - Kate Heppell (c.m.heppell@qmul.ac.uk) for porewater chemistry datasets

## Data structure and usage notes

- Piezometer labeling and arrangement
  - In-stream piezometers: upstream cluster (UC) and downstream cluster (DC); approximately 10 m apart
  - Piezometer depths: 100 cm, 50 cm, and 20 cm below stream bed
  - Porewater sampling tubes at depths: 10 cm, 20 cm, 30 cm, 50 cm, 70 cm, 100 cm
  - Bank piezometers: clusters LB (left bank) and RB (right bank), often in triangular arrangements
  - Secondary labeling within banks: 1 (adjacent to UC), 2 (adjacent to DC), 3 (third corner)
  - Bank piezometer screen depth approximates river bed depth near the bank
  - Porewater tubes extend to screen depth and halfway to screen

- File formats and data columns
  - Hydraulic head spreadsheets: date/time (dd/mm/yyyy hh:mm) in column A; subsequent columns contain head values (mAOD) for sites
  - Ksat spreadsheets: 5 columns - Piezometer ID, Test type (Rising/Falling), Start date/time, Ksat (m/s), Quality control comments
  - Porewater chemistry spreadsheets: Date, Site code, Sample type (SW, B, Sed), Piezometer cluster (UC/DC), Depth (m), and a wide suite of analyte columns (Oxygen, Fe(II), Cl, NO3, SO4, DOC, Al, Ca, Fe, K, Mg, Na, Si, Sr, DIC, methane, N2O, nitrate as N, phosphate as P, ammonia as N); placeholders for not analysed (na) or below detection limit (<LOD)

- Units and interpretation
  - Hydraulic head: metres above OS datum (mAOD)
  - Hydraulic conductivity: metres per second (m/s)
  - Chemical concentrations: milligrams per litre (mg/L) for most solutes; mg C/L for DOC; micromolar and microgram per litre values for some constituents; depth in metres

## Relevance for analysis

- Enables multi-site, multi-depth time-series analysis of groundwater-surface water interactions
- Facilitates correlation analyses between hydraulic head, Ksat, and porewater chemistry across upstream vs downstream and bank vs in-stream locations
- Supports development of predictive models relating hydrological conditions to chemical transport and redox conditions in river systems
- Rich metadata and QA/QC documentation improve data reliability and reproducibility of analyses