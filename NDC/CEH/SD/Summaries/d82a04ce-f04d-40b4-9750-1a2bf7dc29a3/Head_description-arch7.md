# Hydraulic head dataset (6 files), details as follows:

- Overview
  - Three linked hydro-geo datasets described: Hydraulic head dataset (6 files), Hydraulic Conductivity dataset (6 files), and Porewater chemistry dataset (6 files).
  - Geospatial context provided via Ordnance Survey (OS) Grid References for each site (e.g., SU05598 25343; ST85779 38053).

- Hydraulic head dataset (6 files)
  - Files: CE_Head_data.csv, CW_Head_data.csv, GA_Head_data.csv, GN_Head_data.csv, AS_Head_data.csv, AP_Head_data.csv.
  - Content: Water height in metres above OS datum (river stage, bed and bank) calculated from Solinst pressure transducers or similar HOBO devices.
  - Timeframe and location: Each file covers a site with a defined OS Grid Reference; data from various years (e.g., 2013–2020).
  - Structure: Each spreadsheet uses date/time (dd/mm/yyyy hh:mm) in column A, followed by head data per site/instrumentation.

- Hydraulic Conductivity dataset (6 files)
  - Files: CE_Hydraulic_conductivity.csv, CW_Hydraulic_conductivity.csv, GA_ Hydraulic_conductivity.csv, GN_ Hydraulic_conductivity.csv, AS_ Hydraulic_conductivity.csv, AP_ Hydraulic_conductivity.csv.
  - Content: Saturated hydraulic conductivity (Ksat) in m/s measured with slug tests (falling or rising head) using HOBO pressure transducers in piezometers.
  - Location labels: OS Grid References corresponding to each site (same as head datasets).
  - Structure: 5 columns per file: piezometer ID code, test type (Rising/Falling), Start date/time, Ksat value, and quality control comments.

- Porewater chemistry dataset (6 files)
  - Files: CE_porewater_chemistry.csv, CW_porewater_chemistry.csv, GA_porewater_chemistry.csv, GN_porewater_chemistry.csv, AS_porewater_chemistry.csv, AP_porewater_chemistry.csv.
  - Content: Pore water chemistry from piezometer network (in riverbed and banks) with multiple chemical measurements.
  - Location: OS Grid References for each site (same as head/conductivity datasets).
  - Structure: Columns include Date, Site code, Sample type, Piezometer cluster (UC = upstream, DC = downstream), Depth (m), and a wide suite of analytes (Oxygen, Fe(II), Chloride, Nitrate, Sulphate, DOC, Al, Ca, Fe, K, Mg, Na, Si, Sr, DIC, methane, N2O, nitrate as N, phosphate as P, ammonia as N, with flags such as na and <LOD).

- Fieldwork Hydrological Instrumentation
  - Instruments: HOBO U20-001-01 data loggers, Levelogger Edge (Solinst), Manta 2 (Eureka Water Probes).
  - Purpose: Field data collection and instrumentation for hydraulic head and porewater measurements.

- Quality control for Hydraulic head and Saturated hydraulic conductivity
  - Hydraulic head: Corrected for drift using manually dipped piezometer levels, typically every 2–4 weeks; drift correction applied.
  - Conductivity: Falls/ rises slug tests with replication when possible; comparisons of falling vs rising head results included; dataset contains data quality notes.
  - Contact for queries: Andy Binley (a.binley@lancaster.ac.uk).

- Analytical chemistry methods and quality control
  - Oxygen: Measured in field with Unisense electrode; Fe(II) fixed in field and analysed by UV spectrophotometry later.
  - Anions/cations: Chloride, nitrate, sulphate analysed by ion chromatography; major cations (K, Mg, Na, Ca), Si, Sr analysed by ICP-OES; QA/QC with certified reference materials.
  - Phosphate, ammonia, nitrite: Analyzed by Skalar Auto Analyser; detection limits and precision reported; CRM used for accuracy.
  - DOC: Analyzed by non-purgeable organic carbon method with Skalar Formacs HT.
  - QA: Queries to Kate Heppell (c.m.heppell@qmul.ac.uk).

- Data Structure (organization and labelling)
  - Piezometers: Labeled by site; in-stream piezometers arranged upstream cluster (UC) and downstream cluster (DC), ~10 m apart.
  - Depths: Piezometers installed at depths of 100 cm, 50 cm, and 20 cm; multi-level sampling tubes extend to 10–100 cm depths.
  - Bank piezometers: Located on left bank (LB) and right bank (RB); bank clusters can be 3-point triangles (LB1/LB2/LB3, RB1/RB2/RB3); screen depths approximate river bed depth at the channel center.
  - Porewater: Tubes extend to screen depth and halfway to screen.
  - Data files: 6 head spreadsheets (date/time in column A, head data in subsequent columns), 6 conductivity spreadsheets (piezometer ID, test type, start date/time, Ksat, quality comments), 6 porewater spreadsheets (Date, Site code, Sample type, Piezometer cluster, Depth, and numerous chemical parameters).

- Data Access and contact for queries
  - Andy Binley: a.binley@lancaster.ac.uk
  - Kate Heppell: c.m.heppell@qmul.ac.uk

- Notes for GIS use
  - OS Grid References provide precise site locations for mapping and spatial analysis.
  - Data are organized by site with consistent naming conventions across head, conductivity, and porewater datasets, enabling joined GIS workflows and time-series analyses.