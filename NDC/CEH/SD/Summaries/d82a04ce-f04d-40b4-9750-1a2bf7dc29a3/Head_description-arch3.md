# Hydraulic head dataset (6 files), details as follows:

- Datasets included
  - Hydraulic head dataset (6 files):
    - CE_Head_data.csv: From 23- Sept-2020 13 to 02- Sept-2020 15; water height above OS datum (river stage, bed and bank) using Solinst transducers; Location SU05598 25343 (River Ebble).
    - CW_Head_data.csv: From 01- Jun-2013 to 26- Aug-2015; water height above OS datum using HOBO transducers; Location ST85779 38053 (River Wylye).
    - GA_Head_data.csv: From 26- Jun-2013 to 15- Sept-2015; water height above OS datum using HOBO transducers; Location SU09723 57824 (River Avon).
    - GN_Head_data.csv: From 25- Jun-2013 to 30- Sept-2015; water height above OS datum using HOBO transducers; Location ST92380 27376 (River Nadder).
    - AS_Head_data.csv: From 25- Feb-2014 to 03- Sept-2015; water height above OS datum using HOBO transducers; Location ST92346 27381 (River Sem).
    - AP_Head_data.csv: From 09- Jun-2014 to 03- Sept-2015; water height above OS datum using HOBO transducers; Location ST89198 28431 (River Sem).

- Hydraulic Conductivity dataset
  - CE_Hydraulic_conductivity.csv: Saturated Hydraulic Conductivity (Ksat) in m/s; measured via slug tests with HOBO transducers; Location SU05598 25343 (River Ebble). 
  - CW_Hydraulic_conductivity.csv: Ksat; Location ST85779 38053 (River Wylye).
  - GA_Hydraulic_conductivity.csv: Ksat; Location SU09723 57824 (River Avon).
  - GN_Hydraulic_conductivity.csv: Ksat; Location ST92380 27376 (River Nadder).
  - AS_Hydraulic_conductivity.csv: Ksat; Location ST92346 27381 (River Sem).
  - AP_Hydraulic_conductivity.csv: Ksat; Location ST89198 28431 (River Sem).

- Porewater chemistry dataset
  - CE_porewater_chemistry.csv: Pore water chemistry from piezometer network; location SU05598 25343 (River Ebble).
  - CW_porewater_chemistry.csv: Pore water chemistry; location ST85779 38053 (River Wylye).
  - GA_porewater_chemistry.csv: Pore water chemistry; location SU09723 57824 (River Avon).
  - GN_porewater_chemistry.csv: Pore water chemistry; location ST92380 27376 (River Nadder).
  - AS_porewater_chemistry.csv: Pore water chemistry; location ST92346 27381 (River Sem).
  - AP_porewater_chemistry.csv: Pore water chemistry; location ST89198 28431 (River Sem).

- Fieldwork Hydrological Instrumentation
  - HOBO U20-001-01, Onset Corporation, USA
  - Levelogger Edge, Solinst, Canada
  - Manta 2, Eureka Water Probes, USA

- Quality control and data processing
  - Hydraulic head measurements corrected for drift using manually dipped piezometer levels (approx. every 2–4 weeks) with assumed linear drift.
  - Falling and rising head (slug) tests used to compute Ksat; repeat tests conducted where possible; replicates included.
  - Data quality notes accompany datasets; queries directed to Andy Binley (a.binley@lancaster.ac.uk).

- Analytical chemistry methods and quality control
  - In-field oxygen measured with Unisense electrode; Fe(II) fixed in field and analyzed by UV spectrophotometry.
  - Chloride, nitrate, sulfate analyzed by ion chromatography (limits of detection ~0.5 mg/L; RSDs 4.7–8.8% depending on analyte; CRM Ultra Check WP Nutrients used for accuracy ~3.3% at specified levels).
  - Major cations (K, Mg, Na, Ca), silica, and strontium analyzed by ICP-OES with specified limits and QA values; CRM SPS-SW2 used.
  - Phosphate, ammonia, nitrite analyzed via Skalar Auto Analyzer; QA with CRM Ultra Check WP Nutrients.
  - DOC quantified by non-purgeable organic carbon method; QA with CRM TO1C4M14F1.
  - Queries about datasets to Kate Heppell (c.m.heppell@qmul.ac.uk).

- Data structure and format
  - Piezometers labeled by site: in-stream clusters upstream (UC) and downstream (DC) ~10 m apart; depths of 100 cm, 50 cm, 20 cm below bed used for depths.
  - Bank piezometers installed as clusters (LB left bank, RB right bank); secondary labels indicate proximity to upstream (1) or downstream (2) clusters; third piezometer completes an approximately equilateral triangle (3).
  - Porewater tubes extend to screen depth and halfway to screen in bank piezometers.
  - This document comprises:
    - 6 hydraulic head Excel spreadsheets (one per site) with date/time and head data (mAOD).
    - 6 saturated hydraulic conductivity spreadsheets (piezometer ID, test type, start time, Ksat, quality notes).
    - 6 porewater chemistry spreadsheets with a consistent column structure (Date, Site code, Sample type, Piezometer cluster, Depth, multiple chemical and isotopic parameters, NA/LOD indicators).
  - Columns and data conventions:
    - Hydraulic head: date/time (dd/mm/yyyy hh:mm) in column A; subsequent columns for head data.
    - Ksat: piezometer ID, test type (Rising/Falling), start date/time, Ksat (m/s), quality notes.
    - Porewater chemistry: Date, Site code, Sample type, Piezometer cluster, Depth, numerous analytes (O2, Fe(II), chloride, nitrate, sulfate, DOC, Al, Ca, Fe, K, Mg, Na, Si, Sr, DIC, methane, N2O, various nitrogen/phosphorus species), with na or <LOD indicating missing or below detection.
  - Note on data sharing and interpretation:
    - Data may require transformation for use in analyses; alignment of metadata and robust QA/QC is essential.
    - Queries and data issues should be directed to the provided contact persons.

- Governance and monitoring implications (relevant to monitoring framework authors)
  - Provides multi-parameter environmental health indicators: river stage (head data), aquifer/sediment hydraulic properties (Ksat), and porewater chemistry.
  - Demonstrates structured field data collection, multi-site deployment, and standardized QA/QC procedures.
  - Highlights practical data governance considerations: metadata completeness, data sharing barriers, need for consistent labeling, and clear documentation of methods and QA across datasets.
  - Useful as a template for designing monitoring frameworks that integrate hydrological and chemical indicators to evaluate policy impacts and inform future decisions.