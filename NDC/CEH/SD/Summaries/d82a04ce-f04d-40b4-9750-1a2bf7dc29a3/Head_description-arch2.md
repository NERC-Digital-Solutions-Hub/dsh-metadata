# Hydraulic head dataset (6 files), details as follows:

## Overview
- Three integrated datasets for environmental monitoring: Hydraulic head, Hydraulic conductivity, and Porewater chemistry, each consisting of 6 Excel spreadsheets.
- Purpose: standardised, time-series data to assess environmental health and groundwater–surface water interactions across multiple sites.
- Data are collected with established field instrumentation and follow QA/QC procedures; datasets are stored for dissemination via appropriate portals.

## Datasets Included
- Hydraulic head dataset (6 files)
  - Measurements: Water height in metres above OS datum (mAOD), representing river stage, bed, and bank.
  - Sites: River Ebble (SU05598 25343), River Wylye (ST85779 38053), River Avon (SU09723 57824), River Nadder (ST92380 27376), River Sem (ST92346 27381).
  - Timeframes: Various periods spanning 2013–2020.
  - Instrumentation: Solinst pressure transducers and HOBO loggers.
- Hydraulic Conductivity dataset (6 files)
  - Measurements: Saturated hydraulic conductivity (Ksat) in m/s from slug tests (falling/rising head) using HOBO transducers.
  - Sites and locations mirror head dataset.
  - Timeframes: Same broad period coverage as head dataset.
- Porewater chemistry dataset (6 files)
  - Measurements: Porewater chemistry from piezometer network (in-stream bed and banks) including O2, Fe(II), Cl−, NO3−, SO42−, DOC, Al, Ca, K, Mg, Na, Si, Sr, DIC, methane, N2O, nitrate as N, phosphate as P, ammonia as N, and more.
  - Sample types: SW (surface water grab), B (bankside piezometer), Sed (in-stream bed sediment porewater).
  - Depths: Piezometer cluster depths (UC upstream, DC downstream) with bank piezometers LB/RB and sub-labels 1–3; detailed porewater depth profiles.
  - Timeframes: 2013–2020s.

## Field Instrumentation and Methods
- Field tools: HOBO U20-001-01, Levelogger Edge (Solinst), Manta 2 (Eureka Water Probes).
- QA/QC for head and conductivity:
  - Head corrected for drift using manual dip measurements every 2–4 weeks; linear drift assumed.
  - Slug tests repeated when possible; comparisons of falling vs rising head results included; data quality notes provided.
  - Contacts for datasets: Andy Binley (a.binley@lancaster.ac.uk).
- Analytical chemistry and QC:
  - Oxygen by Unisense electrode; Fe(II) fixed in the field and analysed by UV spectrophotometry.
  - Ion chromatography for chloride, nitrate, sulphate; detection limits and RSDs provided; certified reference materials used.
  - ICP-OES for Ca, K, Mg, Na, Si, Sr; LODs and RSDs given; certified references used.
  - Phosphate, ammonia, nitrite by auto-analyser; LOD and QC details provided; certified references used.
  - DOC by non-purgeable organic carbon method; LOD and QC details provided.
  - Queries: Kate Heppell (c.m.heppell@qmul.ac.uk).
- Data structure notes:
  - Piezometers labeled by site: UC (upstream cluster) and DC (downstream cluster); bank clusters LB (left) and RB (right) with sub-labels 1, 2, 3.
  - Porewater sampling tubes extend to screen depth; multi-depth sampling available (0–100 cm in steps).
  - Data format specifics:
    - Hydraulic head: 6 spreadsheets; date/time in column A; subsequent columns per site; head in metres AOD.
    - Hydraulic conductivity: 5 columns: piezometer ID, test type (Rising/Falling), start date/time, Ksat, quality comments.
    - Porewater chemistry: 21+ columns including date, site, sample type, cluster, depth, and numerous analytes (with <LOD and na entries).
- Data accessibility: datasets described for upload to appropriate data portals; QA/QC and methodological notes embedded to ensure reproducibility.

## Data Quality and Documentation
- Data quality: explicit drift corrections, replicate slug-test measurements, cross-comparisons of test types, and detailed quality control notes.
- Analytical methods: comprehensive documentation of instruments, detection limits, precision (RSD), and certified reference materials to ensure traceability.
- Metadata: site coordinates (OS Grid References), site layout details (UC/DC, LB/RB, depth labeled conventions), and sample types clearly defined to support cross-site comparisons.

## Practical Implications for Monitoring
- Provides standardized time-series data across multiple sites for environmental health assessment and policy performance over time.
- Enables integration with other datasets for enhanced interpretation and modelling.
- Clear data ownership and contact points facilitate data access, validation, and reuse.

## Key Contacts
- Data queries for hydraulic head and conductivity: Andy Binley (a.binley@lancaster.ac.uk)
- Data queries for porewater chemistry: Kate Heppell (c.m.heppell@qmul.ac.uk)