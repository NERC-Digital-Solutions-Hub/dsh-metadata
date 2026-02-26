# Sample collection and fieldwork

- Overview
  - Describes the sampling workflow, measurements, laboratory analyses, calibration, and quality control for water quality assessment across baseline and follow-up periods.
  - Emphasizes preventing cross-contamination (microbiology sample taken before physico-chemical tests) and timely processing (within seven hours).

- Field sampling protocol
  - Approximately 500 ml water collected from each well using a stainless steel, pre-rinsed sampling cup.
  - Samples transferred to sterile plastic bottles and stored on ice, in the dark, during transport to the laboratory.
  - Handling aims to preserve sample integrity and minimize contamination risk.

- Measurements and instrumentation (in the field)
  - pH measured with a handheld pH meter (HI-98128 Pocket pHep5) calibrated with standard solutions.
  - Water temperature recorded using the meter’s integrated digital thermometer (note: thermometer not calibrated).
  - Depth to water (below ground level) measured with a dipper probe; depth calculated from calibrated tape, adjusted for plinth height.
  - Conductivity measured with a COND3110 handheld meter, calibrated with standard solutions.
  - Turbidity measured with a HI 93703 portable turbidity meter; sample cell rinsed between samples.

- Laboratory instrumentation and analytical methods
  - Microbiology: thermotolerant coliforms (TTC) quantified by membrane filtration using MLSB medium; 100 ml (or appropriate dilution) filtered, incubated at 44 ± 0.5°C for 20 ± 2 hours; colonies counted and standardized to 100 ml. No further confirmatory tests performed.
  - Chemistry: nitrate, sulfate, phosphate, fluoride, and chloride concentrations measured with a Palintest photometer 7100 using dedicated reagents and manufacturer instructions.

- Calibration steps and instrument performance
  - Incubator temperature checked and adjusted before each campaign; rechecked every two days during the campaign (thermometer used for calibration not itself calibrated against a reference thermometer).
  - pH meter calibrated daily with buffers at pH 4.0, 7.01, and 10.0; buffer solutions traceable to NIST.
  - Conductivity meter calibrated before each campaign with a 1413 µS standard; checked daily for consistency; recalibrated if readings deviated.
  - Turbidity meter calibrated daily against a formazin standard provided by the meter manufacturer.

- Quality control and data quality considerations
  - Analytical QC was challenging given laboratory facilities.
  - Blanks run for each method; when batch size allowed, duplicates performed on the first and last samples to assess repeatability.
  - Tests conducted by the same analyst throughout each campaign to reduce inter-operator variation.

- Data governance implications and metadata needs (for Data Stewards)
  - Document instrument IDs, calibration status, lot numbers, and standard solutions used; capture exact timings for sample collection, processing, and incubation.
  - Record environmental conditions, sample handling steps, and any deviations (e.g., thermometer calibration status) to support data provenance and audit trails.
  - Store results with units, detection limits, and identification of the matrix (water well or site); ensure traceability from field collection to laboratory results.
  - Flag any quality control issues (e.g., reliance on non-calibrated devices) and include them in metadata and data quality flags.
  - Prepare for data sharing by adopting consistent metadata schemas and ensuring that all data (field measurements, lab results, calibration records, and QA/QC) are versioned and stored in a central portal.